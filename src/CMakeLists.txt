llt_gpgpu_compile_i915(i915_memset.clch i915_memset.cl)
add_executable(i915_memset
	i915_memset.cc
	i915_memset.clch)

target_include_directories(i915_memset PRIVATE
	${LLT_GPGPU_RT_INCLUDE_DIRS}
	${CMAKE_CURRENT_BINARY_DIR})

target_link_libraries(i915_memset PRIVATE
	${LLT_GPGPU_RT_LIBRARIES})

llt_gpgpu_compile_i915(i915_xcb_display.clch i915_xcb_display.cl)
add_executable(i915_xcb_display
	i915_xcb_display.cc
	i915_xcb_display.clch)

target_include_directories(i915_xcb_display PRIVATE
	${LLT_GPGPU_RT_INCLUDE_DIRS}
	${XCB_INCLUDE_DIRS}
	${CMAKE_CURRENT_BINARY_DIR})

target_link_libraries(i915_xcb_display PRIVATE
	${LLT_GPGPU_RT_LIBRARIES}
	${XCB_LIBRARIES})
