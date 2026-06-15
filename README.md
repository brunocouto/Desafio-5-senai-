# Desafio Semana 5 - Detecção de Estados com YOLO

Entrega do Grupo 8 para a disciplina de Visão Computacional.

## Objetivo

Treinar um modelo YOLO para detectar o estado de caixas de papelão:

- `aberta`
- `fechada`

## Notebook principal

Execute este arquivo:

```text
VC_Desafio_Semana_5_Entrega_Grupo8.ipynb
```

## Estrutura do projeto

```text
dataset_yolo/
  data.yaml
  images/
    train/
    val/
  labels/
    train/
    val/
imagens_baixadas/
imagens_reais/
imagens_teste_novas/
label_studio_config.xml
label_studio_export.json
requirements.txt
VC_Desafio_Semana_5_Entrega_Grupo8.ipynb
README.md
```

## Dataset e labeling

O dataset de treino e validação está em `dataset_yolo/`.

As imagens de teste estão em `imagens_teste_novas/` e não devem estar no treino nem na validação.

O projeto usa duas classes:

- `0`: caixa aberta;
- `1`: caixa fechada.

O labeling foi organizado em um projeto local do Label Studio. A configuração está em `label_studio_config.xml` e o export oficial está em `label_studio_export.json`.

## Instalação

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
python -m pip install -r requirements.txt
```

## Execução

1. Abra `VC_Desafio_Semana_5_Entrega_Grupo8.ipynb`.
2. Execute as células na ordem.
3. O notebook valida o export do Label Studio e o dataset YOLO antes do treino.
4. O baseline usa 2 épocas.
5. O treino ajustado usa 3 épocas.
6. As predições finais usam as imagens de `imagens_teste_novas/`.

## Label Studio

Para abrir um projeto local do Label Studio usando a configuração incluída:

```powershell
$env:LABEL_STUDIO_BASE_DATA_DIR = ".label-studio"
$env:SECRET_KEY = "desafio5-local-secret-key"
$env:LATEST_VERSION_CHECK = "false"
label-studio start desafio5-caixas
```

## Observação

Arquivos gerados pelo YOLO, caches, ambiente virtual, dados locais do Label Studio e pesos `.pt` não são versionados. Eles serão criados novamente ao executar o projeto.
