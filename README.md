# paper-Schmid-Tectonic-interactions-during-rift-linkage
This repository provides the input files, ASPECT installation details and additional ASPECT plugins used for the paper 

*Schmid et al. (2023). Tectonic interactions during rift linkage: Insights from analog and numerical experiments.*

by

*T. C. Schmid, S. Brune, A. Glerum and G. Schreurs.*

# Documentation
The numerical simulations presented in this paper were run with the geodynamics code ASPECT (https://aspect.geodynamics.org/).

## ASPECT version
The ASPECT input files provided in this repository correspond to the ASPECT branch 

https://github.com/EstherHeck/aspect/commits/fastscape_update_again_erosional_base_level-undo2780-before-rebase-on13mai22

This branch is built on commit 84d40e7 of the ASPECT main version,
which can be found at https://github.com/geodynamics/aspect.

## Additional ASPECT plugins
For the initial model conditions, we used the ASPECT plugins in the folder /plugins. 
The file CMakeLists.txt can be used to install these plugins as shared libraries
against your ASPECT installation.

## ASPECT input files
The ASPECT input files can be found in the folder /prms.
The file `prms/model_list.txt` contains a table linking
prm file names to the model characteristics in the paper. 

## Installation details
ASPECT was built using the underlying library deal.II 10.0.0-pre 
on the German HLRN cluster Lise with the following specifications:
```
###
#
#  ASPECT configuration:
#        ASPECT_VERSION:            2.4.0-pre
#        GIT REVISION:              aa6d41f (fastscape_update_again_erosional_base_level-undo2780-before-rebase-on13mai22)
#        CMAKE_BUILD_TYPE:          Release
#
#        DEAL_II_DIR:               /home/projects/bbp00039/fastscape_build_files/misc/deal.IIdev-master-15th-feb-22/deal.IIdev-master/lib/cmake/deal.II
#        DEAL_II VERSION:           10.0.0-pre
#        ASPECT_USE_FP_EXCEPTIONS:  ON
#        ASPECT_RUN_ALL_TESTS:      OFF
#        ASPECT_USE_SHARED_LIBS:    ON
#        ASPECT_HAVE_LINK_H:        ON
#        ASPECT_WITH_LIBDAP:        OFF
#        ASPECT_WITH_WORLD_BUILDER: ON /home/bbkeheck/aspect/contrib/world_builder
#        ASPECT_PRECOMPILE_HEADERS: ON
#        ASPECT_UNITY_BUILD:        ON
#
#        CMAKE_INSTALL_PREFIX:      /usr/local
#        CMAKE_SOURCE_DIR:          /home/bbkeheck/aspect
#        CMAKE_BINARY_DIR:          /home/bbkeheck/build-release-fastscape-undo2780-plusStrati-devDeal
#        CMAKE_CXX_COMPILER:        GNU 9.2.0 on platform Linux x86_64
#                                   /sw/comm/openmpi/3.1.5/skl/gcc/bin/mpicxx
#        PARAMETER_GUI_EXECUTABLE:  PARAMETER_GUI_EXECUTABLE-NOTFOUND
#
#        LINKAGE:                   DYNAMIC
#
#        COMPILE_FLAGS:             
#
#        _WITH_CXX14:               ON
#        _WITH_CXX17:               FALSE
#        _MPI_VERSION:              3.1
#        _WITH_64BIT_INDICES:       OFF
#
###
```
