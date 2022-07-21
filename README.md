# gvd-neo4j

usr: neo4j
psw: gvd


[neo4j sandbox](https://neo4j.com/sandbox/)

[import data](https://neo4j.com/developer/desktop-csv-import/#loadcsv-desktop)


# Configuracion del entorno Neo4j Desktop

En el siguiente paso a paso se presenta la carga de datos para creaar los nodos y relaciones de materias y alumnos con la herramienta `cypher-shell`.

1. Click the drop-down menu to the right of the Open button and select Terminal.

2. Enter bin/cypher-shell and log in with user `neo4j` and password `gvd`.

# Carga de datos

1. Lista de materias

```
neo4j@neo4j> CREATE ( GdP: Materia { nombre: 'Gestion de Proyectos', codigo: 'GdP', electiva: false });
             CREATE ( PdI: Materia { nombre: 'Protocolos de Internet', codigo: 'PdI', electiva: false });
             CREATE ( DDA1: Materia { nombre: 'Desarrollo de Aplicaciones 1', codigo: 'DDA1', electiva: false });
             CREATE ( AdD: Materia { nombre: 'Arquitectura de datos', codigo: 'AdD', electiva: true });
             CREATE ( AdP: Materia { nombre: 'Arquitectura de protocoloes', codigo: 'AdP', electiva: false });
             CREATE ( DDA2: Materia { nombre: 'Desarrollo de Aplicaciones 2', codigo: 'DDA2', electiva: true });
             CREATE ( BD: Materia { nombre: 'Big Data', codigo: 'BD', electiva: false });
             CREATE ( DDA3: Materia { nombre: 'Desarrollo de Aplicaciones 3', codigo: 'DDA3', electiva: false });
0 rows
ready to start consuming query after 204 ms, results consumed after another 0 ms
Added 1 nodes, Set 3 properties, Added 1 labels
0 rows
ready to start consuming query after 24 ms, results consumed after another 0 ms
Added 1 nodes, Set 3 properties, Added 1 labels
0 rows
ready to start consuming query after 22 ms, results consumed after another 0 ms
Added 1 nodes, Set 3 properties, Added 1 labels
0 rows
ready to start consuming query after 24 ms, results consumed after another 0 ms
Added 1 nodes, Set 3 properties, Added 1 labels
0 rows
ready to start consuming query after 26 ms, results consumed after another 0 ms
Added 1 nodes, Set 3 properties, Added 1 labels
0 rows
ready to start consuming query after 24 ms, results consumed after another 0 ms
Added 1 nodes, Set 3 properties, Added 1 labels
0 rows
ready to start consuming query after 24 ms, results consumed after another 0 ms
Added 1 nodes, Set 3 properties, Added 1 labels
0 rows
ready to start consuming query after 24 ms, results consumed after another 0 ms
Added 1 nodes, Set 3 properties, Added 1 labels
```

2. Lista de alumnos

```
neo4j@neo4j> CREATE ( A1: Alumno { nombre: 'Joseph-Louis', apellido: 'Lagrange', dni: '00000001', esDocente: false });
             CREATE ( A2: Alumno { nombre: 'Pierre-Simon', apellido: 'Laplace', dni: '00000002', esDocente: false });
             CREATE ( A3: Alumno { nombre: 'Andre-Marie', apellido: 'Ampere', dni: '00000003', esDocente: false });
             CREATE ( A4: Alumno { nombre: 'Augustin-Louis', apellido: 'Cauchy', dni: '00000004', esDocente: false });
             CREATE ( A5: Alumno { nombre: 'Augustin-Jean', apellido: 'Fresnel', dni: '00000005', esDocente: false });
             CREATE ( A6: Alumno { nombre: 'Charles-Augustin', apellido: 'de Coulomb', dni: '00000006', esDocente: true });
             CREATE ( A7: Alumno { nombre: 'Leon', apellido: 'Foucault', dni: '00000007', esDocente: true });
             CREATE ( A8: Alumno { nombre: 'Simeon Denis', apellido: 'Poisson', dni: '00000008', esDocente: false });
             CREATE ( A9: Alumno { nombre: 'Jerome', apellido: 'Lalande', dni: '00000009', esDocente: false });
             CREATE ( A10: Alumno { nombre: 'Jacques', apellido: 'Triger', dni: '00000010', esDocente: false });
0 rows
ready to start consuming query after 110 ms, results consumed after another 0 ms
Added 1 nodes, Set 4 properties, Added 1 labels
0 rows
ready to start consuming query after 23 ms, results consumed after another 0 ms
Added 1 nodes, Set 4 properties, Added 1 labels
0 rows
ready to start consuming query after 26 ms, results consumed after another 0 ms
Added 1 nodes, Set 4 properties, Added 1 labels
0 rows
ready to start consuming query after 25 ms, results consumed after another 0 ms
Added 1 nodes, Set 4 properties, Added 1 labels
0 rows
ready to start consuming query after 20 ms, results consumed after another 0 ms
Added 1 nodes, Set 4 properties, Added 1 labels
0 rows
ready to start consuming query after 26 ms, results consumed after another 0 ms
Added 1 nodes, Set 4 properties, Added 1 labels
0 rows
ready to start consuming query after 22 ms, results consumed after another 0 ms
Added 1 nodes, Set 4 properties, Added 1 labels
0 rows
ready to start consuming query after 34 ms, results consumed after another 0 ms
Added 1 nodes, Set 4 properties, Added 1 labels
0 rows
ready to start consuming query after 27 ms, results consumed after another 0 ms
Added 1 nodes, Set 4 properties, Added 1 labels
0 rows
ready to start consuming query after 30 ms, results consumed after another 0 ms
Added 1 nodes, Set 4 properties, Added 1 labels
```


3. Lista de profesores

```
neo4j@neo4j> CREATE ( P1: Profesor { nombre: 'Marc', apellido: 'Seguin', dni: '00000011'});
             CREATE ( P2: Profesor { nombre: 'Henri', apellido: 'Tresca', dni: '00000012'});
             CREATE ( P3: Profesor { nombre: 'Jean-Victor', apellido: 'Poncelet', dni: '00000013'});
             CREATE ( P4: Profesor { nombre: 'Georges', apellido: 'Cuvier', dni: '00000014'});
             CREATE ( P5: Profesor { nombre: 'Michel', apellido: 'Chasles', dni: '00000015'});
             CREATE ( P6: Profesor { nombre: 'Antoine', apellido: 'Lavoisier', dni: '00000016'});
             CREATE ( P7: Profesor { nombre: 'Jules', apellido: 'Jamin', dni: '00000017'});
             CREATE ( P8: Profesor { nombre: 'Louis Le', apellido: 'Chatelier', dni: '00000018'});
0 rows
ready to start consuming query after 46 ms, results consumed after another 0 ms
Added 1 nodes, Set 3 properties, Added 1 labels
0 rows
ready to start consuming query after 21 ms, results consumed after another 0 ms
Added 1 nodes, Set 3 properties, Added 1 labels
0 rows
ready to start consuming query after 27 ms, results consumed after another 0 ms
Added 1 nodes, Set 3 properties, Added 1 labels
0 rows
ready to start consuming query after 31 ms, results consumed after another 0 ms
Added 1 nodes, Set 3 properties, Added 1 labels
0 rows
ready to start consuming query after 26 ms, results consumed after another 0 ms
Added 1 nodes, Set 3 properties, Added 1 labels
0 rows
ready to start consuming query after 30 ms, results consumed after another 0 ms
Added 1 nodes, Set 3 properties, Added 1 labels
0 rows
ready to start consuming query after 25 ms, results consumed after another 0 ms
Added 1 nodes, Set 3 properties, Added 1 labels
0 rows
ready to start consuming query after 25 ms, results consumed after another 0 ms
Added 1 nodes, Set 3 properties, Added 1 labels
```


4. Lista de relaciones DICTO (docentes)

```
neo4j@neo4j> MATCH (P2: Profesor { apellido:"Chatelier"}), (AdD: Materia { codigo: "AdD"} ) CREATE (P2)-[:DICTO{ans: 2016, semestre: 1}]->(AdD);
             MATCH (P2: Profesor { apellido:"Chatelier"}), (AdD: Materia { codigo: "AdD"} ) CREATE (P2)-[:DICTO{ans: 2017, semestre: 1}]->(AdD);
             MATCH (P3: Profesor { apellido:"Chatelier"}), (AdP: Materia { codigo: "AdP"} ) CREATE (P3)-[:DICTO{ans: 2017, semestre: 1}]->(AdP);
             MATCH (P2: Profesor { apellido:"Chatelier"}), (AdD: Materia { codigo: "AdD"} ) CREATE (P2)-[:DICTO{ans: 2018, semestre: 1}]->(AdD);
             MATCH (P3: Profesor { apellido:"Chatelier"}), (AdP: Materia { codigo: "AdP"} ) CREATE (P3)-[:DICTO{ans: 2018, semestre: 1}]->(AdP);
             MATCH (P2: Profesor { apellido:"Chatelier"}), (AdD: Materia { codigo: "AdD"} ) CREATE (P2)-[:DICTO{ans: 2019, semestre: 1}]->(AdD);
             MATCH (P3: Profesor { apellido:"Chatelier"}), (AdP: Materia { codigo: "AdP"} ) CREATE (P3)-[:DICTO{ans: 2019, semestre: 1}]->(AdP);
             MATCH (P1: Profesor { apellido:"Chatelier"}), (GdP: Materia { codigo: "GdP"} ) CREATE (P1)-[:DICTO{ans: 2020, semestre: 1}]->(GdP);
             MATCH (P2: Profesor { apellido:"Chatelier"}), (AdD: Materia { codigo: "AdD"} ) CREATE (P2)-[:DICTO{ans: 2020, semestre: 1}]->(AdD);
             MATCH (P3: Profesor { apellido:"Chatelier"}), (AdP: Materia { codigo: "AdP"} ) CREATE (P3)-[:DICTO{ans: 2020, semestre: 1}]->(AdP);
             MATCH (P1: Profesor { apellido:"Chatelier"}), (GdP: Materia { codigo: "GdP"} ) CREATE (P1)-[:DICTO{ans: 2021, semestre: 1}]->(GdP);
             MATCH (P2: Profesor { apellido:"Chatelier"}), (AdD: Materia { codigo: "AdD"} ) CREATE (P2)-[:DICTO{ans: 2021, semestre: 1}]->(AdD);
             MATCH (P3: Profesor { apellido:"Chatelier"}), (AdP: Materia { codigo: "AdP"} ) CREATE (P3)-[:DICTO{ans: 2021, semestre: 1}]->(AdP);
             
             MATCH (P2: Profesor { apellido:"Jamin"}), (BD: Materia { codigo: "BD"} ) CREATE (P2)-[:DICTO{ans: 2021, semestre: 1}]->(BD);
             MATCH (P2: Profesor { apellido:"Jamin"}), (AdP: Materia { codigo: "AdP"} ) CREATE (P2)-[:DICTO{ans: 2021, semestre: 1}]->(AdP);
             
             MATCH (P3: Profesor { apellido:"Lavoisier"}), (PdI: Materia { codigo: "PdI"} ) CREATE (P3)-[:DICTO{ans: 2018, semestre: 1}]->(PdI);
             MATCH (P3: Profesor { apellido:"Lavoisier"}), (PdI: Materia { codigo: "PdI"} ) CREATE (P3)-[:DICTO{ans: 2019, semestre: 1}]->(PdI);
             MATCH (P3: Profesor { apellido:"Lavoisier"}), (PdI: Materia { codigo: "PdI"} ) CREATE (P3)-[:DICTO{ans: 2020, semestre: 1}]->(PdI);
             MATCH (P3: Profesor { apellido:"Lavoisier"}), (PdI: Materia { codigo: "PdI"} ) CREATE (P3)-[:DICTO{ans: 2021, semestre: 1}]->(PdI);
             
             MATCH (P4: Profesor { apellido:"Chasles"}), (DDA1: Materia { codigo: "DDA1"} ) CREATE (P4)-[:DICTO{ans: 2017, semestre: 1}]->(DDA1);
             MATCH (P4: Profesor { apellido:"Chasles"}), (DDA1: Materia { codigo: "DDA1"} ) CREATE (P4)-[:DICTO{ans: 2018, semestre: 1}]->(DDA1);
             MATCH (P4: Profesor { apellido:"Chasles"}), (DDA1: Materia { codigo: "DDA1"} ) CREATE (P4)-[:DICTO{ans: 2019, semestre: 1}]->(DDA1);
             MATCH (P4: Profesor { apellido:"Chasles"}), (DDA1: Materia { codigo: "DDA1"} ) CREATE (P4)-[:DICTO{ans: 2020, semestre: 1}]->(DDA1);
             MATCH (P4: Profesor { apellido:"Chasles"}), (DDA1: Materia { codigo: "DDA1"} ) CREATE (P4)-[:DICTO{ans: 2021, semestre: 1}]->(DDA1);
             
             
             MATCH (P5: Profesor { apellido:"Cuvier"}), (DDA3: Materia { codigo: "DDA3"} ) CREATE (P5)-[:DICTO{ans: 2014, semestre: 1}]->(DDA3);
             MATCH (P5: Profesor { apellido:"Cuvier"}), (DDA3: Materia { codigo: "DDA3"} ) CREATE (P5)-[:DICTO{ans: 2015, semestre: 1}]->(DDA3);
             MATCH (P5: Profesor { apellido:"Cuvier"}), (DDA3: Materia { codigo: "DDA3"} ) CREATE (P5)-[:DICTO{ans: 2016, semestre: 1}]->(DDA3);
             MATCH (P5: Profesor { apellido:"Cuvier"}), (DDA3: Materia { codigo: "DDA3"} ) CREATE (P5)-[:DICTO{ans: 2017, semestre: 1}]->(DDA3);
             MATCH (P5: Profesor { apellido:"Cuvier"}), (DDA3: Materia { codigo: "DDA3"} ) CREATE (P5)-[:DICTO{ans: 2018, semestre: 1}]->(DDA3);
             MATCH (P5: Profesor { apellido:"Cuvier"}), (DDA3: Materia { codigo: "DDA3"} ) CREATE (P5)-[:DICTO{ans: 2019, semestre: 1}]->(DDA3);
             MATCH (P5: Profesor { apellido:"Cuvier"}), (DDA3: Materia { codigo: "DDA3"} ) CREATE (P5)-[:DICTO{ans: 2020, semestre: 1}]->(DDA3);
             MATCH (P5: Profesor { apellido:"Cuvier"}), (DDA3: Materia { codigo: "DDA3"} ) CREATE (P5)-[:DICTO{ans: 2021, semestre: 1}]->(DDA3);
             
             
             MATCH (P6: Profesor { apellido:"Poncelet"}), (DDA1: Materia { codigo: "DDA1"} ) CREATE (P6)-[:DICTO{ans: 2021, semestre: 1}]->(DDA1);
             
             MATCH (P7: Profesor { apellido:"Tresca"}), (DDA2: Materia { codigo: "DDA2"} ) CREATE (P7)-[:DICTO{ans: 2017, semestre: 1}]->(DDA2);
             MATCH (P7: Profesor { apellido:"Tresca"}), (DDA2: Materia { codigo: "DDA2"} ) CREATE (P7)-[:DICTO{ans: 2018, semestre: 1}]->(DDA2);
             MATCH (P7: Profesor { apellido:"Tresca"}), (DDA2: Materia { codigo: "DDA2"} ) CREATE (P7)-[:DICTO{ans: 2019, semestre: 1}]->(DDA2);
             MATCH (P7: Profesor { apellido:"Tresca"}), (DDA2: Materia { codigo: "DDA2"} ) CREATE (P7)-[:DICTO{ans: 2020, semestre: 1}]->(DDA2);
             MATCH (P7: Profesor { apellido:"Tresca"}), (DDA2: Materia { codigo: "DDA2"} ) CREATE (P7)-[:DICTO{ans: 2021, semestre: 1}]->(DDA2);
             
0 rows
ready to start consuming query after 185 ms, results consumed after another 0 ms
Created 3 relationships, Set 6 properties
0 rows
ready to start consuming query after 13 ms, results consumed after another 0 ms
Created 3 relationships, Set 6 properties
0 rows
ready to start consuming query after 47 ms, results consumed after another 0 ms
Created 3 relationships, Set 6 properties
0 rows
ready to start consuming query after 14 ms, results consumed after another 0 ms
Created 3 relationships, Set 6 properties
0 rows
ready to start consuming query after 19 ms, results consumed after another 0 ms
Created 3 relationships, Set 6 properties
0 rows
ready to start consuming query after 16 ms, results consumed after another 0 ms
Created 3 relationships, Set 6 properties
0 rows
ready to start consuming query after 13 ms, results consumed after another 0 ms
Created 3 relationships, Set 6 properties
0 rows
ready to start consuming query after 54 ms, results consumed after another 0 ms
Created 4 relationships, Set 8 properties
0 rows
ready to start consuming query after 15 ms, results consumed after another 0 ms
Created 3 relationships, Set 6 properties
0 rows
ready to start consuming query after 15 ms, results consumed after another 0 ms
Created 3 relationships, Set 6 properties
0 rows
ready to start consuming query after 12 ms, results consumed after another 0 ms
Created 4 relationships, Set 8 properties
0 rows
ready to start consuming query after 16 ms, results consumed after another 0 ms
Created 3 relationships, Set 6 properties
0 rows
ready to start consuming query after 16 ms, results consumed after another 0 ms
Created 3 relationships, Set 6 properties
0 rows
ready to start consuming query after 54 ms, results consumed after another 0 ms
Created 3 relationships, Set 6 properties
0 rows
ready to start consuming query after 56 ms, results consumed after another 0 ms
Created 3 relationships, Set 6 properties
0 rows
ready to start consuming query after 44 ms, results consumed after another 0 ms
Created 3 relationships, Set 6 properties
0 rows
ready to start consuming query after 14 ms, results consumed after another 0 ms
Created 3 relationships, Set 6 properties
0 rows
ready to start consuming query after 15 ms, results consumed after another 0 ms
Created 3 relationships, Set 6 properties
0 rows
ready to start consuming query after 12 ms, results consumed after another 0 ms
Created 3 relationships, Set 6 properties
0 rows
ready to start consuming query after 56 ms, results consumed after another 0 ms
Created 3 relationships, Set 6 properties
0 rows
ready to start consuming query after 11 ms, results consumed after another 0 ms
Created 3 relationships, Set 6 properties
0 rows
ready to start consuming query after 15 ms, results consumed after another 0 ms
Created 3 relationships, Set 6 properties
0 rows
ready to start consuming query after 19 ms, results consumed after another 0 ms
Created 3 relationships, Set 6 properties
0 rows
ready to start consuming query after 15 ms, results consumed after another 0 ms
Created 3 relationships, Set 6 properties
0 rows
ready to start consuming query after 50 ms, results consumed after another 0 ms
Created 3 relationships, Set 6 properties
0 rows
ready to start consuming query after 11 ms, results consumed after another 0 ms
Created 3 relationships, Set 6 properties
0 rows
ready to start consuming query after 13 ms, results consumed after another 0 ms
Created 3 relationships, Set 6 properties
0 rows
ready to start consuming query after 16 ms, results consumed after another 0 ms
Created 3 relationships, Set 6 properties
0 rows
ready to start consuming query after 15 ms, results consumed after another 0 ms
Created 3 relationships, Set 6 properties
0 rows
ready to start consuming query after 18 ms, results consumed after another 0 ms
Created 3 relationships, Set 6 properties
0 rows
ready to start consuming query after 16 ms, results consumed after another 0 ms
Created 3 relationships, Set 6 properties
0 rows
ready to start consuming query after 14 ms, results consumed after another 0 ms
Created 3 relationships, Set 6 properties
0 rows
ready to start consuming query after 57 ms, results consumed after another 0 ms
Created 3 relationships, Set 6 properties
0 rows
ready to start consuming query after 45 ms, results consumed after another 0 ms
Created 3 relationships, Set 6 properties
0 rows
ready to start consuming query after 10 ms, results consumed after another 0 ms
Created 3 relationships, Set 6 properties
0 rows
ready to start consuming query after 14 ms, results consumed after another 0 ms
Created 3 relationships, Set 6 properties
0 rows
ready to start consuming query after 11 ms, results consumed after another 0 ms
Created 3 relationships, Set 6 properties
0 rows
ready to start consuming query after 14 ms, results consumed after another 0 ms
Created 3 relationships, Set 6 properties
```


5. Relaciones CURSA por alumnos

```
>....                                                                                                                                                                                               CREATE (A1)-[:CURSA{ans: 2019, semestre: 1, cursando: false, grupo: 2,  calificacion: 10}]->(AdD);
             MATCH (A1: Alumno { apellido: "Cauchy"}), (PdI: Materia { codigo: "PdI"} ) 
             CREATE (A1)-[:CURSA{ans: 2020, semestre: 1, cursando: false, grupo: 2,  calificacion: 10}]->(PdI);
             
             
             // Fresnel
             
             MATCH (A1: Alumno { apellido: "Fresnel"}), (DDA3: Materia { codigo: "DDA3"} ) 
             CREATE (A1)-[:CURSA{ans: 2018, semestre: 1, cursando: false, grupo: 1,  calificacion: 7}]->(DDA3);
             MATCH (A1: Alumno { apellido: "Fresnel"}), (PdI: Materia { codigo: "PdI"} ) 
             CREATE (A1)-[:CURSA{ans: 2019, semestre: 1, cursando: false, grupo: 1,  calificacion: 4}]->(PdI);
             MATCH (A1: Alumno { apellido: "Fresnel"}), (DDA1: Materia { codigo: "DDA1"} ) 
             CREATE (A1)-[:CURSA{ans: 2020, semestre: 1, cursando: false, grupo: 1,  calificacion: 7}]->(DDA1);
             MATCH (A1: Alumno { apellido: "Fresnel"}), (DDA2: Materia { codigo: "DDA2"} ) 
             CREATE (A1)-[:CURSA{ans: 2020, semestre: 1, cursando: false, grupo: 1,  calificacion: 7}]->(DDA2);
             MATCH (A1: Alumno { apellido: "Fresnel"}), (GdP: Materia { codigo: "GdP"} ) 
             CREATE (A1)-[:CURSA{ans: 2021, semestre: 1, cursando: true, grupo: 1,  calificacion: null}]->(GdP);
             
             
             // Coulomb
             
             MATCH (A1: Alumno { apellido: "de Coulomb"}), (AdD: Materia { codigo: "AdD"} ) 
             CREATE (A1)-[:CURSA{ans: 2016, semestre: 1, cursando: false, grupo: 1,  calificacion: 10}]->(AdD);
             
             
             // Foucault
             
             MATCH (A1: Alumno { apellido: "Foucault"}), (AdD: Materia { codigo: "AdD"} ) 
             CREATE (A1)-[:CURSA{ans: 2016, semestre: 1, cursando: false, grupo: 2,  calificacion: 10}]->(AdD);
             MATCH (A1: Alumno { apellido: "Foucault"}), (AdD: Materia { codigo: "AdD"} ) 
             CREATE (A1)-[:CURSA{ans: 2017, semestre: 1, cursando: false, grupo: 2,  calificacion: 10}]->(AdD);
             
             
             // Poisson
             
             MATCH (A1: Alumno { apellido: "Poisson"}), (DDA3: Materia { codigo: "DDA3"} ) 
             CREATE (A1)-[:CURSA{ans: 2018, semestre: 1, cursando: false, grupo: 1,  calificacion: 10}]->(DDA3);
             MATCH (A1: Alumno { apellido: "Poisson"}), (PdI: Materia { codigo: "PdI"} ) 
             CREATE (A1)-[:CURSA{ans: 2019, semestre: 1, cursando: false, grupo: 1,  calificacion: 10}]->(PdI);
             MATCH (A1: Alumno { apellido: "Poisson"}), (DDA1: Materia { codigo: "DDA1"} ) 
             CREATE (A1)-[:CURSA{ans: 2020, semestre: 1, cursando: false, grupo: 1,  calificacion: 10}]->(DDA1);
             MATCH (A1: Alumno { apellido: "Poisson"}), (GdP: Materia { codigo: "GdP"} ) 
             CREATE (A1)-[:CURSA{ans: 2021, semestre: 1, cursando: true, grupo: 1,  calificacion: null}]->(GdP);
             MATCH (A1: Alumno { apellido: "Poisson"}), (AdD: Materia { codigo: "AdD"} ) 
             CREATE (A1)-[:CURSA{ans: 2021, semestre: 1, cursando: true, grupo: 1,  calificacion: null}]->(AdD);
             
             
             // Triger
             
             MATCH (A1: Alumno { apellido: "Triger"}), (DDA3: Materia { codigo: "DDA3"} ) 
             CREATE (A1)-[:CURSA{ans: 2018, semestre: 1, cursando: false, grupo: 1,  calificacion: 7}]->(DDA3);
             MATCH (A1: Alumno { apellido: "Triger"}), (PdI: Materia { codigo: "PdI"} ) 
             CREATE (A1)-[:CURSA{ans: 2019, semestre: 1, cursando: false, grupo: 1,  calificacion: 7}]->(PdI);
             MATCH (A1: Alumno { apellido: "Triger"}), (DDA1: Materia { codigo: "DDA1"} ) 
             CREATE (A1)-[:CURSA{ans: 2020, semestre: 1, cursando: false, grupo: 1,  calificacion: 7}]->(DDA1);
             MATCH (A1: Alumno { apellido: "Triger"}), (GdP: Materia { codigo: "GdP"} ) 
             CREATE (A1)-[:CURSA{ans: 2021, semestre: 1, cursando: true, grupo: 1,  calificacion: null}]->(GdP);
             MATCH (A1: Alumno { apellido: "Triger"}), (AdD: Materia { codigo: "AdD"} ) 
             CREATE (A1)-[:CURSA{ans: 2021, semestre: 1, cursando: true, grupo: 1,  calificacion: null}]->(AdD);
0 rows
ready to start consuming query after 38 ms, results consumed after another 0 ms
Created 3 relationships, Set 15 properties
0 rows
ready to start consuming query after 42 ms, results consumed after another 0 ms
Created 3 relationships, Set 15 properties
0 rows
ready to start consuming query after 44 ms, results consumed after another 0 ms
Created 3 relationships, Set 15 properties
0 rows
ready to start consuming query after 43 ms, results consumed after another 0 ms
Created 3 relationships, Set 15 properties
0 rows
ready to start consuming query after 45 ms, results consumed after another 0 ms
Created 4 relationships, Set 20 properties
0 rows
ready to start consuming query after 7 ms, results consumed after another 0 ms
Created 3 relationships, Set 12 properties
0 rows
ready to start consuming query after 15 ms, results consumed after another 0 ms
Created 3 relationships, Set 15 properties
0 rows
ready to start consuming query after 13 ms, results consumed after another 0 ms
Created 3 relationships, Set 15 properties
0 rows
ready to start consuming query after 18 ms, results consumed after another 0 ms
Created 3 relationships, Set 15 properties
0 rows
ready to start consuming query after 11 ms, results consumed after another 0 ms
Created 4 relationships, Set 20 properties
0 rows
ready to start consuming query after 3 ms, results consumed after another 0 ms
Created 3 relationships, Set 12 properties
0 rows
ready to start consuming query after 14 ms, results consumed after another 0 ms
Created 3 relationships, Set 15 properties
0 rows
ready to start consuming query after 13 ms, results consumed after another 0 ms
Created 3 relationships, Set 15 properties
0 rows
ready to start consuming query after 11 ms, results consumed after another 0 ms
Created 3 relationships, Set 15 properties
0 rows
ready to start consuming query after 11 ms, results consumed after another 0 ms
Created 3 relationships, Set 15 properties
0 rows
ready to start consuming query after 12 ms, results consumed after another 0 ms
Created 4 relationships, Set 20 properties
0 rows
ready to start consuming query after 16 ms, results consumed after another 0 ms
Created 3 relationships, Set 12 properties
0 rows
ready to start consuming query after 11 ms, results consumed after another 0 ms
Created 3 relationships, Set 15 properties
0 rows
ready to start consuming query after 11 ms, results consumed after another 0 ms
Created 3 relationships, Set 15 properties
0 rows
ready to start consuming query after 11 ms, results consumed after another 0 ms
Created 3 relationships, Set 15 properties
0 rows
ready to start consuming query after 12 ms, results consumed after another 0 ms
Created 3 relationships, Set 15 properties
0 rows
ready to start consuming query after 13 ms, results consumed after another 0 ms
Created 3 relationships, Set 15 properties
0 rows
ready to start consuming query after 11 ms, results consumed after another 0 ms
Created 3 relationships, Set 15 properties
0 rows
ready to start consuming query after 51 ms, results consumed after another 0 ms
Created 3 relationships, Set 15 properties
0 rows
ready to start consuming query after 61 ms, results consumed after another 0 ms
Created 4 relationships, Set 16 properties
0 rows
ready to start consuming query after 9 ms, results consumed after another 0 ms
Created 3 relationships, Set 15 properties
0 rows
ready to start consuming query after 13 ms, results consumed after another 0 ms
Created 3 relationships, Set 15 properties
0 rows
ready to start consuming query after 13 ms, results consumed after another 0 ms
Created 3 relationships, Set 15 properties
0 rows
ready to start consuming query after 15 ms, results consumed after another 0 ms
Created 3 relationships, Set 15 properties
0 rows
ready to start consuming query after 19 ms, results consumed after another 0 ms
Created 3 relationships, Set 15 properties
0 rows
ready to start consuming query after 15 ms, results consumed after another 0 ms
Created 3 relationships, Set 15 properties
0 rows
ready to start consuming query after 19 ms, results consumed after another 0 ms
Created 4 relationships, Set 16 properties
0 rows
ready to start consuming query after 61 ms, results consumed after another 0 ms
Created 3 relationships, Set 12 properties
0 rows
ready to start consuming query after 10 ms, results consumed after another 0 ms
Created 3 relationships, Set 15 properties
0 rows
ready to start consuming query after 13 ms, results consumed after another 0 ms
Created 3 relationships, Set 15 properties
0 rows
ready to start consuming query after 10 ms, results consumed after another 0 ms
Created 3 relationships, Set 15 properties
0 rows
ready to start consuming query after 17 ms, results consumed after another 0 ms
Created 4 relationships, Set 16 properties
0 rows
ready to start consuming query after 14 ms, results consumed after another 0 ms
Created 3 relationships, Set 12 properties
```


6. Lista de relaciones CONOCE ordenados por persona 


```
neo4j@neo4j> // Lagrange
             
             MATCH(A1: Alumno { apellido: "Lagrange"}), (A2: Alumno { apellido: "Laplace"}) CREATE (A1)-[:CONOCE_A]->(A2);
             MATCH(A1: Alumno { apellido: "Lagrange"}), (A2: Alumno { apellido: "Ampere"}) CREATE (A1)-[:CONOCE_A]->(A2);
             
             MATCH(A1: Alumno { apellido: "Lagrange"}), (P1: Profesor { apellido: "Seguin"}) CREATE (A1)-[:CONOCE_A]->(P1);
             
             
             // Laplace 
             
             MATCH(A1: Alumno { apellido: "Laplace"}), (A2: Alumno { apellido: "Fresnel"}) CREATE (A1)-[:CONOCE_A]->(A2);
             MATCH(A1: Alumno { apellido: "Laplace"}), (A2: Alumno { apellido: "de Coulomb"}) CREATE (A1)-[:CONOCE_A]->(A2);
             
             MATCH(A1: Alumno { apellido: "Laplace"}), (P1: Profesor { apellido: "Tresca"}) CREATE (A1)-[:CONOCE_A]->(P1);
             
             
             // Ampere
             
             MATCH(A1: Alumno { apellido: "Ampere"}), (A2: Alumno { apellido: "Laplace"}) CREATE (A1)-[:CONOCE_A]->(A2);
             MATCH(A1: Alumno { apellido: "Ampere"}), (A2: Alumno { apellido: "Cauchy"}) CREATE (A1)-[:CONOCE_A]->(A2);
             
             MATCH(A1: Alumno { apellido: "Ampere"}),(P1: Profesor { apellido: "Poncelet"}) CREATE (A1)-[:CONOCE_A]->(P1);
             
             
             // Cauchy
             
             MATCH(A1: Alumno { apellido: "Cauchy"}), (A2: Alumno { apellido: "Fresnel"}) CREATE (A1)-[:CONOCE_A]->(A2);
             MATCH(A1: Alumno { apellido: "Cauchy"}), (A2: Alumno { apellido: "Lalande"}) CREATE (A1)-[:CONOCE_A]->(A2);
             
             MATCH(A1: Alumno { apellido: "Cauchy"}), (P1: Profesor { apellido: "Cuvier"}) CREATE (A1)-[:CONOCE_A]->(P1);
             
             
             // Fresnel
             
             MATCH(A1: Alumno { apellido: "Fresnel"}), (P1: Profesor { apellido: "Chasles"}) CREATE (A1)-[:CONOCE_A]->(P1);
             MATCH(A1: Alumno { apellido: "Fresnel"}), (P2: Profesor { apellido: "Lavoisier"}) CREATE (A1)-[:CONOCE_A]->(P2);
             
             
             // de Coulomb
             
             MATCH(A1: Alumno { apellido: "de Coulomb"}), (P1: Profesor { apellido: "Seguin"}) CREATE (A1)-[:CONOCE_A]->(P1);
             MATCH(A1: Alumno { apellido: "de Coulomb"}), (P2: Profesor { apellido: "Tresca"}) CREATE (A1)-[:CONOCE_A]->(P2);
             MATCH(A1: Alumno { apellido: "de Coulomb"}), (P3: Profesor { apellido: "Poncelet"}) CREATE (A1)-[:CONOCE_A]->(P3);
             
             
             // Lalande
             
             MATCH(A1: Alumno { apellido: "Lalande"}), (P1: Profesor { apellido: "Seguin"}) CREATE (A1)-[:CONOCE_A]->(P1);
             MATCH(A1: Alumno { apellido: "Lalande"}), (P2: Profesor { apellido: "Tresca"}) CREATE (A1)-[:CONOCE_A]->(P2);
             MATCH(A1: Alumno { apellido: "Lalande"}), (P3: Profesor { apellido: "Poncelet"}) CREATE (A1)-[:CONOCE_A]->(P3);
```

## Resultados

+ Modelo de datos


![modelo](https://github.com/nandroidj/gvd-neo4j/blob/main/res/data-model.png)


1. Listado de alumnos que cursaron la misma materia, pero en esta materia son de distintos grupos


+ Query

```
MATCH (a:Alumno)-[ac:CURSA]->()<-[bc:CURSA]-(b:Alumno)
WHERE ac.grupo <> bc.grupo
RETURN DISTINCT a.nombre, a.apellido, b.nombre, b.apellido;
```

+ Response

```
╒══════════════════╤════════════╤══════════════════╤════════════╕
│"a.nombre"        │"a.apellido"│"b.nombre"        │"b.apellido"│
╞══════════════════╪════════════╪══════════════════╪════════════╡
│"Pierre-Simon"    │"Laplace"   │"Joseph-Louis"    │"Lagrange"  │
├──────────────────┼────────────┼──────────────────┼────────────┤
│"Jacques"         │"Triger"    │"Joseph-Louis"    │"Lagrange"  │
├──────────────────┼────────────┼──────────────────┼────────────┤
│"Simeo Denis"    │"Poisson"   │"Joseph-Louis"    │"Lagrange"  │
├──────────────────┼────────────┼──────────────────┼────────────┤
│"Augustin-Jean"   │"Fresnel"   │"Joseph-Louis"    │"Lagrange"  │
├──────────────────┼────────────┼──────────────────┼────────────┤
│"Charles-Augustin"│"de Coulomb"│"Joseph-Louis"    │"Lagrange"  │
├──────────────────┼────────────┼──────────────────┼────────────┤
│"Andre-Marie"     │"Ampere"    │"Pierre-Simon"    │"Laplace"   │
├──────────────────┼────────────┼──────────────────┼────────────┤
│"Joseph-Louis"    │"Lagrange"  │"Pierre-Simon"    │"Laplace"   │
├──────────────────┼────────────┼──────────────────┼────────────┤
│"Augustin-Louis"  │"Cauchy"    │"Pierre-Simon"    │"Laplace"   │
├──────────────────┼────────────┼──────────────────┼────────────┤
│"Pierre-Simon"    │"Laplace"   │"Andre-Marie"     │"Ampere"    │
├──────────────────┼────────────┼──────────────────┼────────────┤
│"Jacques"         │"Triger"    │"Andre-Marie"     │"Ampere"    │
├──────────────────┼────────────┼──────────────────┼────────────┤
│"Simeon Denis"    │"Poisson"   │"Andre-Marie"     │"Ampere"    │
├──────────────────┼────────────┼──────────────────┼────────────┤
│"Augustin-Jean"   │"Fresnel"   │"Andre-Marie"     │"Ampere"    │
├──────────────────┼────────────┼──────────────────┼────────────┤
│"Charles-Augustin"│"de Coulomb"│"Andre-Marie"     │"Ampere"    │
├──────────────────┼────────────┼──────────────────┼────────────┤
│"Jacques"         │"Triger"    │"Augustin-Louis"  │"Cauchy"    │
├──────────────────┼────────────┼──────────────────┼────────────┤
│"Simeon Denis"    │"Poisson"   │"Augustin-Louis"  │"Cauchy"    │
├──────────────────┼────────────┼──────────────────┼────────────┤
│"Augustin-Jean"   │"Fresnel"   │"Augustin-Louis"  │"Cauchy"    │
├──────────────────┼────────────┼──────────────────┼────────────┤
│"Pierre-Simon"    │"Laplace"   │"Augustin-Louis"  │"Cauchy"    │
├──────────────────┼────────────┼──────────────────┼────────────┤
│"Charles-Augustin"│"de Coulomb"│"Augustin-Louis"  │"Cauchy"    │
├──────────────────┼────────────┼──────────────────┼────────────┤
│"Andre-Marie"     │"Ampere"    │"Augustin-Jean"   │"Fresnel"   │
├──────────────────┼────────────┼──────────────────┼────────────┤
│"Joseph-Louis"    │"Lagrange"  │"Augustin-Jean"   │"Fresnel"   │
├──────────────────┼────────────┼──────────────────┼────────────┤
│"Augustin-Louis"  │"Cauchy"    │"Augustin-Jean"   │"Fresnel"   │
├──────────────────┼────────────┼──────────────────┼────────────┤
│"Leon"            │"Foucault"  │"Charles-Augustin"│"de Coulomb"│
├──────────────────┼────────────┼──────────────────┼────────────┤
│"Augustin-Louis"  │"Cauchy"    │"Charles-Augustin"│"de Coulomb"│
├──────────────────┼────────────┼──────────────────┼────────────┤
│"Andre-Marie"     │"Ampere"    │"Charles-Augustin"│"de Coulomb"│
├──────────────────┼────────────┼──────────────────┼────────────┤
│"Joseph-Louis"    │"Lagrange"  │"Charles-Augustin"│"de Coulomb"│
├──────────────────┼────────────┼──────────────────┼────────────┤
│"Jacques"         │"Triger"    │"Leon"            │"Foucault"  │
├──────────────────┼────────────┼──────────────────┼────────────┤
│"Simeon Denis"    │"Poisson"   │"Leon"            │"Foucault"  │
├──────────────────┼────────────┼──────────────────┼────────────┤
│"Charles-Augustin"│"de Coulomb"│"Leon"            │"Foucault"  │
├──────────────────┼────────────┼──────────────────┼────────────┤
│"Leon"            │"Foucault"  │"Simeon Denis"    │"Poisson"   │
├──────────────────┼────────────┼──────────────────┼────────────┤
│"Augustin-Louis"  │"Cauchy"    │"Simeon Denis"    │"Poisson"   │
├──────────────────┼────────────┼──────────────────┼────────────┤
│"Andre-Marie"     │"Ampere"    │"Simeon Denis"    │"Poisson"   │
├──────────────────┼────────────┼──────────────────┼────────────┤
│"Joseph-Louis"    │"Lagrange"  │"Simeon Denis"    │"Poisson"   │
├──────────────────┼────────────┼──────────────────┼────────────┤
│"Leon"            │"Foucault"  │"Jacques"         │"Triger"    │
├──────────────────┼────────────┼──────────────────┼────────────┤
│"Augustin-Louis"  │"Cauchy"    │"Jacques"         │"Triger"    │
├──────────────────┼────────────┼──────────────────┼────────────┤
│"Andre-Marie"     │"Ampere"    │"Jacques"         │"Triger"    │
├──────────────────┼────────────┼──────────────────┼────────────┤
│"Joseph-Louis"    │"Lagrange"  │"Jacques"         │"Triger"    │
└──────────────────┴────────────┴──────────────────┴────────────┘
```


2. Listado de personas que dictaron mas de una materia

+ Query

```
MATCH (p:Profesor)-[d:DICTO]->()
WITH p, count(d) AS cnt
WHERE cnt > 1
RETURN p;
```

+ Response

```
╒═══════════════════════════════════════════════════════════════╕
│"p"                                                            │
╞═══════════════════════════════════════════════════════════════╡
│{"apellido":"Tresca","nombre":"Henri","dni":"00000012"}        │
├───────────────────────────────────────────────────────────────┤
│{"apellido":"Poncelet","nombre":"Jean-Victor","dni":"00000013"}│
├───────────────────────────────────────────────────────────────┤
│{"apellido":"Cuvie","nombre":"Georges","dni":"00000014"}      │
├───────────────────────────────────────────────────────────────┤
│{"apellido":"Chasles","nombre":"Michel","dni":"00000015"}      │
├───────────────────────────────────────────────────────────────┤
│{"apellido":"Lavoisier","nombre":"Antoine","dni":"00000016"}   │
├───────────────────────────────────────────────────────────────┤
│{"apellido":"Jamin","nombre":"Jules","dni":"00000017"}         │
├───────────────────────────────────────────────────────────────┤
│{"apellido":"Chatelier","nombre":"Louis Le","dni":"00000018"}  │
└───────────────────────────────────────────────────────────────┘
```


3. Calculo de mi promedio

+ Query

```
MATCH (p:Alumno)-[c:CURSA]->()
WHERE p.apellido = "Lagrange"
RETURN avg(c.calificacion);
```

+ Response

```
╒═════════════════════╕
│"avg(c.calificacion)"│
╞═════════════════════╡
│10.0                 │
└─────────────────────┘
```


4. Recomendacion de personas que cursaron juntas pero no se conocen

+ Query

```
MATCH (a:Alumno)-[ac:CURSA]->()<-[bc:CURSA]-(b:Alumno)
WHERE ac.ans = bc.ans
AND ac.semestre = bc.semestre
AND NOT (a)-[:CONOCE_A]-(b)
RETURN DISTINCT a.apellido, b.apellido;
```

+ Response

```
╒════════════╤════════════╕
│"a.apellido"│"b.apellido"│
╞════════════╪════════════╡
│"Lagrange"  │"Lagrange"  │
├────────────┼────────────┤
│"Laplace"   │"Laplace"   │
├────────────┼────────────┤
│"Poisson"   │"Fresnel"   │
├────────────┼────────────┤
│"Triger"    │"Fresnel"   │
├────────────┼────────────┤
│"Foucault"  │"de Coulomb"│
├────────────┼────────────┤
│"de Coulomb"│"Foucault"  │
├────────────┼────────────┤
│"Triger"    │"Poisson"   │
├────────────┼────────────┤
│"Fesnel"    │"Poisson"   │
├────────────┼────────────┤
│"Poisson"   │"Triger"    │
├────────────┼────────────┤
│"Fresnel"   │"Triger"    │
└────────────┴────────────┘
```


5. Conocidos de mis conocidos hasta longitud 2

+ Query

```
MATCH (a:Profesor)-[s:CONOCE_A*..2]->(b)
WHERE a.apellido = "Laplace"
RETURN DISTINCT a,b;
```

+ Response

```

```


6. Alumnos que también son docentes (dictaron y cursaron materias)


+ Query

```
MATCH (p:Profesor)-[d:DICTO]->()
WITH p, count(d) AS cntd
WHERE cntd > 0
MATCH (p)-[c:CURSA]->()
WITH p, count(c) AS cntc
WHERE cntc > 0
RETURN p;
```

+ Response

```

```

7.  Dado un alumno en particular, se quiere obtener el listado de materias electivas que no haya cursado, en base al criterio de haber sido cursadas por otros alumnos que cursaron por lo menos una en comun con el:


+ Query

```
MATCH (a:Alumno)-[ac:CURSA]-(am:Materia), (b:Alumno)-[bc:CURSA]-(bm:Materia)
WHERE a.apellido = "Cauchy"
AND NOT EXISTS ((a:Alumno)-[:CURSA]-(bm:Materia))
AND ac.semestre = bc.semestre
AND bm.electiva = true
RETURN bm.nombre;
```

+ Response

```
╒══════════════════════════════╕
│"bm.nombre"                   │
╞══════════════════════════════╡
│"Desarrollo de Aplicaciones 2"│
├──────────────────────────────┤
│"Desarrollo de Aplicaciones 2"│
├──────────────────────────────┤
│"Desarrollo de Aplicaciones 2"│
├──────────────────────────────┤
│"Desarrollo de Aplicaciones 2"│
├──────────────────────────────┤
│"Desarrollo de Aplicaciones 2"│
├──────────────────────────────┤
│"Desarrollo de Aplicaciones 2"│
├──────────────────────────────┤
│"Desarrollo de Aplicaciones 2"│
├──────────────────────────────┤
│"Desarrollo de Aplicaciones 2"│
├──────────────────────────────┤
│"Desarrollo de Aplicaciones 2"│
├──────────────────────────────┤
│"Desarrollo de Aplicaciones 2"│
├──────────────────────────────┤
│"Desarrollo de Aplicaciones 2"│
├──────────────────────────────┤
│"Desarrollo de Aplicaciones 2"│
├──────────────────────────────┤
│"Desarrollo de Aplicaciones 2"│
├──────────────────────────────┤
│"Desarrollo de Aplicaciones 2"│
├──────────────────────────────┤
│"Desarrollo de Aplicaciones 2"│
├──────────────────────────────┤
│"Desarrollo de Aplicaciones 2"│
├──────────────────────────────┤
│"Desarrollo de Aplicaciones 2"│
├──────────────────────────────┤
│"Desarrollo de Aplicaciones 2"│
├──────────────────────────────┤
│"Desarrollo de Aplicaciones 2"│
├──────────────────────────────┤
│"Desarrollo de Aplicaciones 2"│
├──────────────────────────────┤
│"Desarrollo de Aplicaciones 2"│
├──────────────────────────────┤
│"Desarrollo de Aplicaciones 2"│
├──────────────────────────────┤
│"Desarrollo de Aplicaciones 2"│
├──────────────────────────────┤
│"Desarrollo de Aplicaciones 2"│
├──────────────────────────────┤
│"Desarrollo de Aplicaciones 2"│
├──────────────────────────────┤
│"Desarrollo de Aplicaciones 2"│
├──────────────────────────────┤
│"Desarrollo de Aplicaciones 2"│
└──────────────────────────────┘
```


8. Variante

+ Query

```
MATCH (a:Alumno)-[ac:CURSA]-(am:Materia), (b:Alumno)-[bc:CURSA]-(bm:Materia)
WHERE a.apellido = "Ampere"
AND NOT EXISTS ((a:Alumno)-[:CURSA]-(bm:Materia))
AND ac.semestre = bc.semestre
AND bm.electiva = true
AND EXISTS ((a:Alumno)-[:CONOCE_A*..]-(b:Alumno))
RETURN DISTINCT bm.nombre;
```

+ Response

```
╒══════════════════════════════╕
│"bm.nombre"                   │
╞══════════════════════════════╡
│"Desarrollo de Aplicaciones 2"│
└──────────────────────────────┘
```


9. Query final


+ Query

```
MATCH (p:Alumno)-[c:CURSA]-(m:Materia) 
WHERE NOT EXISTS (c.calificacion)
RETURN p.apellido, m.nombre, c.anio, c.semestre
```

+ Response

```
╒════════════╤═════════════════════════════╤═══════╤════════════╕
│"p.apellido"│"m.nombre"                   │"c.ans"│"c.semestre"│
╞════════════╪═════════════════════════════╪═══════╪════════════╡
│"Lagrange"  │"Arquitectura de protocoloes"│2021   │1           │
├────────────┼─────────────────────────────┼───────┼────────────┤
│"Lagrange"  │"Arquitectura de protocoloes"│2021   │1           │
├────────────┼─────────────────────────────┼───────┼────────────┤
│Lagrange"  │"Arquitectura de protocoloes"│2021   │1           │
├────────────┼─────────────────────────────┼───────┼────────────┤
│"Lagrange"  │"Arquitectura de protocoloes"│2021   │1           │
├────────────┼─────────────────────────────┼───────┼────────────┤
│"Lagrange"  │"Arquitectura de protocoloes"│2021   │1           │
├────────────┼─────────────────────────────┼───────┼────────────┤
│"Lagrange"  │"Arquitectura de protocoloes"│2021   │1           │
├────────────┼─────────────────────────────┼───────┼────────────┤
│"Laplace"   │"Arquitectura de protocoloes"│2021   │1           │
├────────────┼─────────────────────────────┼───────┼────────────┤
│"Laplace"   │"Arquitectura de protocoloes"│2021   │1           │
├────────────┼─────────────────────────────┼───────┼────────────┤
│"Laplace"   │"Arquitectura de protocoloes"│2021   │1           │
├────────────┼─────────────────────────────┼───────┼────────────┤
│"Laplace"   │"Arquitectura de protocoloes"│2021   │1           │
├────────────┼─────────────────────────────┼───────┼────────────┤
│"Laplace"   │"Arquitectura de protocoloes"│2021   │1           │
├────────────┼─────────────────────────────┼───────┼────────────┤
│"Laplace"   │"Arquitectura de protocoloes"│2021   │1           │
├────────────┼─────────────────────────────┼───────┼────────────┤
│"Ampere"    │"Arquitectura de protocoloes"│2021   │1           │
├────────────┼─────────────────────────────┼───────┼────────────┤
│"Ampere"    │"Arquitectura de protocoloes"│2021   │1           │
├────────────┼─────────────────────────────┼───────┼────────────┤
│"Ampere"    │"Arquitectura de protocoloes"│2021   │1           │
├────────────┼─────────────────────────────┼───────┼────────────┤
│"Fresnel"   │"Gestion de Proyectos"       │2021   │1           │
├────────────┼─────────────────────────────┼───────┼────────────┤
│"Fresnel"   │"Gestion de Proyectos"       │2021   │1           │
├────────────┼─────────────────────────────┼───────┼────────────┤
│"Fresnel"   │"Gestion de Proyectos"       │2021   │1           │
├────────────┼─────────────────────────────┼───────┼────────────┤
│"Fresnel"   │"Gestion de Proyectos"       │2021   │1           │
├────────────┼─────────────────────────────┼───────┼────────────┤
│"Poisson"   │"Arquitectura de datos"      │2021   │1           │
├────────────┼─────────────────────────────┼───────┼────────────┤
│"Poisson"   │"Arquitectura de datos"      │2021   │1           │
├────────────┼─────────────────────────────┼───────┼────────────┤
│"Poisson"   │"Arquitectura de datos"      │2021   │1           │
├────────────┼─────────────────────────────┼───────┼────────────┤
│"Poisson"   │"Gestion de Proyectos"       │2021   │1           │
├────────────┼─────────────────────────────┼───────┼────────────┤
│"Poisson"   │"Gestion de Proyectos"       │2021   │1           │
├────────────┼─────────────────────────────┼───────┼────────────┤
│"Poisson"   │"Gestion de Proyectos"       │2021   │1           │
├────────────┼─────────────────────────────┼───────┼────────────┤
│"Poisson"   │"Gestion de Proyectos"       │2021   │1           │
├────────────┼─────────────────────────────┼───────┼────────────┤
│"Triger"    │"Arquitectura de datos"      │2021   │1           │
├────────────┼─────────────────────────────┼───────┼────────────┤
│"Triger"    │"Arquitectura de datos"      │2021   │1           │
├────────────┼─────────────────────────────┼───────┼────────────┤
│"Triger"    │"Arquitectura de datos"      │2021   │1           │
├────────────┼─────────────────────────────┼───────┼────────────┤
│"Triger"    │"Gestion de Proyectos"       │2021   │1           │
├────────────┼─────────────────────────────┼───────┼────────────┤
│"Triger"    │"Gestion de Proyectos"       │2021   │1           │
├────────────┼─────────────────────────────┼───────┼────────────┤
│"Triger"    │"Gestion de Proyectos"       │2021   │1           │
├────────────┼─────────────────────────────┼───────┼────────────┤
│"Triger"    │"Gestion de Proyectos"       │2021   │1           │
└────────────┴─────────────────────────────┴───────┴────────────┘
```
















