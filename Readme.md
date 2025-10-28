# Kautham demos

The purpose of this repository is to propose a Kautham project structure that guarantees it can be opened using the Kautham GUI. The recommended use is to copy this repository in the user's own workspace, and follow its structure by editing and adding their own files. 

There is **no** Kautham code in this repository, and it requires no installation of any kind. 


## Directory structure


your_kautham_project
├── models
│   ├── robots
│   └── obstacles
└── your_scenarios_folder
    └── singular_scenario_folder




### Folder Descriptions

- **`your_kautham_project/`**  
  This is the root folder containing all files related to your Kautham project.  

  - **`models/`**  
    This folder stores all the models that Kautham uses. **Do not rename or move this folder** — Kautham expects it to be located exactly two levels above the `.xml` problem file by default.  
      
    Inside this folder, you can organize models for robots and obstacles however you like, as long as any `.xacro` files reference the correct relative paths.  

    For detailed recommendations on structuring and referencing model files, see [these instructions](your_kautham_project/models/README.md).

  - **`your_scenarios_folder/`**  
    This folder contains one or more subfolders, each representing a distinct scenario in Kautham. A scenario folder defines a specific setup, including its configuration and problem files.

    It is recommended (though not strictly required) to create a separate scenario folder for each unique combination of robot and environment. Within a scenario, you can include multiple Kautham problem files to represent different configurations or queries — for example, adding new objects (like a can) or using alternative control files.
