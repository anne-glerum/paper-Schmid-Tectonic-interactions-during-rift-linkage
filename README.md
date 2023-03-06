# paper-Schmid-Tectonic-interactions-during-rift-linkage
This repository provides the input files, ASPECT installation details and additional ASPECT plugins used for the paper 

*Schmid et al. (2023). Tectonic interactions during rift linkage: Insights from analog and numerical experiments.*

by

*T. C. Schmid, S. Brune, A. Glerum and G. Schreurs.*

# Documentation
The numerical simulations presented in this paper were run with the geodynamics code ASPECT (https://aspect.geodynamics.org/).

## ASPECT version
The ASPECT input files provided in this repository correspond to the ASPECT branch 

https://github.com/EstherHeck/aspect/commits/fastscape_update_again_as_on14thJanuary_for_Timi

This branch is built on commit a584ccce71a736a31b577895f26967c823b9e75d of the ASPECT main version
which can be found at https://github.com/geodynamics/aspect.

## Additional ASPECT plugins
For the initial model conditions, we used the ASPECT plugins in the folder /plugins. 
The file CMakeLists.txt can be used to install these plugins as shared libraries
against your ASPECT installation.

The files for the plugin that outputs the stress regime can be found here:
https://github.com/anne-glerum/aspect/blob/paper-Victoria-microplate-rotation/source/postprocess/visualization/stress_regime.cc
https://github.com/anne-glerum/aspect/blob/paper-Victoria-microplate-rotation/include/aspect/postprocess/visualization/stress_regime.h

## ASPECT input files
The ASPECT input files can be found in the folder /prms.
The file `prms/model_list.txt` contains a table linking
prm file names to the model characteristics in the paper. 

## System requirements and installation
ASPECT was built using the underlying library deal.II 10.0.0-pre 
on the German HLRN cluster Lise with the following specifications:
```
###
#
#  ASPECT configuration:
#        ASPECT_VERSION:            2.4.0-pre
#        GIT REVISION:              cbba35f (fastscape_update_again_as_on14thJanuary_for_Timi)
#        CMAKE_BUILD_TYPE:          Release
#
#        DEAL_II_DIR:               /home/projects/bbp00039/fastscape_build_files/misc/deal.IIdev-master/lib/cmake/deal.II
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
#        CMAKE_BINARY_DIR:          /home/bbkeheck/build-for-Timi
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
