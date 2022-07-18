

// Lista de materias
CREATE ( GdP: Materia { nombre: 'Gestion de Proyectos', codigo: 'GdP', electiva: false });
CREATE ( PdI: Materia { nombre: 'Protocolos de Internet', codigo: 'PdI', electiva: false });
CREATE ( DDA1: Materia { nombre: 'Desarrollo de Aplicaciones 1', codigo: 'DDA1', electiva: false });
CREATE ( AdD: Materia { nombre: 'Arquitectura de datos', codigo: 'AdD', electiva: true });
CREATE ( AdP: Materia { nombre: 'Arquitectura de protocoloes', codigo: 'AdP', electiva: false });
CREATE ( DDA2: Materia { nombre: 'Desarrollo de Aplicaciones 2', codigo: 'DDA2', electiva: true });
CREATE ( BD: Materia { nombre: 'Big Data', codigo: 'BD', electiva: false });
CREATE ( DDA3: Materia { nombre: 'Desarrollo de Aplicaciones 3', codigo: 'DDA3', electiva: false });


// Lista de alumnos
CREATE ( A1: Alumno { nombre: 'Joseph-Louis', apellido: 'Lagrange', dni: '00000001', esDocente: false });
CREATE ( A2: Alumno { nombre: 'Pierre-Simon', apellido: 'Laplace', dni: '00000002', esDocente: false });
CREATE ( A3: Alumno { nombre: 'Andre-Marie', apellido: 'Ampere', dni: '00000003', esDocente: false });
CREATE ( A4: Alumno { nombre: 'Augustin-Louis', apellido: 'Cauchy', dni: '00000004', esDocente: false });
CREATE ( A5: Alumno { nombre: 'Augustin-Jean', apellido: 'Fresnel', dni: '00000005', esDocente: false });
CREATE ( A6: Alumno { nombre: 'Charles-Augustin', apellido: 'de Coulomb', dni: '00000006', esDocente: true });
CREATE ( A7: Alumno { nombre: 'Leon', apellido: 'Foucault', dni: '00000007', esDocente: true });
CREATE ( A8: Alumno { nombre: 'Simeon Denis', apellido: 'Poisson', dni: '00000008', esDocente: false });
CREATE ( A9: Alumno { nombre: 'Jerome', apellido: 'Lalande', dni: '00000009', esDocente: false });
CREATE ( A10: Alumno { nombre: 'Jacques', apellido: 'Triger', dni: '00000010', esDocente: false });


// Lista de profesores
CREATE ( P1: Profesor { nombre: 'Marc', apellido: 'Seguin', dni: '00000011'});
CREATE ( P2: Profesor { nombre: 'Henri', apellido: 'Tresca', dni: '00000012'});
CREATE ( P3: Profesor { nombre: 'Jean-Victor', apellido: 'Poncelet', dni: '00000013'});
CREATE ( P4: Profesor { nombre: 'Georges', apellido: 'Cuvier', dni: '00000014'});
CREATE ( P5: Profesor { nombre: 'Michel', apellido: 'Chasles', dni: '00000015'});
CREATE ( P6: Profesor { nombre: 'Antoine', apellido: 'Lavoisier', dni: '00000016'});
CREATE ( P7: Profesor { nombre: 'Jules', apellido: 'Jamin', dni: '00000017'});
CREATE ( P8: Profesor { nombre: 'Louis Le', apellido: 'Chatelier', dni: '00000018'});


// Relaciones DICTO (docentes)

MATCH (P2: Profesor { apellido:"Chatelier"}), (AdD: Materia { codigo: "AdD"} ) CREATE (P2)-[:DICTO{ans: 2016, semestre: 1}]->(AdD);
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


// Relaciones CURSA ( agrupadas por alumnos)

// Lagrange

