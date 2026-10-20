<!-- ============================================================ -->
<!--  Header                                                       -->
<!-- ============================================================ -->
<p align="center">
  <img width="100%" alt="Caio Leimig — Data Engineering"
       src="https://capsule-render.vercel.app/api?type=waving&height=220&color=0:0B1120,50:134E4A,100:14B8A6&text=Caio%20Leimig&fontColor=FFFFFF&fontSize=52&fontAlignY=36&desc=Data%20Engineering%20%E2%80%A2%20Ci%C3%AAncia%20da%20Computa%C3%A7%C3%A3o%20%40%20CESAR%20School&descSize=18&descAlignY=56&animation=fadeIn" />
</p>

<p align="center">
  <img alt="Engenharia de Dados · ELT · Modelagem"
       src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=500&size=19&duration=3500&pause=900&color=2DD4BF&center=true&vCenter=true&width=680&lines=Engenharia+de+Dados+%E2%80%94+pipelines%2C+ELT+e+modelagem;Python+%C2%B7+SQL+%C2%B7+AWS+%C2%B7+dbt;Do+dado+bruto+ao+dado+confi%C3%A1vel+e+consult%C3%A1vel" />
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/caio-leimig-rodrigues-da-silva/" target="_blank"><img alt="LinkedIn" src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" /></a>
  <a href="mailto:caiolrs2005@gmail.com"><img alt="Email" src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" /></a>
  <a href="https://github.com/caioleimig" target="_blank"><img alt="GitHub" src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white" /></a>
</p>

<br />

## Sobre

Estudante de Ciência da Computação na **CESAR School** (Recife, PE), construindo carreira em **Engenharia de Dados** e **Análise de Dados**. Meu interesse está no caminho que o dado percorre: da extração na fonte até virar uma tabela limpa, modelada e pronta para consulta. Gosto de pensar em ingestão, transformação, modelagem e qualidade — e de entregar isso como pipelines reprodutíveis, não como scripts soltos.

Hoje trabalho principalmente com **Python** e **SQL**, usando **AWS** (S3 + Athena) e **dbt** para montar fluxos ELT de ponta a ponta, sem deixar de lado a base de engenharia de software que vem da graduação.

```sql
-- models/marts/dim_developer.sql
SELECT
    'Caio Leimig'                                        AS nome,
    'Data Engineering'                                   AS role,
    'B.Sc. Ciência da Computação @ CESAR School'         AS formacao,
    'Recife, PE — Brasil'                                AS base,
    ARRAY['ELT pipelines', 'Modelagem de dados', 'SQL']  AS foco,
    ARRAY['dbt', 'AWS', 'Orquestração de pipelines']     AS aprendendo_agora
FROM {{ ref('stg_cesar_school__students') }}
WHERE curiosidade > 0
  AND cafe IS NOT NULL;
```

## Projeto em destaque — Global Music DNA

Pipeline **ELT diário** que coleta os charts do Apple Music em **30 países**, armazena o dado bruto em um data lake na AWS, transforma com dbt e expõe os resultados em um dashboard — construído de ponta a ponta como projeto de portfólio.

```mermaid
flowchart LR
    A["🎵 Apple Music<br/>Charts API"] -->|Python · extração diária| B[("☁️ AWS S3<br/>raw / landing")]
    B --> C["🔎 AWS Athena<br/>tabelas externas"]
    C -->|dbt · staging → marts| D[("📐 Modelos<br/>analíticos")]
    D --> E["📊 Streamlit<br/>dashboard"]
```

<sub>Decisão de projeto: a fonte original era a API do Spotify; após problemas de autenticação, migrei a ingestão para a API pública de charts do Apple Music sem alterar o restante do pipeline.</sub>

## Projetos

