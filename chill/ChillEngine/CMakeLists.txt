CMAKE_MINIMUM_REQUIRED(VERSION 2.6)
PROJECT(ChillEngine)

include(UseCXX17)

ADD_LIBRARY( ChillEngine STATIC
	Processor.h
	ProcessingGraph.h
	LuaProcessor.h
	
	ProcessingGraph.cpp
	Processor.cpp
	GroupProcessors.cpp
	LuaProcessor.cpp

	Style.h
	UI.h
	UI.cpp
	NodeEditor.h
	NodeEditor.cpp

	VisualComment.h
	VisualComment.cpp

	IOTypes.h
	IOs.h
	IOs.cpp
  
	GraphSaver.h
	GraphSaver.cpp
  
	FileDialog.h
	FileDialog.cpp

	Resources.h
	SourcePath.h
  )

TARGET_LINK_LIBRARIES(ChillEngine
        tinyfiledialogs
        lua
	luabind
	LibSL
	LibSL_gl
)

SET_PROPERTY(TARGET ChillEngine APPEND PROPERTY
   INTERFACE_INCLUDE_DIRECTORIES
 			${CMAKE_CURRENT_SOURCE_DIR}
)
SET_TARGET_PROPERTIES(ChillEngine PROPERTIES DEBUG_POSTFIX "-d")
set_target_properties(ChillEngine PROPERTIES ENABLE_EXPORTS ON)