MATCH (A1: Alumno { apellido: "Lagrange"}), (DDA3: Materia { codigo: "DDA3"} ) 
CREATE (A1)-[:CURSA{ans: 2017, semestre: 1, cursando: false, grupo: 2,  calificacion: 10}]->(DDA3);
MATCH (A1: Alumno { apellido: "Lagrange"}), (AdD: Materia { codigo: "AdD"} ) 
CREATE (A1)-[:CURSA{ans: 2018, semestre: 1, cursando: false, grupo: 2,  calificacion: 10}]->(AdD);
MATCH (A1: Alumno { apellido: "Lagrange"}), (PdI: Materia { codigo: "PdI"} ) 
CREATE (A1)-[:CURSA{ans: 2018, semestre: 1, cursando: false, grupo: 2,  calificacion: 10}]->(PdI);
MATCH (A1: Alumno { apellido: "Lagrange"}), (DDA1: Materia { codigo: "DDA1"} ) 
CREATE (A1)-[:CURSA{ans: 2019, semestre: 1, cursando: false, grupo: 2,  calificacion: 10}]->(DDA1);
MATCH (A1: Alumno { apellido: "Lagrange"}), (GdP: Materia { codigo: "GdP"} ) 
CREATE (A1)-[:CURSA{ans: 2020, semestre: 1, cursando: false, grupo: 2,  calificacion: 10}]->(GdP);
MATCH (A1: Alumno { apellido: "Lagrange"}), (AdP: Materia { codigo: "AdP"} ) 
CREATE (A1)-[:CURSA{ans: 2021, semestre: 1, cursando: true, grupo: 2,  calificacion: null}]->(AdP);


// Laplace

MATCH (A1: Alumno { apellido: "Laplace"}), (DDA3: Materia { codigo: "DDA3"} ) 
CREATE (A1)-[:CURSA{ans: 2017, semestre: 1, cursando: false, grupo: 1,  calificacion: 7}]->(DDA3);
MATCH (A1: Alumno { apellido: "Laplace"}), (PdI: Materia { codigo: "PdI"} ) 
CREATE (A1)-[:CURSA{ans: 2018, semestre: 1, cursando: false, grupo: 1,  calificacion: 7}]->(PdI);
MATCH (A1: Alumno { apellido: "Laplace"}), (DDA1: Materia { codigo: "DDA1"} ) 
CREATE (A1)-[:CURSA{ans: 2019, semestre: 1, cursando: false, grupo: 1,  calificacion: 7}]->(DDA1);
MATCH (A1: Alumno { apellido: "Laplace"}), (GdP: Materia { codigo: "GdP"} ) 
CREATE (A1)-[:CURSA{ans: 2020, semestre: 1, cursando: false, grupo: 1,  calificacion: 7}]->(GdP);
MATCH (A1: Alumno { apellido: "Laplace"}), (AdP: Materia { codigo: "AdP"} ) 
CREATE (A1)-[:CURSA{ans: 2021, semestre: 1, cursando: true, grupo: 1,  calificacion: null}]->(AdP);


// Ampere

MATCH (A1: Alumno { apellido: "Ampere"}), (DDA3: Materia { codigo: "DDA3"} ) 
CREATE (A1)-[:CURSA{ans: 2017, semestre: 1, cursando: false, grupo: 2,  calificacion: 10}]->(DDA3);
MATCH (A1: Alumno { apellido: "Ampere"}), (AdD: Materia { codigo: "AdD"} ) 
CREATE (A1)-[:CURSA{ans: 2018, semestre: 1, cursando: false, grupo: 2,  calificacion: 10}]->(AdD);
MATCH (A1: Alumno { apellido: "Ampere"}), (PdI: Materia { codigo: "PdI"} ) 
CREATE (A1)-[:CURSA{ans: 2018, semestre: 1, cursando: false, grupo: 2,  calificacion: 10}]->(PdI);
MATCH (A1: Alumno { apellido: "Ampere"}), (DDA1: Materia { codigo: "DDA1"} ) 
CREATE (A1)-[:CURSA{ans: 2019, semestre: 1, cursando: false, grupo: 2,  calificacion: 10}]->(DDA1);
MATCH (A1: Alumno { apellido: "Ampere"}), (GdP: Materia { codigo: "GdP"} ) 
CREATE (A1)-[:CURSA{ans: 2020, semestre: 1, cursando: false, grupo: 2,  calificacion: 10}]->(GdP);
MATCH (A1: Alumno { apellido: "Ampere"}), (AdP: Materia { codigo: "AdP"} ) 
CREATE (A1)-[:CURSA{ans: 2021, semestre: 1, cursando: true, grupo: 2,  calificacion: null}]->(AdP);


// Cauchy

MATCH (A1: Alumno { apellido: "Cauchy"}), (DDA3: Materia { codigo: "DDA3"} ) 
CREATE (A1)-[:CURSA{ans: 2019, semestre: 1, cursando: false, grupo: 2,  calificacion: 10}]->(DDA3);
MATCH (A1: Alumno { apellido: "Cauchy"}), (AdD: Materia { codigo: "AdD"} ) 
CREATE (A1)-[:CURSA{ans: 2019, semestre: 1, cursando: false, grupo: 2,  calificacion: 10}]->(AdD);
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


// Lista de relaciones CONOCE ordenados por persona

// Lagrange

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



