cmake_minimum_required(VERSION 2.8)

set(COBRA_SETUP_PY_IN ${CMAKE_CURRENT_SOURCE_DIR}/setup.py.in)
set(COBRA_SETUP_PY ${CMAKE_CURRENT_BINARY_DIR}/setup.py)

configure_file(${COBRA_SETUP_PY_IN} ${COBRA_SETUP_PY})

install(
  CODE "execute_process(COMMAND ${PYTHON_EXECUTABLE} ${COBRA_SETUP_PY} install --user)"
  )
