set(HEADERS
  gr.h
  lib2d.h)
set(CPPS
  font.cpp
  hardsurf.cpp
  memsurf.cpp
  pen.cpp
  pentext.cpp
  screen.cpp
  surface.cpp
  viewport.cpp
)

add_library(2dlib STATIC ${HEADERS} ${CPPS})
target_link_libraries(2dlib PRIVATE
  cfile
  logger
  mem
  misc
)
target_include_directories(2dlib PUBLIC
  $<BUILD_INTERFACE:
    ${PROJECT_SOURCE_DIR}/2dlib
  >
)
