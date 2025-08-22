# 🚀 Pipeline ETL - GitHub API

## 📋 Descrição

Este projeto implementa uma **pipeline ETL (Extract, Transform, Load)** utilizando a API do GitHub, desenvolvido com foco na prática de **Programação Orientada a Objetos (POO)** em Python para especialização em **Engenharia de Dados**.

## 🎯 Objetivos

- **Praticar POO**: Implementar conceitos de orientação a objetos (herança, encapsulamento, polimorfismo, abstração)
- **Desenvolver Pipeline ETL**: Criar um fluxo completo de extração, transformação e carregamento de dados
- **Integrar com GitHub API**: Consumir dados da API pública do GitHub
- **Aplicar Boas Práticas**: Seguir padrões de código limpo e arquitetura modular
- **Especialização em Engenharia de Dados**: Aplicar conceitos fundamentais da área

## 🏗️ Arquitetura do Projeto

```
projeto_engenharia_de_dados/
├── src/
│   ├── extract/          # Camada de Extração
│   │   └── data_extraction.py
│   ├── transform/        # Camada de Transformação
│   │   └── data_transform.py
│   └── load/            # Camada de Carregamento
│       └── data_load.py
├── requirements.txt      # Dependências do projeto
└── README.md
```

## 🔧 Tecnologias Utilizadas

- **Python 3.x**
- **GitHub API** - Para extração de dados
- **Pandas** - Manipulação e análise de dados
- **NumPy** - Computação numérica
- **Requests** - Requisições HTTP para API

## 📦 Dependências

```bash
pip install -r requirements.txt
```

### Principais Bibliotecas:
- `requests==2.28.2` - Cliente HTTP para consumir a API do GitHub
- `pandas==2.0.0` - Manipulação e análise de dados
- `numpy==2.2.6` - Computação numérica
- `certifi==2025.8.3` - Certificados SSL/TLS

## 🎨 Padrões de POO Implementados

### 1. **Abstração**
- Classes abstratas para definir contratos de ETL
- Interfaces claras entre as camadas

### 2. **Encapsulamento**
- Métodos privados para lógica interna
- Propriedades públicas para acesso controlado aos dados

### 3. **Herança**
- Hierarquia de classes para diferentes tipos de extração
- Reutilização de código comum

### 4. **Polimorfismo**
- Múltiplas implementações para diferentes fontes de dados
- Comportamento flexível baseado no tipo de objeto

## 🔄 Fluxo da Pipeline ETL

### **Extract (Extração)**
- Conexão com a API do GitHub
- Coleta de dados de repositórios, usuários, issues, etc.
- Tratamento de rate limiting e autenticação

### **Transform (Transformação)**
- Limpeza e validação dos dados
- Agregações e cálculos
- Normalização de estruturas

### **Load (Carregamento)**
- Persistência em diferentes formatos
- Estruturação para análise posterior

## 🚀 Como Executar

1. **Clone o repositório**
```bash
git clone <url-do-repositorio>
cd projeto_engenharia_de_dados
```

2. **Instale as dependências**
```bash
pip install -r requirements.txt
```

3. **Configure as variáveis de ambiente** (se necessário)
```bash
export GITHUB_TOKEN=seu_token_aqui
```

4. **Execute a pipeline**
```bash
python src/main.py
```

## 📊 Exemplos de Uso

### Extração de Dados
```python
from src.extract.data_extraction import GitHubDataExtractor

extractor = GitHubDataExtractor()
repos_data = extractor.extract_repositories("username")
```

### Transformação de Dados
```python
from src.transform.data_transform import DataTransformer

transformer = DataTransformer()
clean_data = transformer.clean_repository_data(repos_data)
```

### Carregamento de Dados
```python
from src.load.data_load import DataLoader

loader = DataLoader()
loader.save_to_csv(clean_data, "repositories.csv")
```

## 🎓 Conceitos de Engenharia de Dados Aplicados

- **Data Pipeline**: Fluxo estruturado de processamento de dados
- **API Integration**: Consumo de APIs externas para coleta de dados
- **Data Quality**: Validação e limpeza de dados
- **Modular Architecture**: Separação clara de responsabilidades
- **Error Handling**: Tratamento robusto de erros e exceções
- **Logging**: Rastreamento de execução e debugging

## 🔍 Estrutura das Classes

### `GitHubDataExtractor`
- Responsável pela extração de dados da API do GitHub
- Implementa métodos para diferentes tipos de dados
- Gerencia autenticação e rate limiting

### `DataTransformer`
- Processa e transforma os dados extraídos
- Aplica regras de negócio e validações
- Prepara dados para carregamento

### `DataLoader`
- Persiste dados em diferentes formatos
- Gerencia conexões com sistemas de armazenamento
- Implementa estratégias de backup e versionamento

## 📈 Próximos Passos

- [ ] Implementar autenticação OAuth para GitHub
- [ ] Adicionar suporte a múltiplas fontes de dados
- [ ] Implementar cache para otimização de performance
- [ ] Adicionar testes unitários e de integração
- [ ] Implementar monitoramento e alertas
- [ ] Adicionar suporte a streaming de dados
- [ ] Implementar paralelização para processamento

## 🤝 Contribuição

Este projeto é focado no aprendizado e prática. Sinta-se à vontade para:

- Reportar bugs
- Sugerir melhorias
- Implementar novas funcionalidades
- Compartilhar conhecimento

## 📚 Recursos de Aprendizado

- [GitHub API Documentation](https://docs.github.com/en/rest)
- [Python POO Tutorial](https://docs.python.org/3/tutorial/classes.html)
- [Pandas Documentation](https://pandas.pydata.org/docs/)
- [Engenharia de Dados - Conceitos Fundamentais](https://www.databricks.com/glossary/data-engineering)

## 📄 Licença

Este projeto é desenvolvido para fins educacionais e de prática profissional.

---

**Desenvolvido com ❤️ para especialização em Engenharia de Dados**
