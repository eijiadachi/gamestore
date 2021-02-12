# gamestore

## Objetivo
Este é um exercício para fixar os conceitos vistos sobre automatização de testes com JUnit e sobre critérios de Testes Funcionais

## Enunciado
O Sistema de Empréstimos Integrados de Jogos Ispeciais (S-EIJI) é um programa simples para controlar empréstimos de jogos, registrando: o usuário que realizou o empréstimo, a data em que um empréstimo é realizado, a data prevista para devolução e o valor previsto para cobrança. As seguintes regras deverão ser seguidas pelo programa. Empréstimos de até dois jogos devem ser devolvidos em até dois dias; já aqueles com mais de dois devem ser devolvidos em até três dias. Empréstimos com mais de dois jogos do mesmo gênero recebem um dia extra no prazo de devolução. Cada jogo tem um valor de empréstimo, sendo o valor cobrado pelo empréstimo o somatório do valor individual dos jogos. Empréstimos com mais de quatro jogos recebem um desconto de 10%. Empréstimos que custam mais do que R$ 100,00 recebem um desconto de 10%. Para empréstimos que custam mais de R$ 100,00 e tem mais do que quatro jogos, o valor do desconto é de 15%.

## Entregável
Você deverá implementar testes de unidade para a função responsável por registrar o empréstimo de uma lista de jogos em nome de um determinado usuário, registrar a data de empréstimo e calcular o valor a ser pago e a data prevista para devolução dos jogos, encapsulando tais informações no objeto do tipo `Rental`. Tal função é dedinida na classe `RentalService` com a seguinte assinatura:

    public Rental registerRental(User user, List<Game> games)

  
O seu objetivo é implementar casos de testes executáveis compatíveis com o JUnit 4. Todos os testes devem empregar a [`@Rule`](https://github.com/junit-team/junit4/wiki/Rules) do tipo [`ErrorCollector`](https://junit.org/junit4/javadoc/4.12/org/junit/rules/ErrorCollector.html) para realizar as assertivas e coletar e agregar as mensagens de erro.

Não é o seu objetivo implementar a lógica de negócio do método `RentalService.registerRental`. A implementação deste método contará como ponto extra, mas o critério para correção será binário: ou está 100% correto, ou está incorreto. Portanto, foque seus esforços na implementação dos testes. Para apoiar a criação dos testes, você deverá aplicar os critérios de particionamento em classes de equivalência e análise de valor limite. Também deverá produzir uma tabela de decisão para as condições e ações identidicadas a partir do enunciado das regras de negócio acima. As classes de equivalência, os valores limites e a tabela de decisão deverão estar num documento de texto com identificação do autor.

Observação: você pode alterar o código das classes de domínio, mas não deve alterar em hipótese alguma a assinatura do método `RentalService.registerRental`.
