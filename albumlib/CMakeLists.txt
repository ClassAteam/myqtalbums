add_library(albums "")

target_sources(albums
  PRIVATE
    ${CMAKE_CURRENT_LIST_DIR}/Album.cpp
  PUBLIC
    ${CMAKE_CURRENT_LIST_DIR}/Album.h
  PRIVATE
    ${CMAKE_CURRENT_LIST_DIR}/AlbumModel.cpp
  PUBLIC
    ${CMAKE_CURRENT_LIST_DIR}/AlbumModel.h
  PRIVATE
    ${CMAKE_CURRENT_LIST_DIR}/AlbumDao.cpp
  PUBLIC
    ${CMAKE_CURRENT_LIST_DIR}/AlbumDao.h
  PRIVATE
    ${CMAKE_CURRENT_LIST_DIR}/Picture.cpp
  PUBLIC
    ${CMAKE_CURRENT_LIST_DIR}/Picture.h
  PRIVATE
    ${CMAKE_CURRENT_LIST_DIR}/PictureModel.cpp
  PUBLIC
    ${CMAKE_CURRENT_LIST_DIR}/PictureModel.h
  PRIVATE
    ${CMAKE_CURRENT_LIST_DIR}/PictureDao.cpp
  PUBLIC
    ${CMAKE_CURRENT_LIST_DIR}/PictureDao.h
  PRIVATE
    ${CMAKE_CURRENT_LIST_DIR}/DatabaseManager.cpp
  PUBLIC
    ${CMAKE_CURRENT_LIST_DIR}/DatabaseManager.h
  )

target_include_directories(albums
  PUBLIC
    ${CMAKE_CURRENT_LIST_DIR}
  )

target_link_libraries(albums PRIVATE Qt${QT_VERSION_MAJOR}::Widgets)
target_link_libraries(albums PRIVATE Qt${QT_VERSION_MAJOR}::Core)
