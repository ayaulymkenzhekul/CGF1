cmake_minimum_required (VERSION 3.8)

# Название проекта
project("CGF1")

# Стандарт языка
set(CMAKE_CXX_STANDARD 20)

# Если компилятор MSVC — включаем горячую перезагрузку
if (POLICY CMP0141)
  cmake_policy(SET CMP0141 NEW)
  set(CMAKE_MSVC_DEBUG_INFORMATION_FORMAT "$<IF:$<AND:$<C_COMPILER_ID:MSVC>,$<CXX_COMPILER_ID:MSVC>>,$<$<CONFIG:Debug,RelWithDebInfo>:EditAndContinue>,$<$<CONFIG:Debug,RelWithDebInfo>:ProgramDatabase>>")
endif()

# Ищем библиотеки
find_package(OpenGL REQUIRED)
find_package(glfw3 CONFIG REQUIRED)
find_package(GLEW REQUIRED)

# --- Основной проект (оставим как есть) ---
add_executable(CGF1 "CGF1.cpp" "CGF1.h")
target_link_libraries(CGF1 PRIVATE OpenGL::GL glfw GLEW::GLEW)

# --- Пример 1: красный треугольник ---
add_executable(red_triangle "red_triangle.cpp")
target_link_libraries(red_triangle PRIVATE OpenGL::GL glfw GLEW::GLEW)

# --- Пример 2: синий квадрат ---
add_executable(blue_square "blue_square.cpp")
target_link_libraries(blue_square PRIVATE OpenGL::GL glfw GLEW::GLEW)
