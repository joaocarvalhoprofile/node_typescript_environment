# Test and TDD - Test-Driven Development

## Tipos de Testes

### Unit
### Integration
### End-To-End


### Por que devemos escrever testes ? Algumas das vantages de se escrever testes unitários são:
* Diminuir a quantidade de bugs do sistema;
* Dimiuir a necessidade de testes manuais;
* Desenvolver uma arquitetura mais eficiente;
* Facilitar o refactoring e aumentar a confiança.

# Fases do TDD
### Red: 
* escrever um teste que falhe.
### Green: 
* escrever o mínimo possível para o teste passar.
### Blue: 
* refatorar o código escrito.

# Leis do TDD
### 1ª Lei: 
* Você não deve escreve nenhum código em produção sem antes ter um spec falhando.
### 2ª Lei: 
* Você não pode escrever mais do que um teste unitário para fazer seu spec falhar, e não copilar é falhar.
### 3ª Lei: 
* Você não pode escrever mais do que o necessário para fazer o seu teste passar.

# Ténicas BDD
## GIVEN 
* a context - Definição de todas as informações necessárias para executar o comportamento que será testado
## WHEN 
* some condition - Executar o comportamento
## THEN 
* expect some output - Verificar o que aconteceu após a execução. comparando as informações retornadas com a expectativa que foi criada

# Ténicas TDD
## AAA = Arrange Act Assert - Triple A

### 1ª Arrange
* Nesta etapa nós configuramos tudo o que é necessário para que o nosso teste possa rodar, inicializamos variáveis, criamos alguns test doubles como Mocks ou Spies dentre outras coisas.
### 2ª Act
* Esta etapa é onde rodamos de fato o nosso teste. Chamamos alguma função ou método que queremos por a prova.
### 3ª Assert
* Esta etapa é onde faremos nosso assert. É onde verificamos se a operação realizada na etapa anterior (Act) surtiu o resultado esperado. Assim sabemos se o teste passa ou falha.

# Vantagens do Test Driven Development
### Tempo: 
* Desenvolver com TDD diminui consideravelmente o tempo que perdemos com debugging, que hoje sabemos é onde perdemos a maior parte do tempo em desenvolvimento.
### Foco: 
* Desenvolver em pequenos ciclos nos faz pensar em pequenos contextos, tornando nosso trabalho mais focado e mais controlado. Desenvolver em grandes ciclos é mais fácil de perder o controle e o foco do que queremos atingir.
### Cobertura: 
* A partir do momento que não escrevemos nada em produção sem antes ter um teste falhando, nossa cobertura de testes cresce podendo facilmente chegar a 90%, 95% ou mais.
### Confiança: 
* Com uma boa cobertura de testes bem escritos não temos receios nem medos na hora de mudar alguma coisa no código ou adicionar uma nova feature, pois sabemos que se algo sair errado nossos testes vão nos avisar.
### Documentação: 
* Os testes também são ótimas fontes de documentação, pois specs e métodos bem escritos, seguindo padrões de clean code, podem ajudar a entender o que aquela parte do código faz.
### Desacoplamento: 
* Desenvolvendo peças pequenas de software por vez, consequentemente estamos desenvolvendo código com baixo acoplamento, o que aumenta nossa escalabilidade.
### Disciplina: 
* A prática do TDD nos trás disciplina no desenvolvimento diário. Ela nos permite trabalhar em uma pequena parte do código por vez independente do todo o resto do sistema. Isso aliado à técnica pomodoro faz nossa produtividade aumentar exponencialmente.
### Boa Arquitetrua: 
* O TDD acaba moldando a arquitetura do nosso código de forma que ela fique menos acoplada e mais escalável.

# Tests Paterns
## Dummy
* Objetos que cr iamos apenas para completar a lista d eparametros que precisamos passar para invocar um determinado método
## Stubs
* Objetos que retornam respostas prontas, definidas para um determinado teste, por questão de performance ou segurança 
  (Exemplo: quando eu executtar o método fazer pedido preciso que o método pegar cotação do dolar retorne R$ 5,00)
## Spies
* Objetos que "espionam" a execução do método e armazenam os resultdos para a verificação posterior 
   (Exemplo: quando eu executar o método fazer pedido preciso saber se o método evniar email foi invocado internamente e com quais parametros)
## Mocks
* Objetos similares a stubs e spies, permitem que você diga exatamente o que quer que ele faça e o teste vai quebrar se isso
  não acontecer
## Fake
* Objetos que tem implementações que simulam o funcionamento da instancia real, que seria utilizada em produção
  (Exemplo: uma base de dados em memória)