| Projeto | Visão geral |
| :-- | :-- |
| **Global Music DNA**<br /><sub>Python · AWS S3 · Athena · dbt · Streamlit</sub> | Pipeline ELT diário sobre os charts do Apple Music em 30 países: ingestão em Python, data lake no S3, consultas via Athena, transformações modeladas em dbt e visualização em Streamlit. |
| **Autocar BD**<br /><sub>Java · JavaFX · MySQL · JDBC</sub> | Sistema de gestão de locação de veículos, feito em trio para Modelagem de Banco de Dados: modelo relacional próprio, cadastro de clientes e veículos, registro de locações e devoluções e consulta de histórico persistido em MySQL. |
| **[rota](https://github.com/gabrielfranca10/rota-fccpd)**<br /><sub>Python · threads · stdlib</sub> | Núcleo de despacho de pedidos de delivery com concorrência baseada em threads, usando só a biblioteca padrão. Projeto em equipe de Computação Concorrente, Paralela e Distribuída, com roadmap de quatro entregas. |
| **EDA — Online Food Delivery**<br /><sub>Python · Pandas · Google Colab</sub> | Análise exploratória do Online Food Ordering Dataset (Kaggle): limpeza, perfil das variáveis, distribuições e relações entre atributos de clientes e pedidos. |

<details>
<summary><b>Mais trabalhos</b> — jogos e disciplinas de base</summary>
<br />

- **[Frevo Runner](https://github.com/yan791/Frevo_Runner)** — endless runner inspirado no Carnaval de Olinda, em C com Raylib. Atuei em refatoração do código, fluxo de Git da equipe e apresentação.
- **Cosmic Blaster** — jogo em C/Raylib feito em trio para Programação Imperativa e Funcional, aplicando listas encadeadas, matrizes e modularização em funções.

</details>

## Stack técnica

| Área | Tecnologias |
| :-- | :-- |
| **Linguagens** | ![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white) ![SQL](https://img.shields.io/badge/SQL-336791?style=flat-square&logo=postgresql&logoColor=white) ![Java](https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white) ![C](https://img.shields.io/badge/C-00599C?style=flat-square&logo=c&logoColor=white) |
| **Dados & Análise** | ![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat-square&logo=pandas&logoColor=white) ![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat-square&logo=numpy&logoColor=white) ![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=flat-square&logo=jupyter&logoColor=white) ![Google Colab](https://img.shields.io/badge/Colab-F9AB00?style=flat-square&logo=googlecolab&logoColor=white) |
| **Engenharia de Dados & Cloud** | ![AWS S3](https://img.shields.io/badge/AWS%20S3-569A31?style=flat-square&logo=amazons3&logoColor=white) ![AWS Athena](https://img.shields.io/badge/AWS%20Athena-232F3E?style=flat-square&logo=amazonwebservices&logoColor=white) ![dbt](https://img.shields.io/badge/dbt-FF694B?style=flat-square&logo=dbt&logoColor=white) ![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=flat-square&logo=streamlit&logoColor=white) |
| **Bancos de dados** | ![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white) ![JDBC](https://img.shields.io/badge/JDBC-ED8B00?style=flat-square&logo=openjdk&logoColor=white) |
| **Ferramentas** | ![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white) ![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github&logoColor=white) ![Linux](https://img.shields.io/badge/Ubuntu-E95420?style=flat-square&logo=ubuntu&logoColor=white) ![Obsidian](https://img.shields.io/badge/Obsidian-7C3AED?style=flat-square&logo=obsidian&logoColor=white) |

## Objetivo

Atuar como **Engenheiro de Dados**, projetando pipelines confiáveis, modelando dados para análise e garantindo que a informação chegue limpa, documentada e no tempo certo a quem precisa dela.

## GitHub Analytics

<p align="center">
  <img height="165" alt="GitHub stats"
       src="https://github-readme-stats.vercel.app/api?username=caioleimig&show_icons=true&hide_rank=true&hide=stars&hide_border=true&border_radius=8&bg_color=0D1117&title_color=2DD4BF&icon_color=2DD4BF&text_color=C9D1D9" />
  <img height="165" alt="Linguagens mais usadas"
       src="https://github-readme-stats.vercel.app/api/top-langs/?username=caioleimig&layout=compact&langs_count=8&hide_border=true&border_radius=8&bg_color=0D1117&title_color=2DD4BF&text_color=C9D1D9" />
</p>

<p align="center">
  <img alt="Contribution streak"
       src="https://streak-stats.demolab.com?user=caioleimig&hide_border=true&border_radius=8&background=0D1117&stroke=30363D&ring=2DD4BF&fire=2DD4BF&currStreakLabel=2DD4BF&currStreakNum=FFFFFF&sideNums=FFFFFF&sideLabels=C9D1D9&dates=8B949E" />
</p>

<!-- ============================================================ -->
<!--  Footer                                                       -->
<!-- ============================================================ -->
<p align="center">
  <img width="100%" alt=""
       src="https://capsule-render.vercel.app/api?type=waving&height=110&section=footer&color=0:14B8A6,50:134E4A,100:0B1120" />
</p>
