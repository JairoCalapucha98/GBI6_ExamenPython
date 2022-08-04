# GBI6_ExamenPython
<img src="https://ecogenomics.github.io/CheckM/img/checkm.png" width=300 height=240 />
 <center><h2> INGENIERÍA EN BIOTECNOLOGÍA</h2></center>

<img src="https://www.ikiam.edu.ec/img/logo-ikiam-grey.png" width=400 height=300 />

# <center><h1 style="color:orange">GBI6 - BIOINFORMÁTICA</h1></center>

# <center><h1 style="color:orange">EXAMEN PARCIAL PYTHON</h1></center>

<center><h3>GBI6-2021II: BIOINFORMÁTICA<center><h3>

<center><h3>Apellidos, Nombres: Jairo Calapucha Alvarado<center><h3>

<center><h4>03-08-2022<center><h4>
## datos personales:

- Nombres y Apillidos: Jairo Livardo Calapucha Alvarado
- Sexo: Masculino
- Edad: 23 años
- Nacionalidad: Indígena
- Residencia: Tena 

## características de su computador:

| Características del computador | | |
| :- | -: | :-: |
| Nombre del dispositivo: | IKIAM365JC |
| Procesador: | Intel(R) Core(TM) i7-8550U CPU @ 1.80GHz   1.99 GHz |
| RAM instalada: | 8,00 GB|
| Identificador de dispositivo: | 12E25A8B-54F5-4DE5-BE4F-0E769C07FE17 |
| Id. del producto: | 00330-80000-00000-AA815 |
| Tipo de sistema	Sistema operativo: | 64 bits, procesador basado en x64 |
| Lápiz y entrada táctil: | La entrada táctil o manuscrita no está disponible para esta pantalla |
## Aquí se resolverán los ejercicios del Examen 
# Ejercicio 1 [2 puntos] Jairo utilizo estos códigos
## Se usaron los siguientes códigos 
# Escriba aquí su código para el ejercicio 1
- import miningscience as msc
- data = msc.download_pubmed("Zika")
- print("Este es el resultado", data)
- msc.map_science("sequence.seq")
# Ejercicio 2 [2 puntos] Jairo utilizo estos códigos
## Se usaron los siguientes códigos
- import os
- import re
- palabra1 = msc.download_pubmed("Zika")
- print ('El número artículos para KEYWORD es: ',len (palabra1))
- with open ("Data/Resultados 01.txt","w") as txt:
-    txt.write(palabra1)
- palabra2 = msc.download_pubmed("vitamins")
- print ('El número artículos para KEYWORD es: ', len (palabra2))
- with open ("Data/Resultados 02.txt","w") as txt:
-    txt.write(palabra2)
# Ejercicio 3 Jairo utilizo estos códigos
## Estos son los código que en principio deben dar las gráficas pero no pude encuentrar el error 
- msc.mapscience(palabra1)
- msc.mapscience(palabra2)
# Ejercicio 4 Jairo utilizo estos códigos
------------------------------------------------------------------------------------------
# Ejercicio 5 Jairo utilizo estos códigos
## Se usaron lso siguientes códigos 
#PUDE LLEGAr SOLO HASTA EL CUARTO PASO
- from Bio import Phylo
- from Bio import SeqIO
- from Bio import AlignIO
- from Bio.Phylo.TreeConstruction import DistanceCalculator
- from Bio.Phylo.TreeConstruction import DistanceTreeConstructor
- from Bio import Entrez
- from Bio import SeqIO
- from Bio import GenBank 
- import csv 
- import re 
- from Bio.Align.Applications import ClustalwCommandline
- import os

# Secuencia simple fasta 
- with open("data/sequence.seq", errors="ignore") as file: 
-    texto_1 = file.read()
- accession = texto_1.split("\n")
- Entrez.email="jairo.calapucha@est.ikiam.edu.ec"
- archivo = open("data/sequence.fasta", "w")
- for i in accession[0:15]: 
-    handle=Entrez.efetch(db="nuccore", id=i, rettype="fasta")
-    archivo.write(handle.read())
