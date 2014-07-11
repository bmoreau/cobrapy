cmake_minimum_required(VERSION 2.8)

set(COBRA_SETUP_PY ${CMAKE_CURRENT_SOURCE_DIR}/setup.py)

install(
  CODE "execute_process(COMMAND ${PYTHON_EXECUTABLE} ${COBRA_SETUP_PY} install --user WORKING_DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR})"
  )
