
# Phishing - Identificação de Padrão

![Segmento](https://img.shields.io/badge/Segmento_:-Segurança_da_Informação-blue?style=flat-square)
![Tecnologias](https://img.shields.io/badge/Tecnologias_:-Python-lightyellow?style=flat-square) 
![Ano](https://img.shields.io/badge/Ano_:-2025-darkred?style=flat-square)

Esta é a minha resposta ao primeiro desafio de código oferecido pelo Bootcamp de Cibersegurança - Santander.

## Objetivo

Desenvovla uma solução para analisar uma lista de e-mails recebidos, verificando padrões comuns de phishing nas mensagens. Se um e-mail contiver palavras suspeitas como "ganhe", "prêmio", "urgente", "desconto", "click" e "promoção" ele deve ser classificado como "Phishing" e "Seguro".

## Estrutura

* **Entrada**

  Uma String contendo um conteúdo único representando o corpo do e-mail.

* **Saída**

  "Phishing" ou "Seguro" para cada e-mail.

## Exemplos

A tabela abaixo apresenta exemplos com alguns dados de entrada e suas respectivas saídas esperadas. Certifique-se de testar seu programa com esses exemplos e com outros casos possíveis.

**Entrada	Saída**

| Entrada                                    | Saída                   |
|--------------------------------------------|-------------------------|
| Ganhe um prêmio incrível hoje!	           | Classificação: Phishing |
| Não perca esta promoção exclusiva!	       | Classificação: Phishing |
| Você está convidado para a reunião amanhã! | Classificação: Seguro   |

## O Código em Pyhton 

Abaixo está o código criado em resposta, em linguagem python.

   ```bash
# Função para verificar se o corpo do e-mail contém palavras suspeitas de phishing
def verificar_phishing(mensagem):
    # Lista de palavras que indicam possíveis e-mails de phishing
    palavras_suspeitas = ["ganhe", "prêmio", "urgente", "desconto", "click",  "promoção"]
    
    # TODO: Verifique se alguma palavra suspeita está presente no corpo do e-mail:
    if any(palavra in mensagem.lower() for palavra in palavras_suspeitas):
      return "Phishing"
    return "Seguro"
            
        
email_usuario = input()

email_usuario = email_usuario.strip()

resultado = verificar_phishing(email_usuario)

print(f"Classificação: {resultado}")
   ```
