# Desafio Semana 5 - Detecção de Estados com YOLO

Entrega do Grupo 8 para a disciplina de Visão Computacional.

## Objetivo

Treinar um modelo YOLO para detectar o estado de caixas de papelão:

- `aberta`
- `fechada`

## Notebook Principal

Execute este arquivo:

```text
VC_Desafio_Semana_5_Entrega_Grupo8.ipynb
```

## Estrutura do Projeto

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
VC_Desafio_Semana_5_Entrega_Grupo8.ipynb
README.md
```

## Dataset

O dataset de treino e validação está em `dataset_yolo/`.

As imagens de teste estão em `imagens_teste_novas/` e não devem estar no treino nem na validação.

## Execução

1. Abra `VC_Desafio_Semana_5_Entrega_Grupo8.ipynb`.
2. Execute as células na ordem.
3. O notebook valida o dataset antes do treino.
4. O baseline usa 2 épocas.
5. O treino ajustado usa 3 épocas.
6. As predições finais usam as imagens de `imagens_teste_novas/`.

## Observação

Arquivos gerados pelo YOLO, caches e pesos `.pt` não são versionados. Eles serão criados novamente ao executar o notebook.
