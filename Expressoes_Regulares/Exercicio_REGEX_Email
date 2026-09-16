Atividade - Construa um programa que:

Solicita 5 endereços de e-mail.
Valida cada endereço com Regex.
Armazena válidos e inválidos separadamente.
Exibe os dois grupos ao final.
Explica o motivo de cada rejeição.

```python
import re

# Regex para validação de e-mail
padrao_email = r'^[A-Za-z0-9._%+-]+@[A-Za-z0-9.-]+\.[A-Za-z]{2,}$'

validos = []
invalidos = []

for i in range(5):
    email = input(f"Digite o {i+1}º e-mail: ")

    if re.match(padrao_email, email):
        validos.append(email)
    else:
        motivo = ""

        if "@" not in email:
            motivo = "não possui o caractere '@'."
        elif email.count("@") > 1:
            motivo = "possui mais de um '@'."
        elif "." not in email.split("@")motivo = "o domínio não possui extensão válida (ex.: .com, .br, .edu)."
        else:
            motivo = "não segue o padrão válido de e-mail."

        invalidos.append((email, motivo))

print("\n=== E-MAILS VÁLIDOS ===")
for email in validos:
    print(email)

print("\n=== E-MAILS INVÁLIDOS ===")
for email, motivo in invalidos:
    print(f"{email} -> {motivo}")
```

Teste com as entradas fornecidas:

Entradas:

maria@gmail.com
joao.silva@udf.edu.br
estudante_01@faculdade.com
pedro.gmail.com
ana@dominio


Saída esperada:

=== E-MAILS VÁLIDOS ===
maria@gmail.com
joao.silva@udf.edu.br
estudante_01@faculdade.com

=== E-MAILS INVÁLIDOS ===
pedro.gmail.com -> não possui o caractere '@'.
ana@dominio -> o domínio não possui extensão válida (ex.: .com, .br, .edu).

Explicação das entradas inválidas

pedro.gmail.com -> Rejeitado porque não contém o caractere @, obrigatório em um endereço de e-mail.

ana@dominio -> Rejeitado porque o domínio não possui uma extensão válida após um ponto, como .com, .br, .edu.br, etc.

A expressão regular utilizada é:

^[A-Za-z0-9._%+-]+@[A-Za-z0-9.-]+\.[A-Za-z]{2,}$


Ela verifica se:

Existe uma parte de usuário antes do @;
Existe um domínio após o @;
O domínio possui uma extensão com pelo menos 2 letras;
São aceitos caracteres comuns em e-mails (., _, %, +, -).
