remove_definitions(-DRDKIT_DISTGEOMETRY_BUILD)
rdkit_python_extension(DistGeom DistGeom.cpp
                       DEST DistanceGeometry
LINK_LIBRARIES DistGeometry EigenSolvers ForceField ForceFieldHelpers Optimizer RDGeneral RDGeometryLib RDBoost )


add_pytest(pyDistGeom ${CMAKE_CURRENT_SOURCE_DIR}/rough_test.py)




