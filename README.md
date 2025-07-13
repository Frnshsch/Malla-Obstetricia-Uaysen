# 🧬 Malla Interactiva - Obstetricia

```mermaid
graph TD

%% Año 1 - I Semestre
A1[Fundamentos disciplinarios de la profesión] --> A7[Salud de la mujer y RN I]
A2[Química y bioquímica] --> A8[Biología celular y genética]
A2 --> A9[Fisiología general y de sistemas]
A3[Anatomía] --> A7
A3 --> A9
A4[Fundamentos socioculturales de la salud] --> B6[Educación para la salud e interculturalidad]
A5[Formación fundamental I] --> A6[Formación fundamental II]

%% Año 1 - II Semestre
A7 --> B1[Salud de la mujer y RN II]
A8 --> B2[Fisiopatología]
A8 --> B3[Inmunología y agentes vivos]
A9 --> B1
A9 --> B2
A9 --> B3
A10[Histología] --> B1
A6 --> B4[Formación fundamental III]

%% Año 2 - III Semestre
B1 --> C1[Salud de la mujer y RN III]
B2 --> C1
B2 --> C2[Farmacología]
B3 --> E1[Internado obstetricia I]
B3 --> E2[Internado obstetricia II]
B3 --> E3[Internado APS I]
B3 --> E4[Internado APS II]
B3 --> E5[Internado ginecología I]
B3 --> E6[Internado ginecología II]
B3 --> E7[Internado Neonatología I]
B3 --> E8[Internado Neonatología II]
B5[Psicología general y del desarrollo] --> E1
B5 --> E2
B5 --> E3
B5 --> E4
B5 --> E5
B5 --> E6
B5 --> E7
B5 --> E8
B6 --> E1
B6 --> E2
B6 --> E3
B6 --> E4
B6 --> E5
B6 --> E6
B6 --> E7
B6 --> E8
B7[Inglés I] --> C3[Inglés II]

%% Año 2 - IV Semestre
C1 --> D1[Clínica salud mujer y RN I]
C2 --> D1
C3 --> D2[Inglés III]
C4[Salud pública y epidemiología I] --> D3[Gestión y liderazgo I]
C4 --> D4[Salud pública y epidemiología II]

%% Año 3 - V Semestre
D1 --> E9[Salud de la mujer y RN IV]
D3 --> E10[Gestión y liderazgo II]
D4 --> E11[Investigación en salud I]
D2 --> E12[Inglés IV]

%% Año 3 - VI Semestre
E9 --> F1[Salud de la mujer y RN V]
E10 --> F2[Gestión y liderazgo III]
E11 --> F3[Investigación en salud II]

%% Año 4 - VII Semestre
F1 --> G1[Clínica salud mujer y RN III - Intrahospitalaria]
F1 --> G2[Clínica salud mujer y RN II - APS]
F2 --> G1
F2 --> G2
F2 --> G3[Formulación y evaluación de proyectos en salud]
F3 --> G3
G4[Bioética clínica] --> E1
G4 --> E2
G4 --> E3
G4 --> E4
G4 --> E5
G4 --> E6
G4 --> E7
G4 --> E8
B4 --> G5[Formación fundamental IV]

%% Año 4 - VIII Semestre
G2 --> E1
G2 --> E2
G2 --> E3
G2 --> E4
G2 --> E5
G2 --> E6
G2 --> E7
G2 --> E8
G1 --> E1
G1 --> E2
G1 --> E3
G1 --> E4
G1 --> E5
G1 --> E6
G1 --> E7
G1 --> E8
G3 --> E1
G3 --> E2
G3 --> E3
G3 --> E4
G3 --> E5
G3 --> E6
G3 --> E7
G3 --> E8

%% Año 5 - IX y X Semestres
E1 --> H1[Internado obstetricia II]
E3 --> H2[Internado APS II]
E5 --> H3[Internado ginecología II]
E7 --> H4[Internado Neonatología II]
