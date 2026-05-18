# 🇬🇧 Data Analysis for the "Alfabetiza Sergipe" 2025 Program (Programa Brasil Alfabetizado in the State of Sergipe) — SEDUC/SE & FGV DGPE

This repository centralizes the data analysis codes and workflows developed by me and validated by the **Fundação Getulio Vargas (FGV DGPE)** team responsible for implementing the PBA SE 2025. This project was carried out in compliance with the contractual milestones established with the **State Secretariat of Education of Sergipe (SEDUC-SE)** for the pedagogical and statistical monitoring of the literacy program's classes (PBA 2025).

The primary objective of this analysis suite is to process the educational data generated during the program's execution to produce the official technical reports designated in the contract between FGV DGPE and the State Secretariat of Education of Sergipe (SEDUC SE).

---

## 🔒 Data Governance and Compliance (LGPD)

In strict compliance with the Brazilian **General Data Protection Law (LGPD - Law No. 13,709/2018)** and institutional compliance guidelines, **no Personally Identifiable Information (PII)** is exposed in this public repository.

* All textual data (Names of students, literacy teachers, and coordinators) and numerical records (CPFs and Phone Numbers) have been replaced with fictitious equivalents generated deterministically using the `Faker` library.
* Referential integrity and data crossovers between different notebooks have been fully preserved through a local persistent mapping architecture.
* Macro-level spatial data (**Neighborhoods** and **Full Addresses**) have also been replaced with fictitious equivalents generated deterministically via `Faker`.
* The anonymization pipeline utilized in this project is documented in the `protect_sensitive_data.ipynb` file.

---

## 📐 Analysis File Structure (.ipynb)

The analysis notebooks are systematically organized using prefixes that identify the specific group of classes evaluated, followed by the type of assessment activity in the pedagogical cycle.

### 🧩 Understanding the Prefix Nomenclature

1.  **`SE_` (Regular Classes):** Reports concerning the main group of classes that started their activities according to the regularly planned schedule.
2.  **`SE35_` (Late-Starting Classes):** Exclusive analyses for the 35 classes that started their cycle late. Due to methodological and scheduling differences, they required separate monitoring and reporting.
3.  **`SE_aditivo_` (Contract Addendum):** Reports focusing on the 30 additional classes integrated into the program under the contractual addendum signed between FGV DGPE and SEDUC-SE.

### 📑 Mapping Notebooks by Pedagogical Evaluation Cycle

| Jupyter Notebook File | Group Scope | Pedagogical Evaluation Cycle |
| :--- | :--- | :--- |
| `SE_Diagnostica.ipynb` | Regular Classes | Diagnostic Evaluation (Baseline/Entry) |
| `SE_Relatorio_2.1.1.ipynb` | Regular Classes | Formative Activity 1 |
| `SE_Relatorio_2.2.1.ipynb` | Regular Classes | Formative Activity 2 |
| `SE_Relatorio_2.3.2.ipynb` | Regular Classes | Formative Activity 3 |
| `SE_Relatorio_2.4.2.ipynb` | Regular Classes | Formative Activity 4 |
| `SE_Somativa.ipynb` | Regular Classes | Summative Evaluation (Endline/Final) |
| `SE_Somativa_348_turmas.ipynb` | Regular Classes | Final Consolidation of the 348 Classes |
| | | |
| `SE35_Diagnostica.ipynb` | Late-Starting Classes | Diagnostic Evaluation (Baseline/Entry) |
| `SE35_Relatorio_2.1.1.ipynb` | Late-Starting Classes | Formative Activity 1 |
| `SE35_Relatorio_2.2.1.ipynb` | Late-Starting Classes | Formative Activity 2 |
| `SE35_Relatorio_2.3.1.ipynb` | Late-Starting Classes | Formative Activity 3 |
| `SE35_Relatorio_2.4.2.ipynb` | Late-Starting Classes | Formative Activity 4 |
| `SE35_Relatorio_Somativa.ipynb` | Late-Starting Classes | Summative Evaluation (Endline/Final) |
| | | |
| `SE_aditivo_Diagnostica.ipynb` | Addendum (+30 Classes) | Diagnostic Evaluation (Baseline/Entry) |
| `SE_aditivo_Relatorio_2.1.1.ipynb` | Addendum (+30 Classes) | Formative Activity 1 |
| `SE_aditivo_Relatorio_2.2.ipynb` | Addendum (+30 Classes) | Formative Activity 2 |
| `SE_aditivo_Relatorio_2.3.ipynb` | Addendum (+30 Classes) | Formative Activity 3 |
| `SE_aditivo_Relatorio_2.3_extra.ipynb`| Addendum (+30 Classes) | Complementary Formative Analysis 3 |
| `SE_aditivo_Relatorio_Somativa.ipynb` | Addendum (+30 Classes) | Summative Evaluation (Endline/Final) |

