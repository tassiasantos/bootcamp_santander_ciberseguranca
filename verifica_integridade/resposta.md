# Verificação de Integridade de Arquivo

![Segmento](https://img.shields.io/badge/Segmento_:-Segurança_da_Informação-blue?style=flat-square)
![Tecnologias](https://img.shields.io/badge/Tecnologias_:-Python-lightyellow?style=flat-square) 
![Ano](https://img.shields.io/badge/Ano_:-2024-darkyellow?style=flat-square)

Esta é a minha resposta ao primeiro desafio de código oferecido pelo Bootcamp de Cibersegurança - Santander.

## Objetivo

Você foi encarregado de criar um sistema simples que verifica a integridade de arquivos, comparando o hash fornecido pelo usuário com o hash real do arquivo. Na função verificar_hashes que irá receber uma lista de hashes e compará-los com os valores esperados para cada arquivo. Seu objetivo é verificar se o hash calculado é igual ao hash esperado.

## Estrutura

* **Entrada**

  Uma lista de pares de hashes (hash calculado e hash esperado), separados por vírgulas, e cada par separado por ponto e vírgula.

* **Saída**

  Para cada par de hashes fornecido, o código imprime o resultado "Correto" ou "Inválido".

## Exemplos

A tabela abaixo apresenta exemplos com alguns dados de entrada e suas respectivas saídas esperadas. Certifique-se de testar seu programa com esses exemplos e com outros casos possíveis.

**Entrada	Saída**

| Entrada                       | Saída                |
|-------------------------------|----------------------|
| abc123, abc123	              | Correto              |
| def456, def789	              | Inválido             |
| 123abc, 123abc; 456def,456def	| Correto              |

## O Código em Pyhton 

Abaixo está o código criado em resposta, em linguagem python.

   ```bash
def verificar_hashes(lista_hashes):
 for hash_comparacao in lista_hashes:
     hash_calculado, hash_esperado = hash_comparacao.split(",")

     hash_calculado = hash_calculado.strip()
     hash_esperado = hash_esperado.strip()

     if hash_calculado == hash_esperado:
         print("Correto")
     else:
         print("Inválido")

hashes_usuario = input().strip()

lista_hashes = hashes_usuario.split(";")

verificar_hashes(lista_hashes)
  ...
