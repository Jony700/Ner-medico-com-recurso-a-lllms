# Extração de Entidades Clínicas com Grandes Modelos de Linguagem

Este projeto foi desenvolvido no contexto de um estágio curricular na empresa Prologica, S.A., com o objetivo de aplicar Grandes Modelos de Linguagem (LLMs) à tarefa de Reconhecimento de Entidades Nomeadas (NER) em registos clínicos no domínio da cardiologia.

A abordagem combina técnicas de engenharia de prompts e fine-tuning parametricamente eficiente (PEFT), utilizando a metodologia QLoRA para adaptação de modelos LLM em ambientes com recursos computacionais limitados.

## Estrutura do Projeto

- `training.ipynb`: Notebook responsável pelo pré-processamento de dados e fine-tuning com QLoRA.
- `Identificação de classes ner com recurso a llms.ipynb`: Notebook com abordagem de engenharia de prompts e ensemble.
- `LICENSE.txt`: Licença de código aberto (GPLv3).
- `README.md`: Este ficheiro com instruções de uso.

## Requisitos

- Python 3.10+

Instalar dependências com:

```bash
pip install -r requirements.txt
```

## Execução

### 1. Fine-Tuning com QLoRA

Abra e execute o notebook `training.ipynb`. Certifique-se de que os dados estão corretamente formatados e que o ambiente suporta quantização em 4 bits (é possível executar em CPU, embora lentamente).

### 2. Inferência por Engenharia de Prompts

Abra o notebook `Identificação de classes ner com recurso a llms.ipynb`. Configure os parâmetros do prompt conforme o modelo desejado (ex: `Gemma 12B`) e execute a inferência em modo zero-shot.


## Resultados

Os testes indicaram que o fine-tuning com QLoRA proporciona um ganho substancial de acurácia em comparação com a abordagem zero-shot por prompt, mesmo com severas restrições de hardware.

## Autor

João Sousa  
Estágio Curricular | Prologica, S.A.  
Faculdade de Ciências da Universidade do Porto