### 🛠️ Auxiliary and Infrastructure Notebooks
* `Analise_especialistas.ipynb`: Analysis requested by the Pedagogical department of FGV DGPE to evaluate and understand the program's outcomes (still under construction).
* `protect_sensitive_data.ipynb`: Script responsible for masking, PII sanitization, and the controlled generation of stable encryption/anonymization dictionaries.

---

## 💻 Tech Stack and Execution

The analyses were entirely developed using the **Python** programming language and its scientific data analysis ecosystem:

* **Data Manipulation and Cleaning:** `pandas`, `numpy`
* **Anonymization and Synthetic Sampling:** `faker`
* **Data Structure I/O:** `openpyxl`, `xlrd`

### 📂 Reproducibility and Data Download

Due to storage guidelines and **GitHub file size limit policies** for large datasets, the original and processed source files (`.xlsx`, `.csv`, among others) have been omitted from this repository's main file tree.

To reproduce all analyses, metrics, and charts present in the notebooks, the complete dataset package containing the public tables (fully anonymized with fictitious data) must be downloaded externally:

👉 **[Click here to download the anonymized data files](https://1drv.ms/f/c/835153c0338453fe/IgCEuAoJgzJUSLyY76mmSd24AQugqQweobBXIl4FdewfjiU?e=JGPQud)**

> 📥 **Storage Instructions:** After downloading, extract and place the files directly inside the local folder structure at `Data_files/public_data/` before launching Jupyter Notebook.

### 🚀 How to Run Locally

1. Clone the repository:
   ```bash
   git clone https://github.com/fabcmc/pba_se_2025.git
   ```
2. Install the required dependencies:
   ```bash
   pip install pandas numpy faker openpyxl jupyter
   ```
3. Ensure that you have placed the data downloaded in the previous step inside `Data_files/public_data/`.
4. Start the Jupyter server to browse the reports:
   ```bash
   jupyter notebook
   ```

> 📌 *Note: This repository reflects the technical commitment to methodological excellence, analytical rigor, and respect for data privacy guidelines in public administration, combining my own execution of the analyses with the specialized validation of the FGV DGPE team.*

---


# 🇧🇷 Análise de Dados do Programa "Alfabetiza Sergipe" em 2025 (Programa Brasil Alfabetizado realizado no estado de Sergipe) — SEDUC/SE & FGV DGPE

Este repositório centraliza os códigos e as análises de dados desenvolvidos por mim e validados pela equipe da **Fundação Getulio Vargas (FGV DGPE)** responsável pela aplicação do PBA SE 2025, em cumprimento às metas contratuais estabelecidas com a **Secretaria de Educação do Estado de Sergipe (SEDUC-SE)** para o monitoramento pedagógico e estatístico das turmas do programa de alfabetização (PBA 2025).

O objetivo principal desta suíte de análises é processar os dados educacionais gerados durante a aplicação do programa para gerar os relatórios técnicos oficiais designados em contrato entre a FGV DGPE e a Secretaria de Educação do Estado de Sergipe (SEDUC SE).

---

## 🔒 Governança de Dados e Conformidade (LGPD)

Em estrita conformidade com a **Lei Geral de Proteção de Dados (Lei nº 13.709/2018)** e com as regras de *compliance* institucional, **nenhum dado pessoal identificável (PII)** está exposto neste repositório público. 

* Todos os dados de texto (Nomes de alunos, alfabetizadores e coordenadores) e numéricos (CPFs e Telefones) foram substituídos por equivalentes fictícios gerados deterministicamente via `Faker`.
* A integridade referencial e os cruzamentos de dados entre diferentes notebooks foram integralmente preservados através de uma arquitetura de mapeamento persistente local.
* Os dados espaciais de nível macro (**Bairros** e **Endereço completo**) também foram substituídos por equivalentes fictícios gerados deterministicamente via `Faker`.
* O pipeline de anonimização utilizado está documentado no arquivo `protect_sensitive_data.ipynb`.

---

## 📐 Estrutura dos Arquivos de Análise (.ipynb)

Os notebooks de análise estão organizados sistematicamente através de prefixos que identificam o grupo de turmas avaliado, seguidos pelo tipo de atividade avaliativa do ciclo pedagógico.

### 🧩 Entendendo a Nomenclatura dos Prefixos

1.  **`SE_` (Turmas Regulares):** Relatórios referentes ao grupo principal de turmas que iniciaram as atividades dentro do cronograma regular planejado.
2.  **`SE35_` (Turmas Tardias):** Análises exclusivas das 35 turmas que iniciaram o ciclo de forma tardia e que, por questões metodológicas e de calendário, exigiram monitoramento e relatórios segregados.
3.  **`SE_aditivo_` (Aditivo Contratual):** Relatórios focados nas 30 turmas adicionadas ao programa por força de termo aditivo firmado entre a FGV DGPE e a SEDUC-SE.

### 📑 Mapeamento dos Notebooks por Ciclo de Avaliação

| Arquivo Jupyter Notebook | Escopo do Grupo | Ciclo de Avaliação Pedagógica |
| :--- | :--- | :--- |
| `SE_Diagnostica.ipynb` | Turmas Regulares | Avaliação Diagnóstica (Entrada) |
| `SE_Relatorio_2.1.1.ipynb` | Turmas Regulares | Atividade Formativa 1 |
| `SE_Relatorio_2.2.1.ipynb` | Turmas Regulares | Atividade Formativa 2 |
| `SE_Relatorio_2.3.2.ipynb` | Turmas Regulares | Atividade Formativa 3 |
| `SE_Relatorio_2.4.2.ipynb` | Turmas Regulares | Atividade Formativa 4 |
| `SE_Somativa.ipynb` | Turmas Regulares | Avaliação Somativa (Final) |
| `SE_Somativa_348_turmas.ipynb` | Turmas Regulares | Consolidação Final das 348 Turmas |
| | | |
| `SE35_Diagnostica.ipynb` | Turmas Tardias | Avaliação Diagnóstica (Entrada) |
| `SE35_Relatorio_2.1.1.ipynb` | Turmas Tardias | Atividade Formativa 1 |
| `SE35_Relatorio_2.2.1.ipynb` | Turmas Tardias | Atividade Formativa 2 |
| `SE35_Relatorio_2.3.1.ipynb` | Turmas Tardias | Atividade Formativa 3 |
| `SE35_Relatorio_2.4.2.ipynb` | Turmas Tardias | Atividade Formativa 4 |
| `SE35_Relatorio_Somativa.ipynb` | Turmas Tardias | Avaliação Somativa (Final) |
| | | |
| `SE_aditivo_Diagnostica.ipynb` | Aditivo (+30 Turmas) | Avaliação Diagnóstica (Entrada) |
| `SE_aditivo_Relatorio_2.1.1.ipynb` | Aditivo (+30 Turmas) | Atividade Formativa 1 |
| `SE_aditivo_Relatorio_2.2.ipynb` | Aditivo (+30 Turmas) | Atividade Formativa 2 |
| `SE_aditivo_Relatorio_2.3.ipynb` | Aditivo (+30 Turmas) | Atividade Formativa 3 |
| `SE_aditivo_Relatorio_2.3_extra.ipynb`| Aditivo (+30 Turmas) | Análise Complementar Formativa 3 |
| `SE_aditivo_Relatorio_Somativa.ipynb` | Aditivo (+30 Turmas) | Avaliação Somativa (Final) |

### 🛠️ Notebooks Auxiliares e de Infraestrutura
* `Analise_especialistas.ipynb`: Análise solicitada pelo setor Pedagógico da FGV DGPE com o objetivo de entender resultados do programa (ainda em contrução).
* `protect_sensitive_data.ipynb`: Script responsável pelo mascaramento, sanitização de PII e geração controlada de dicionários estáveis de criptografia/anonimização.

---

## 💻 Stack Tecnológica e Execução

As análises foram integralmente desenvolvidas utilizando a linguagem **Python** e o ecossistema científico de análise de dados:

* **Manipulação e Limpeza de Dados:** `pandas`, `numpy`
* **Anonimização e Amostragem Sintética:** `faker`
* **Leitura e Escrita de Estruturas:** `openpyxl`, `xlrd`

### 📂 Reprodutibilidade e Download dos Dados

Devido às diretrizes de armazenamento e **políticas de limite de espaço do GitHub** para grandes volumes de dados, os arquivos originais e tratados (`.xlsx`, `.csv`, dentre outros arquivos) não foram incluídos diretamente na árvore deste repositório.

Para fins de reprodutibilidade de todas as análises e gráficos presentes nos notebooks, o pacote completo contendo as tabelas públicas (já anonimizadas com dados fictícios) deve ser baixado externamente:

👉 **[Clique aqui para baixar os arquivos de dados anonimizados](https://1drv.ms/f/c/835153c0338453fe/IgCEuAoJgzJUSLyY76mmSd24AQugqQweobBXIl4FdewfjiU?e=JGPQud)**

> 📥 **Instrução de Armazenamento:** Após o download, extraia e insira os arquivos diretamente dentro da pasta de estrutura local `Data_files/public_data/` antes de inicializar o Jupyter Notebook.

### 🚀 Como Executar Localmente

1. Clone o repositório:
   ```bash
   git clone https://github.com/fabcmc/pba_se_2025.git
   ```
2. Instale as dependências requeridas:
   ```bash
   pip install pandas numpy faker openpyxl jupyter
   ```
3. Certifique-se de que inseriu os dados baixados no passo anterior em `Data_files/public_data/`.
4. Inicie o servidor do Jupyter para navegar pelos relatórios:
   ```bash
   jupyter notebook
   ```

> 📌 *Nota:Este repositório reflete o compromisso técnico com a excelência metodológica, rigor analítico e respeito às diretrizes de privacidade de dados na administração pública, combinando a execução própria das análises com a validação especializada da equipe da FGV DGPE.*