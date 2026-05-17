# Análise de Dados do Programa "Alfabetiza Sergipe" em 2025 (Programa Brasil Alfabetizado realizado no estado de Sergipe) — SEDUC/SE & FGV DGPE

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

👉 **[Clique aqui para baixar os arquivos de dados anonimizados](COLE_AQUI_O_LINK_DO_SEU_DRIVE_OU_NUVEM)**

> 📥 **Instrução de Armazenamento:** Após o download, extraia e insira os arquivos diretamente dentro da pasta de estrutura local `Data_files/public_data/` antes de inicializar o Jupyter Notebook.

### 🚀 Como Executar Localmente

1. Clone o repositório:
   ```bash
   git clone [https://github.com/seu-usuario/seu-repositorio.git](https://github.com/seu-usuario/seu-repositorio.git)
