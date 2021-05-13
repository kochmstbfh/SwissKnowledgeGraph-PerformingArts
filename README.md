# Swiss Knowledge Graph for the Performing Arts
Within the scope of a master thesis in the field of business informatics at the Bern University of Applied Sciences, a prototypical version of a Swiss Knowledge Graph for the Performing Arts is implemented.
This Github repository serves as a storage for the files created during the development of the prototype. 

## Github repository structure

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

