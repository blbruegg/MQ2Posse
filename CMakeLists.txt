# MQ2Posse
# Forked from RedGuides/MQ2Posse (github.com/RedGuides org sweep, forum-plugins-2026-08-02
# follow-up batch). Vendored as a git submodule tracking https://github.com/blbruegg/MQ2Posse
# (fork of RedGuides/MQ2Posse). See F:\\EQProject\\docs\\re_progress.md for the write-up.

include("../../Plugin.cmake")

set(MQ2Posse_SOURCES
    "MQ2Posse.cpp"
    "MQ2Posse.rc"
    "resource.h"
)

source_groups("Source Files" ${MQ2Posse_SOURCES})

add_library(MQ2Posse SHARED
    ${MQ2Posse_SOURCES}
)

set_target_properties(MQ2Posse PROPERTIES FOLDER "core/plugins")

target_Plugin_props(MQ2Posse)

target_link_libraries(MQ2Posse PRIVATE MQ2Main)
