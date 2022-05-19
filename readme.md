# Testes Focados

Prof. Andre Hora

Objetivo: mostrar que testes de unidade devem, preferencialmente, ser focados.

Explore o código da classe `Dollar` e o teste `WyCashTest`.
Observe que o teste `testDollar` é bastante genérico e testa duas funcionalidades distintas da classe `Dollar`, isto é, `times` e `equals`.

Clique no botão **run** para rodar os testes e veja a falha em `testDollar`.
Veja que a falha ocorre logo no primeiro assert (abaixo).
Portanto, os demais asserts não serão nem executados.

```java
assertEquals(new Dollar(10), five.times(2));
```

Divida o teste `testDollar` em dois testes: `testMultiplication` e `testEquality`.

Rode o teste novamente e veja que agora fica claro qual funcionalidade contém a falha, isto é, `times`.
A funcionalidade `equals` está correta e não contém nenhum erro, no entanto, isso não estava claro.

Conserte o erro no método `times` de `Dollar` e rode os testes novamente.

- Moral da história: métodos de testes focados permitem a identificação mais precisa de erros. Métodos de testes genéricos (como `testDollar`) não ajudam a identificar realmente onde o erro ocorreu e não fornecem garantias, pois os asserts podem nem ser executados.

- Tente sempre escrever testes curtos e focados em apenas uma funcionalidade do sistema. Evite escrever testes longos e que testam múltiplas funcionalidades.