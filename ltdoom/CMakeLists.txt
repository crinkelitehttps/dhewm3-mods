# this CMakeLists.txt is  supposed to be used (with add_subdirectory())
# from CMakeLists.txt in neo/mods/ which in turn is supposed to be used
# (with add_subdirectory()...) from CMakeLists.txt in neo/

# Linuxtrack Doom 3

# it's based on the base game (from game/), so use corresponding source files
# and add the dentonmod-specific files (tracer.cpp)
set(src_ltdoom
	${src_game_mods} # defined in neo/mods/CMakeLists.txt
	linuxtrack.c
)

# SETUP_MOD( name srclist compile_defs ) - also from neo/mods/CMakeLists.txt
# make sure to have quotes around srclist!
SETUP_MOD("ltdoom" "${src_ltdoom}" "GAME_DLL;_LTDOOM")
