# GBI6_ExamenPython
## Aquí se resolverán los ejercicios del Examen 
# Ejercicio 1 [2 puntos] Jairo utilizo estos códigos
## Se usaron los siguientes códigos 
# Escriba aquí su código para el ejercicio 1
import miningscience as msc
data = msc.download_pubmed("Zika")
print("Este es el resultado", data)
msc.map_science("sequence.seq")
# Ejercicio 2 [2 puntos] Jairo utilizo estos códigos
## Se usaron los siguientes códigos
import os
import re
palabra1 = msc.download_pubmed("Zika")
print ('El número artículos para KEYWORD es: ',len (palabra1))
with open ("Data/Resultados 01.txt","w") as txt:
    txt.write(palabra1)
palabra2 = msc.download_pubmed("vitamins")
print ('El número artículos para KEYWORD es: ', len (palabra2))
with open ("Data/Resultados 02.txt","w") as txt:
    txt.write(palabra2)
# Ejercicio 3 Jairo utilizo estos códigos
## Estos son los código que en principio deben dar las gráficas pero no pude encuentrar el error 
msc.mapscience(palabra1)
msc.mapscience(palabra2)
# Ejercicio 4 Jairo utilizo estos códigos
------------------------------------------------------------------------------------------
# Ejercicio 5 Jairo utilizo estos códigos
## Se usaron lso siguientes códigos 
# Escriba aquí su código para el ejercicio 6
#PUDE LLEGAS SOLO HASTA EL CUARTO PASO
from Bio import Phylo
from Bio import SeqIO
from Bio import AlignIO
from Bio.Phylo.TreeConstruction import DistanceCalculator
from Bio.Phylo.TreeConstruction import DistanceTreeConstructor
from Bio import Entrez
from Bio import SeqIO
from Bio import GenBank 
import csv 
import re 
from Bio.Align.Applications import ClustalwCommandline
import os

# Secuencia simple fasta 
with open("data/sequence.seq", errors="ignore") as file: 
    texto_1 = file.read()
accession = texto_1.split("\n")
Entrez.email="jairo.calapucha@est.ikiam.edu.ec"
archivo = open("data/sequence.fasta", "w")
for i in accession[0:15]: 
    handle=Entrez.efetch(db="nuccore", id=i, rettype="fasta")
    archivo.write(handle.read())
