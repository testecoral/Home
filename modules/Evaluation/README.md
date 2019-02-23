Módulo de avaliação presencial 
==============================================

A avaliação presencial contará com questionários dinâmicos que serão configurados pelo administrador, que no caso de corais pode ser o maestro.

## Dados

### Tipos de Campo
Cada tipo de campo será implementado por uma classe no _frontend_.
Esta classe deverá expor qual o código do tipo e o comportamento do campo (se exibir combo, se exibir opções, etc.). 

### Questionários
Cada questionário possuirá mais ou menos a seguinte estrutura:
```yaml
$id: id auto-gerado
description: descricao do questionario
creation_date: data em que foi criado (principalmente para viabilizar ordenação e filtro)
questions:
  - id: id da questao
    type: tipo do campo, conforme os tipos definidos
    description: descricao da questao
    properties:
      # Propriedades da questao, conforme o tipo do campo
``` 

### Testes
Cada teste será armazenado como um documento mais ou menos na seguinte estrutura:
```yaml
$id: id auto-gerado
questionario_id: id do questionario sendo respondido
pessoa_id: id da pessoa que estará sendo avaliada
respostas:
  campo1:
    tipo: tipo do campo
    valor: resposta
  campo2:
    tipp: tipo do campo
    valor:
      subcampo: resposta do subcampo
      outro_subcampo: outra resposta
  campo3:
    tipo: tipo do campo
    valor:
      - resposta1
      - resposta2
```