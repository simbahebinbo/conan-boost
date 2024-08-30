 cmake_minimum_required(VERSION 3.15)

 project(conan-boost LANGUAGES CXX VERSION 1.0.0)

 set(CMAKE_POSITION_INDEPENDENT_CODE TRUE)
 set(CMAKE_CXX_STANDARD 20)
 set(CMAKE_CXX_STANDARD_REQUIRED ON)
 set(CMAKE_CXX_EXTENSIONS OFF)
 
 # 找到 Conan 生成的包配置文件
 find_package(boost REQUIRED)

 # 添加可执行文件
 add_executable(ip_list ip_list.cpp)
 add_executable(web_request web_request.cpp)
 add_executable(async_wait async_wait.cpp)
 add_executable(receiver receiver.cpp)
 add_executable(sender sender.cpp)

 # 链接 Boost 库
 target_link_libraries(ip_list Boost::boost)
 target_link_libraries(web_request Boost::boost)
 target_link_libraries(async_wait Boost::boost)
 target_link_libraries(receiver Boost::boost)
 target_link_libraries(sender Boost::boost)
