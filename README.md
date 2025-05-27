# Desafio DIO: Azure Cognitive Search - Indexação e Consulta de Dados com AI Search

---

## 📄 Visão Geral do Desafio

Este repositório documenta a resolução do desafio proposto pela DIO, focado na aplicação prática do Azure Cognitive Search para indexação e consulta de dados utilizando recursos de Inteligência Artificial. O objetivo principal é demonstrar a capacidade de organizar, pesquisar e extrair conhecimento de grandes volumes de informações, explorando as funcionalidades avançadas do AI Search.

Durante este laboratório, foram explorados os conceitos de ingestão de conteúdo para IA, criação de índices inteligentes e a exploração prática dos dados organizados. A finalidade é desenvolver uma compreensão sólida sobre como essas ferramentas podem ser utilizadas para minerar e extrair conhecimento de conjuntos de dados complexos.

---

## 🎯 Objetivos de Aprendizagem Atendidos

Ao concluir este desafio, os seguintes objetivos de aprendizagem foram alcançados:

* **Aplicar os conceitos aprendidos em um ambiente prático:** Implementação de um serviço Azure Cognitive Search, configuração de indexadores, conjuntos de habilidades e índices.
* **Documentar processos técnicos de forma clara e estruturada:** Detalhamento das etapas de configuração, problemas encontrados e soluções aplicadas, bem como insights obtidos.
* **Utilizar o GitHub como ferramenta para compartilhamento de documentação técnica:** Organização do repositório com informações claras e acessíveis para demonstrar a compreensão técnica.

---

## 🚀 Tecnologias Utilizadas

* **Azure Cognitive Search:** Serviço de busca como serviço que adiciona recursos de busca inteligentes aos dados.
* **Azure AI Services (anteriormente Cognitive Services):** Utilizado para enriquecer os dados durante a indexação (por exemplo, extração de entidades, detecção de idiomas, OCR, etc.).
* **Azure Blob Storage:** Armazenamento de documentos para ingestão no Azure Cognitive Search.
* **Porta do Azure:** Para configuração e gerenciamento dos recursos.
* **Python (opcional):** Para interagir programaticamente com o serviço (SDK do Azure Cognitive Search).
* **Postman/Ferramenta de API:** Para testar consultas ao índice.

---

## 🛠️ Etapas Realizadas

As etapas abaixo descrevem o fluxo de trabalho para a implementação do desafio. Cada seção pode conter subdiretórios ou links para arquivos específicos com detalhes adicionais, capturas de tela e trechos de código.

---

### 1. Preparação do Ambiente no Azure

* Criação de um Grupo de Recursos no Azure.
* Provisionamento de um recurso de **Azure Storage Account (Blob Storage)** para armazenar os documentos a serem indexados.
* Upload dos documentos de exemplo para um contêiner no Blob Storage.
* Provisionamento de um recurso de **Azure Cognitive Search**.
* Provisionamento de um recurso de **Azure AI Services** (ou um recurso multi-serviço) para integrar as habilidades de IA no pipeline de indexação.

---

### 2. Ingestão de Conteúdo para IA

* **Conexão de Dados:** Configuração de uma fonte de dados no Azure Cognitive Search apontando para o contêiner de Blob Storage.
* **Criação de Conjunto de Habilidades (Skillset):**
    * Definição de habilidades de IA para enriquecer os documentos (e.g., `OcrSkill` para extrair texto de imagens, `EntityRecognitionSkill` para identificar pessoas/organizações/locais, `KeyPhraseExtractionSkill` para identificar frases-chave, `LanguageDetectionSkill` para identificar o idioma do texto, `SentimentSkill` para análise de sentimento).
    * Mapeamento das entradas e saídas das habilidades para campos temporários ou diretamente para o índice.
* **Criação de Indexador:**
    * Associação da fonte de dados e do conjunto de habilidades ao indexador.
    * Configuração do agendamento do indexador.

---

### 3. Criação de Índices Inteligentes

* **Definição do Esquema do Índice:**
    * Criação de um novo índice no Azure Cognitive Search.
    * Definição dos campos do índice com seus respectivos tipos de dados (string, int, datetime, etc.).
    * Configuração de atributos para cada campo:
        * `Retrievable`: Se o campo pode ser retornado nos resultados da busca.
        * `Filterable`: Se o campo pode ser usado em expressões de filtro.
        * `Sortable`: Se o campo pode ser usado para ordenar os resultados.
        * `Facetable`: Se o campo pode ser usado para navegação facetada.
        * `Searchable`: Se o campo é incluído no índice de texto completo.
        * `Suggester`: Para habilitar sugestões de consulta.
* **Mapeamento de Campos:** Mapeamento dos campos enriquecidos pelo conjunto de habilidades para os campos correspondentes no índice.

---

### 4. Exploração Prática dos Dados Organizados

* **Execução do Indexador:** Monitoramento do processo de indexação no portal do Azure para garantir que os documentos foram processados e enriquecidos corretamente.
* **Testes de Consulta no Portal:** Utilização da ferramenta de "Search explorer" no portal do Azure para realizar consultas básicas e avançadas, testar filtros, ordenação e facetas.
* **Testes de Consulta via API (Opcional):**
    * Uso de ferramentas como Postman ou scripts Python para realizar consultas programáticas ao índice.
    * Exemplos de consultas utilizando busca de texto completo, filtros OData, ordenação, paginação e destaques.
* **Análise dos Resultados:** Observação de como o enriquecimento por IA melhora a relevância e a capacidade de descoberta dos dados.

---

## ✅ Conclusão

Este desafio me proporcionou uma imersão prática e valiosa no Azure Cognitive Search e nos Azure AI Services. Ao longo do projeto, consegui consolidar o entendimento sobre como a ingestão de dados, a criação de índices inteligentes e a exploração de informações se interligam para formar um sistema de busca robusto e eficiente.

---

## 🔗 Contato

📧 jorginho.vigas31@gmail.com  
📱 (11) 99403-2967  
💼 [LinkedIn](https://www.linkedin.com/in/jorgevigas/)
