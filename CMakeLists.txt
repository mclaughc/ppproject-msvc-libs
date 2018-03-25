# Detect paths for shared includes/libs.
set(SHARED_INCLUDE_DIR "${CMAKE_CURRENT_SOURCE_DIR}/include")
if(CMAKE_SIZEOF_VOID_P EQUAL 8)
    set(SHARED_LIB_DIR "${CMAKE_CURRENT_SOURCE_DIR}/lib64")
else()
    set(SHARED_LIB_DIR "${CMAKE_CURRENT_SOURCE_DIR}/lib")
endif()

# Set paths for external dependencies.
set(LIBSNDFILE_INCLUDE_DIR "${SHARED_INCLUDE_DIR}" CACHE STRING "libsndfile include dir" FORCE)
set(LIBSNDFILE_LIBRARY "${SHARED_LIB_DIR}/libsndfile-1.lib" CACHE STRING "libsndfile libraries" FORCE)
set(FFTW_INCLUDES "${SHARED_INCLUDE_DIR}" CACHE STRING "libsndfile include dir" FORCE)
set(FFTW_LIBRARIES "${SHARED_LIB_DIR}/libfftw3-3.lib" CACHE STRING "libsndfile libraries" FORCE)

