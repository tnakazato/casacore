set (tests
dArrayAccessor
tArrayAccessor
tArrayBase
tArray
tArrayIO2
tArrayIO3
tArrayIO
tArrayIter1
tArrayIteratorSTL
tArrayIter
tArrayLogical
tArrayMath2
tArrayMath
tArrayMathPerf
tArrayMathTransform
tArrayOpsDiffShapes
tArrayPosIter
tArrayUtil
tArrayUtilPerf
tAxesSpecifier
tBoxedArrayMath
tCompareBoxedPartial
tConvertArray
tDiagonal
tExtendSpecifier
tIPosition
tLinAlgebra
tMaskArrExcp
tMaskArrIO
tMaskArrLogi
tMaskArrMath0
tMaskArrMath1
tMaskArrMath2
tMaskedArray
tMatrixMath
tMedianSmooth
tPerfTransform
tSlice
tSlicer
tSlidingArrayMath
tStringArray
tSumPerformance
tVector
tVectorSTLIterator
)

foreach (test ${tests})
    add_executable (${test} ${test}.cc)
    target_link_libraries (${test} casa_casa)
    add_test (${test} ${CMAKE_SOURCE_DIR}/cmake/cmake_assay ./${test})
    add_dependencies(check ${test})
endforeach (test)
