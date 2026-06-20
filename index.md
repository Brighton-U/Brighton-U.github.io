---
layout: default
---

- [Professional Self-Assessment](#professional-self-assessment)
- [Code Review](#code-review)
- [Enhancement 1](#enhancement-1-software-design-and-engineering)
- [Enhancement 2](#enhancement-2-algorithms-and-data-structures)
- [Enhancement 3](#enhancement-3-databases)

## Professional Self-Assessment
> TODO: Finish professional self-assessment

## Code Review
<div style="position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden;">
  <iframe 
    src="https://www.youtube.com/embed/XmJoiTorFZo?si=UDx-yVo4MTU6OwPW" 
    style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"
    frameborder="0"
    allowfullscreen
  >
  </iframe>
</div>

## Enhancement 1: Software Design and Engineering
[Enhanced Artifact](https://github.com/reeduxx/yet-another-pokemon-randomizer/tree/enhancement-1)
Prior to this enhancement, the project used hardcoded game definitions for each game version and generation that was supported. This meant that in order to support a new game version, the source code would have to be modified. To improve scalability and extensibility, this system was redesigned to load game definitions dynamically from external JSON files, separating the static data from the business logic. This system also allowed optional user-defined game definitions to be loaded from a designated directory. I implemented a modular loader, factory, and registry architecture to support these definitions, incorporating schema validation using Pydantic to ensure that definitions were properly structured and validated before use.

## Enhancement 2: Algorithms and Data Structures
[Enhanced Artifact](https://github.com/reeduxx/yet-another-pokemon-randomizer/tree/enhancement-2)
Several components of this enhancement showcase these skills. I implemented filtering systems that allow Pokémon species to be selected according to user-defined constraints, including base stat total ranges and type restrictions. These filtering operations require efficient traversal and evaluation of collections of species data. I also designed and implemented a type-trio generation system that allows users to generate starter Pokémon based on predefined type relationships, such as the traditional grass, fire, and water trio. This required the creation of data structures to represent type combinations and algorithms capable of selecting valid Pokémon  while enforcing uniqueness and user-defined restrictions. The starter generation algorithm combines multiple filtering and validation steps to produce valid randomized results while maintaining the constraints established by the user. Two planned features that were not fully realized in this enhancement were exclusion systems for legendary Pokémon and evolutionary families. They have been partially implemented in the source code but not fully realized in the user interface.

## Enhancement 3: Databases
[Enhanced Artifact](https://github.com/reeduxx/yet-another-pokemon-randomizer/tree/enhancement-3)
Several components of this enhancement showcase my software development and database skills. I designed a relational schema consisting of separate tables for game definitions and related offsets, connected through foreign key relationships. I implemented uniqueness constraints to prevent duplicate records and indexes to improve lookup performance. A repository layer was also introduced to abstract database operations from the rest of the application and provide methods for inserting, retrieving, and querying game definitions. Additionally, an importer was designed to transform validated JSON definitions into database records. I also created a database manager for coordinating schema creation, data imports, and data retrieval. Finally, the database layer was integrated into the existing game registry workflow so that game definitions are validated, imported into SQLite, and then loaded from the database before being used by the application. In addition to these changes for the enhancement, I also continued to develop additional tests regarding validation coverage.
