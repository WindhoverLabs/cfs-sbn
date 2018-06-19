# Set local variables
set(APPTARGET sbn)

# Set source files
set(APP_SRC 
	${CMAKE_CURRENT_SOURCE_DIR}/../src/sbn_app.c
	${CMAKE_CURRENT_SOURCE_DIR}/../src/sbn_netif.c)
	
# Set include paths
set(APP_INC_DIRS 
	$ENV(CFE_CORE_SRC)/sb
	${CMAKE_CURRENT_SOURCE_DIR}/../src/)
include_directories(${APP_INC_DIRS})
include_directories(${CFE_INC_DIRS})
include_directories(${OSAL_INC_DIRS})
include_directories(${PSP_INC_DIRS})
	
# Build application
add_app(${APP_FILE} SHARED ${APP_SRC})

