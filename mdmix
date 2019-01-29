#estos comandos se corren desde la carpeta raíz(por ejemplo, ETA_1, ETA_2, WAT_1, etc.)
#Primero hay que alinear la trayectoria
#-C5 indica el número de procesadores a usar, usar el máximo número disponible
#--mask indica los residuos que se usan como ancla para el alineamiento y estas regiones dependen de cada especie. En este caso se tiene la máscara para S. aureus.
#byname -s ETA_1 ETA_2 indica que se hará el alineamiento en ambas carpetas
mdmix analyze align byname -s ETA_1 ETA_2 -C5 --mask 780-800,2163-2174,2715-2759,3179-3190

#Cálculo de densidades
mdmix analyze density byname -s ETA_1 ETA_2 -C6

#Cálculo de Energa
mdmix analyze energy byname -s ETA_1 ETA_2

#Cálculo de Hotspots con corte automático
mdmix analyze hotspots create -i PROBE_AVG/ETA_CT_DG0.dx PROBE_AVG/ETA_OH_DG0.dx PROBE_AVG/ETA_WAT_DG.dx -o ETA_allprobes_hotspots

#Cálculo de Hotspots con corte manual
#--hardcutoff indica el nivel energético del corte. El máximo es -1.5 kcal/mol
mdmix analyze hotspots create -i PROBE_AVG/ETA_CT_DG0.dx PROBE_AVG/ETA_OH_DG0.dx PROBE_AVG/ETA_WAT_DG.dx --hardcutoff -0.8 -o ETA_allprobes_hotspots_minus08
