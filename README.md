# Swiss Knowledge Graph for the Performing Arts
Within the scope of a master thesis in the field of business informatics at the Bern University of Applied Sciences, a prototypical version of a Swiss Knowledge Graph for the Performing Arts is implemented.
This Github repository serves as a storage for the files created during the development of the prototype. 

## Basic information
GraphDB Free from Ontotext was used as the triplestore in this project. 
The RDF files of the named graphs are stored in the "NamedGraphs" folder. These files contain all triples that were loaded into the triplestore during the development of the knowledge graph. The "Repositories" folder contains the configuration files of the two repositories used ("RawData" and "SwissKnowledgeGraphforthePerformingArts"). In the folder "Ontologies" all ontology files are stored, which were used in the triplestore.

The developed prototype can thus be recreated by creating the two repositories in GraphDB using the configuration files from the "Repositories" folder and loading the corresponding files from the "NamedGraphs" and "Ontologies" folders into the appropriate repositories in GraphDB.

Thus, for reproducing the knowledge graph, the RDF files are the most important. The CSV/Excel files in the folders of iterations 1-4 are stored for completeness. These files were only used to match entities with Wikidata (Reconcile Process) and create the corresponding RDF files using OntoRefine. 

The following section shows the structure of the iteration folders. Behind the respective file names a short description of the information they contain can be found. The following section thus serves as documentation of the procedure used in the development of the master thesis. 

## Structure of the iteration (1-4) folders

### Iteration 1
#### CSV/Excel
- “Iteration1_Grunddaten_schauspielhaus_repertoire_1938-1968 (1)”: Source data of the selected production
- “Iteration1_Event_schauspielhaus_repertoire_1938-1968 (1)”: Source data with date changed to ISO 8601 date format
- “Iteration1_Organization_schauspielhaus_repertoire_1938-1968-1-csv”: File of the class "Organization" 
- “Iteration1_Personen_schauspielhaus_repertoire_1938-1968 (1)”: File of the class “Person” 
- “Iteration1_Work_schauspielhaus_repertoire_1938-1968 (1)”: File of the class “Work” 
- “Iteration1_OpenRefine”: Production-file used for the reconcile process of all entities
- “Iteration1_EventGraphDB_schauspielhaus_repertoire_1938-1968 (1)”: Final production file for iteration 1 with links to the corresponding class entities 
#### RDF files
- "Iteration1_Event_V1": RDF file of the class "Performing Arts Production"
- "Iteration1_Person_V1": RDF file of the class "Person"
- "Iteration1_Organization_V1": RDF file of the class "Organization"
- "Iteration1_Work_V1": RDF file of the class "Work" 

### Iteration 2
#### CSV/Excel
- “schauspielhaus_repertoire_1938-1968 (1)”: Source data of the “Repertoire Schaus-pielhaus Zurich 1938-1968”  
- “Iteration2_Person”: File of the class “Person” with generated UUIDs and the Q-Identifiers from Wikidata (after reconcile process)
- “Iteration2_Work”: File of the class “Work” with generated UUIDs and the Q-Identifiers from Wikidata (after reconcile process)
- “Stück+UUID_PAE”: File of the Schauspielhaus Zurich productions matched with the Q-Identifier for the corresponding production entity in Wikidata (They all had a Q-Identifier since these productions were entered as part of a Wikidata-project). “Schaus-pielhaus Zürich” was added to the name of the work, because the corresponding Wiki-data entities of the Schauspielhaus Zürich productions could thus be better reconciled.
- “Iteration2_PerformingArtsProduction_V1.0”: Final version of the performing arts production data 

#### RDF files
- “Iteration2_Person_RDF”: RDF-File of class “Person”
- “Iteration2_Work_RDF”: RDF-File of class “Work”
- “Iteration2_Production_RDF_V0.1”: RDF-File of performing arts production

### Iteration 3
#### CSV/Excel
- “Schauspieler_Iteration3-csv_UTF8”: List of new actors (actors who still have a string value in the “RawData” repository in UTF8
- “NewAuthors_Iteration3_UTF8”: List of new authors (authors who still have a string value in the “RawData” repository in UTF8
- “NewStageDirectors_Iteration3_UTF8”: List of new stage directors (stage directors who still have a string value in the “RawData” repository in UTF8
- “NewAssistantStageDirectors_Iteration3_UTF8”: List of new assistant stage directors (assistant stage directors who still have a string value in the “RawData” repository in UTF8
- “Schauspieler_Iteration3-csv_UTF8_ohneDuplikate_mitUUID»: List of new actors without duplicates, with generated UUID identifier
- “NewAuthors_Iteration3_UTF8_ohneProduction+Duplikate_mitUUID”: List of new authors without duplicates, with generated UUID identifier
- “NewStageDirectors_Iteration3_UTF8_ohneProduction+Duplikate_mitUUID”: List of new stage directors without duplicates, with generated UUID identifier
- “NewAssistantStageDirec-tors_Iteration3_UTF8_ohneProduction+Duplikate_mitUUID”: List of new assistant stage directors without duplicates, with generated UUID identifier
- “NewActors_Iteration3”: Final Table of new actors with all the information needed to construct the RDF file with OntoRefine
- “NewAuthors_Iteration3_Final”: Final Table of new authors with all the information needed to construct the RDF file with OntoRefine
- “NewStageDirectors_Iteration3_Final”: Final Table of new stage directors with all the information needed to construct the RDF file with OntoRefine
- “NewAssistantStageDirectors_Iteration3_Final”: Final Table of new assistant stage directors with all the information needed to construct the RDF file with OntoRefine

#### RDF files
- “NewActors_Iteration3”: RDF-File of new actors
- “ExistingActors_Iteration3”: RDF-File of existing actors (which had already an existing identifier in the triplestore)
- “ProductionCompany+Venues”: RDF-File with data of the production company and venues
- “NewAuthors_Iteration3”: RDF-File of new authors
- “NewStageDirectors_Iteration3”: RDF-File of new stage directors
- “NewAssistantStageDirectors_Iteration3”: RDF-File of new assistant stage directors
- “ExistingAuthors_Iteration3”: RDF-File of existing authors (which had already an existing identifier in the triplestore)
- “ExistingStageDirectors_Iteration3”: RDF-File of existing stage directors (which had already an existing identifier in the triplestore)
- “ExistingAssistantStageDirector”: RDF-File of existing assistant stage directors (which had already an existing identifier in the triplestore)
- “ÜbrigeBeteiligteMitSAPAID”: RDF-File with data of additional roles, which were imported directly from SAPA with the corresponding identifiers (Conductor, Performer, Cos-tumeDesigner, Dancer, Narrator, Puppeteer, Music Performer, Choreographer, SoundDesigner, LightingDesigner, ProjectionDe-signer, VideoDesigner, Dramaturgy, Scenographer)

### Iteration 4
#### Huginn
- add-raw-event.sparql: This SPARQL query is used in connection with a Huginn agent. With this SPARQL query the desired triples are generated. 

#### agents (JSON files)
- kleintheater-grenchen (1): Agents to crawl the website of the Kleintheater Grenchen
- theater-winkelwiese (1): Agents to crawl the website of the Theater Winkelwiese
- load-data-to-graphdb: Agents used to load the crawled data into the triplestore. 





