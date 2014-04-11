# MongoDB What's That File

MongoDB What's That File is a utility to print out documentation on the files in the MongoDB server
source tree.  It's based on the notes in https://github.com/Zarkantho/module_data/

## Setup

    git submodule init
    git submodule update

## Example Usage

    $ mongowtf src/mongo/s/config_upgrade.cpp
    system_title: Sharding
    system_description: Code related specifically to sharding support in MongoDB.  See
        http://docs.mongodb.org/manual/sharding/ for a high level description.
    system_module:
        module_title: Config Metadata Upgrade
        module_description: Code to handle the versioning and upgrading of metadata on
            the config servers
        module_group:
            group_title: Config Upgrade
            group_description: Code to upgrade config server metadata
            group_files:
            - src/mongo/s/config_upgrade.cpp
            - src/mongo/s/config_upgrade.h
            - src/mongo/s/config_upgrade_helpers.cpp
            - src/mongo/s/config_upgrade_helpers.h
            - src/mongo/s/config_upgrade_v0_to_v5.cpp
            - src/mongo/s/config_upgrade_v4_to_v5.cpp

## Notes

- Currently all data is based on MongoDB server version 2.6.
- To update the documentation for a file, see https://github.com/Zarkantho/module_data/
- The project https://github.com/Zarkantho/willitlink/ is used for some helper libraries and could
  in the future be used to display dependency information
