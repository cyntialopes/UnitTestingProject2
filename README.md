# UnitTestingProject2

# Phonebook

O **Phonebook** faz parte do projeto da disciplina de Teste Unitário da especialização em Testes Ágeis. Este projeto implementa uma classe Python que simula um registro de contatos telefônicos, e foi criado como parte do aprendizado sobre testes unitários e boas práticas de desenvolvimento.

## Funcionalidades

A classe **Phonebook** possui as seguintes funcionalidades:

### Inicialização

Ao criar uma instância da classe, um registro inicial é criado com um contato de exemplo (POLICIA - 190).

```python
phonebook = Phonebook()
```

### Adicionar Contato

Adicione um novo contato ao registro, fornecendo um nome e um número de telefone. O nome deve consistir apenas de letras e números.

```python
result = phonebook.add("Nome", "123456789")
# Retorna "Numero adicionado" se bem-sucedido
# Retorna "Nome invalido" se o nome não atender aos critérios
# Retorna "Numero invalido" se o número for vazio
```

### Procurar Número

Pesquise um número de telefone pelo nome associado.

```python
number = phonebook.lookup("Nome")
# Retorna o número associado ao nome se encontrado
# Retorna "Nome invalido" se o nome não atender aos critérios
```

### Obter Nomes

Obtenha uma lista de todos os nomes no registro.

```python
names = phonebook.get_names()
# Retorna uma lista de nomes de contatos
```

### Obter Números

Obtenha uma lista de todos os números no registro.

```python
numbers = phonebook.get_numbers()
# Retorna uma lista de números de contatos
```

### Limpar Registro

Limpe todo o registro de contatos.

```python
result = phonebook.clear()
# Retorna "phonebook limpado"
```

### Pesquisar Nomes

Pesquise todos os nomes que contêm uma substring específica.

```python
results = phonebook.search("mar")
# Retorna uma lista de tuplas (nome, número) que contêm a substring fornecida
```

### Obter Registro Ordenado

Obtenha o registro ordenado alfabeticamente.

```python
sorted_phonebook = phonebook.get_phonebook_sorted()
# Retorna uma lista de tuplas (nome, número) ordenadas alfabeticamente
```

### Obter Registro em Ordem Reversa

Obtenha o registro em ordem alfabética reversa.

```python
reversed_phonebook = phonebook.get_phonebook_reverse()
# Retorna uma lista de tuplas (nome, número) em ordem alfabética reversa
```

### Excluir Contato

Exclua um contato pelo nome.

```python
result = phonebook.delete("Nome")
# Retorna "Numero deletado"
```

### Alterar Número

Altere o número associado a um nome.

```python
result = phonebook.change_number("Nome", "987654321")
# Retorna "Numero modificado" se bem-sucedido
# Retorna "Nome não encontrado" se o nome não estiver no registro
```

### Obter Nome por Número

Obtenha o nome associado a um número.

```python
name = phonebook.get_name_by_number("123456789")
# Retorna o nome associado ao número se encontrado
# Retorna "Número não encontrado" se o número não estiver no registro
```

## Testes Unitários

A classe **Phonebook** é testada por meio de testes unitários implementados na classe **TestPhonebook**. Esses testes verificam se as funcionalidades da classe estão funcionando conforme o esperado. Os testes incluem cenários de sucesso e falha para garantir a robustez da classe.

## Como Executar os Testes

Para executar os testes unitários, você pode utilizar um framework de testes como o `unittest` padrão do Python. Basta criar uma instância da classe `TestPhonebook` e chamar a função `unittest.main()`.

```python
import unittest

# Importe a classe Phonebook e a classe TestPhonebook do módulo correspondente
from phonebook import Phonebook, TestPhonebook

if __name__ == '__main__':
    unittest.main()
```

Isso executará todos os testes definidos na classe `TestPhonebook` e mostrará os resultados no console.

## Conclusão

O **Phonebook** é uma implementação simples de um registro de contatos telefônicos em Python, oferecendo várias funcionalidades básicas para gerenciar contatos. Certifique-se de entender a lógica por trás de cada funcionalidade e como os testes foram implementados para garantir o bom funcionamento do código.
