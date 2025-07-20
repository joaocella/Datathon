# Projeto de Compatibilidade e Plataforma de Vagas

Este repositório contém dois programas principais:

1. **Programa 1: Classificador de Compatibilidade**
2. **Programa 2: Aplicativo Web em Streamlit + Ngrok**

---

## 🎥 Demonstração em Vídeo

O vídeo a seguir demonstra o funcionamento completo dos dois programas:

🔗 https://www.youtube.com/watch?v=FjJXoPNBDUc&feature=youtu.be

---

## 📂 Estrutura dos Dados

Os dados estão em formato **JSON**. Todas as informações sensíveis (nome, e-mail, celular) foram **anonimizadas**.

- **jobs.json**: contém as informações das vagas (perfil da vaga, local, requisitos, benefícios etc.)
- **prospects.json**: contém as candidaturas por vaga, incluindo a situação do candidato
- **applicants.json**: contém os dados dos candidatos (informações pessoais, profissionais, formação, CV)

---

## 🚀 Programa 1: Classificador de Compatibilidade

### O que faz

- Realiza a leitura e limpeza dos dados de candidatos, vagas e candidaturas.
- Extrai variáveis de compatibilidade (match) como:
  - Localização
  - Faixa etária
  - Escolaridade
  - Idiomas
  - Experiência
  - Habilidades
  - Certificações
  - Necessidade especial (PCD)
- Treina um modelo **Random Forest** para prever o sucesso da contratação (`sucesso`).
- Avalia o modelo com métricas como **acurácia**, **f1-score** e **AUC-ROC**.
- Salva o modelo treinado em um arquivo `.joblib`.

### Como executar

1. Instale as dependências:
```bash
pip install pandas numpy nltk scikit-learn joblib
```

2. Execute o script principal:
```bash
python programa1.py
```

---

## 🌐 Programa 2: Aplicativo Web com Streamlit + Ngrok

### O que faz

- Interface Web interativa usando **Streamlit**
- Formulário de candidatura para o candidato
- Dashboard de acompanhamento de vagas e candidatos
- Armazena os dados em banco **SQLite**
- Usa **Ngrok** para criar uma URL pública e acessar o app remotamente

### Como executar

1. Instale as dependências:
```bash
pip install streamlit pyngrok pandas numpy sqlalchemy plotly
```

2. Obtenha um token gratuito do Ngrok: https://dashboard.ngrok.com/get-started/setup

3. Configure seu token no início do script:
```python
NGROK_AUTH_TOKEN = "seu_token_aqui"
```

4. Execute o script:
```bash
python programa2_streamlit.py
```

5. A URL pública do aplicativo será exibida no terminal.

---
6. Aqui está o MVP da plataforma deployado:
https://datathon-trecmzeaappcbwmbklsr4h3.streamlit.app/

## ✅ Requisitos adicionais

- Python 3.7 ou superior
- Conexão com a internet (para baixar recursos do NLTK e usar o Ngrok)
- Os arquivos JSON (`jobs.json`, `applicants.json`, `prospects.json`) devem estar na mesma pasta do script

---

## 📌 Observações Finais

- O vídeo no YouTube cobre **toda a lógica do Programa 1 e do Programa 2**.
- Os scripts estão organizados por etapas para facilitar manutenção e evolução.
- É possível adaptar o modelo para outros tipos de recrutamento e critérios.
- Compartilhamos um documento com a reunião dos links.
---

## 📜 Licença

Este projeto está licenciado sob a **MIT License**.
