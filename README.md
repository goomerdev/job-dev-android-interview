![alt text](https://github.com/goomerdev/job-dev-android-interview/raw/master/media/logo-azul.png "Goomer")

## Challenge - Developer Android

Você provavelmente já está participando do nosso processo seletivo, mas se você caiu aqui por acaso, leia esse documento até o final e se você se interessar, pode começar o processo à partir daqui =]

Não é esperado que todos consigam realizar esse desafio por completo, já que é destinado a todos os níveis de carreira.

Você será avaliado pela sua capacidade de escrever um código simples, de fácil manutenção, e pela quantidade de funcionalidades que você entregar.

### Instruções

- **Nome do Projeto:** Goomer Lista Rango
- **Objetivo do Projeto:** Criar um aplicativo Android para Tablet, que consulte nossa API e exiba uma lista de restaurantes e o cardápio de cada um deles.
- **Tecnologia:** Kotlin/Java. Não utilize plataformas híbridas.
- **User Interface:** Você deve [usar esse link](https://xd.adobe.com/spec/f1288410-9211-41e1-588b-c5e98f0c6643-8719/) como referência de UI durante o desenvolvimento.
- **Entregáveis:** Crie um repositório pessoal para esse projeto, siga as instruções abaixo e responda e-mail recebido com link do repositório. Caso você resolveu fazer o teste por conta própria pode enviar para selecao.tech@goomer.com.br.

### Desafio

- Consulte a API disponibilizada para buscar as informações.
- Crie uma tela para exibir a lista de restaurantes indicando se cada um deles está aberto ou fechado:
    - Para cada restaurante, deve ser exibido os horários de funcionamento, as promoções ativas no momento e o cardápio.
    - O restaurante deve atualizar o status de aberto/fechado, de acordo com o horário de funcionamento, sem ser necessário recarregar ou reabrir a página.
- Crie uma tela para exibir o cardápio de cada um dos restaurantes:
    - Para os produtos com promoção ativa, deve ser exibido o valor original e o valor promocional.
    - As promoções ativas e o valor promocional devem ser atualizados na interface, de acordo com o horário, sem a necessidade de recarregar ou reabrir a página.

##### Formato de horários
- É necessário tratar os campos que indicam horários de funcionamento. 
- Os campos `from` e `to` possuem o formato `HH:mm`. 
- Caso o campo `to` possua um horário anterior ao valor de `from`, deve-se considerar que o horário se estende até o horário contido em `to` do próximo dia. Por exemplo, se `from` for `19:00` e `to` for `02:00`, o horário a ser considerado é das 19h do dia atual até às 02h do dia seguinte.
- O campo `days` guarda os dias da semana em que o horário é válido. Sendo Domingo o valor 1 e Sábado o valor 7. Os horários possuem intervalo mínimo de 15 minutos.

### O que nós vamos avaliar

- Você será avaliado pela qualidade do código, legibilidade e pela quantidade de funcionalidades implementadas.
- Você é livre para tomar as decisões técnicas com as quais você se sente mais confortável. Apenas esteja pronto para explicar as razões que fundamentaram suas escolhas =]
- Inclua um arquivo *README* que possua:
  - desafios/problemas com os quais você se deparou durante a execução do projeto.
  - maneiras através das quais você pode melhorar a aplicação, seja em performance, estrutura ou padrões. 
  - todas as intruções necessárias para que qualquer pessoa consiga rodar sua aplicação sem maiores problemas.

### Dicas

- Documente seu projeto em arquivos markdown explicando a estrutura, processo de setup e requisitos.
- Tenha sempre uma mentalidade de usabilidade, escalabilidade e colaboração.
- A organização das branches e os commits no repositório falam muito sobre como você organiza seu trabalho.
- Você pode utilizar bibliotecas de componentes visuais;
- Busque seguir o material de UI/UX da forma mais fiel possível. Caso você encontre alguma inconsistência ou limitação e veja a necessidade de fazer algo diferente, implemente da forma que pensa e explique os motivos.
- Seria legal você restringir a visualização da tela para o modo *Landspace*.
- Os testes unitários são muito importantes.
- O design/estrutura do código da aplicação deve ser *production ready*.
- Tenha em mente os conceitos de *SOLID, KISS, YAGNI e DRY*.
- Use boas práticas de programação.

### API que você deve consumir

Temos uma API REST JSON para esse desafio e seus endpoints estão disponíveis publicamente.

**Examplos de consulta na API:**

- Busca de restaurantes - http://challange.goomer.com.br/restaurants
```
GET: http://challange.goomer.com.br/restaurants

Formato de Resposta:
[
  {
    "id": Number,
    "name": String,
    "address": String,
    "image": String,
    "hours:[
      {
        "from": String,
        "to": String,
        "days": [Number]
      }
    ]
  }
]
```

- Busca de cardápio de um restaurante - http://challange.goomer.com.br/restaurants/{id}/menu
```
GET: http://challange.goomer.com.br/restaurants/{id}/menu

Formato de resposta:
[
  {
    "restaurantId": Number,
    "name": String,
    "image": String,
    "price": Number,
    "group": String,
    "sales": [
      {
        "description": String,
        "price": Number,
        "hours": [
          {
            "from": String,
            "to": String,
            "days": [Number]
          }
        ]
      }
    ]
  }
]
```

### FAQ
#### Posso utilizar frameworks/bibliotecas?
Sim.

#### Quanto tempo eu tenho?

Quanto mais tempo você demorar, mais críticos seremos na sua avaliação =]

#### Kotlin or Java?
Você pode escolher qualquer uma delas.

### Happy coding 

![alt text](https://github.com/goomerdev/job-dev-android-interview/raw/master/media/may-the-force-be-with-you.jpg "Happy Ccoding!!!")
