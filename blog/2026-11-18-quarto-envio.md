---
title: "Pre-Release-2"
authors: vitorcoelho21
tags: [pre-release-2]
date: 2026-11-18
---

# 1-O que mudou, para você, entre o início da disciplina e este momento — tecnicamente e no seu jeito de trabalhar em equipe?

Tecnicamente mudou muita coisa. No começo quase toda a stack era novidade pra mim, e eu travava até no scraping do SIGAA. Hoje eu já consigo pegar uma ideia e levar ela do começo ao fim, como foi com a agenda do professor e com o SDK em Python, que eu estruturei do zero. Também aprendi a não confiar em regra que eu acho que está certa: várias vezes o dado real do SIGAA era diferente do que eu imaginava, tipo a grade de horário noturna, que estava errada até o Daniel testar com turma de verdade. Agora antes de escrever uma regra eu vou atrás de um exemplo real pra confirmar.

No jeito de trabalhar em equipe acho que a maior mudança foi parar de olhar só pra minha parte. Na primeira release cada um sabia da sua área e pouco do resto, e agora eu reviso PR dos colegas, eles revisam os meus, e muitos bugs que eu corrigi apareceram porque alguém do front achou e me avisou. Como Scrum Master também fiquei mais tranquilo, as reuniões de segunda viraram um momento de ver o que travou e o que depende de quem, e não só de perguntar "como está sua parte".

# 2-Descreva como as decisões técnicas estão sendo tomadas na sua equipe nesta fase — quem decide, como se chega a um consenso.

Nessa fase as decisões ficaram bem mais conversadas. Normalmente quem está mais perto do problema traz uma proposta, e a gente discute na reunião ou no próprio PR antes de implementar. Um exemplo foi a paginação e a busca nas listas de disciplinas e professores: a ideia veio do Daniel, porque o front estava baixando milhares de turmas só pra mostrar um número, e eu desenhei a solução no backend em cima do que ele precisava. Outro exemplo foi a troca do deploy do Railway pra AWS, que o Gabriel trouxe porque o teste grátis ia acabar bem perto da entrega, e o grupo aceitou depois de entender o motivo.

Quando é uma decisão maior a gente registra num ADR, pra ficar escrito o porquê e ninguém precisar lembrar de cabeça depois. Acho que o consenso tem saído mais fácil justamente porque cada decisão vem com um motivo claro e não só com "acho que é melhor assim", que era algo que acontecia mais no começo do projeto.

# 3-Que lacunas técnicas ainda te incomodam, e o que você tem feito, ou pretende fazer, a respeito?

O que mais me incomoda ainda é a parte de infraestrutura e deploy. Essa parte ficou mais com o Gabriel, e eu sei o básico de Docker e de como a aplicação sobe, mas se der um problema em produção eu ainda dependeria dele pra resolver. Como o deploy na AWS é manual, quero sentar com ele antes da entrega e seguir o passo a passo do guia de deploy pelo menos uma vez, pra não ter só uma pessoa que sabe fazer isso.

Outra lacuna é a parte de testes mais avançados, como teste de mutação e de sabotagem, que o João Paulo puxou. Vendo os resultados dele, que acharam falhas reais no scraper do SIGAA que estavam passando como sucesso, eu percebi o quanto isso é importante e o quanto eu ainda sei pouco. Quero entender melhor como ele montou esses testes, principalmente pros módulos que são meus, pra conseguir escrever teste desse tipo sozinho e não só o teste básico de que a função funciona.

# 4-Descreva uma situação recente de colaboração ou feedback, positiva ou difícil, que marcou sua semana.

O que mais me marcou foi a revisão que o Gabriel fez no meu PR do SDK. Ele apontou 9 problemas, desde uma URL padrão que nem funcionava até erro da API virando lista vazia sem avisar ninguém. Na hora deu um pouco de desânimo ver tanta coisa, mas quando fui corrigir percebi que quase tudo era algo que ia dar problema de verdade pra quem fosse usar o SDK. Corrigi todos, e o PR saiu bem mais sólido do que entrou.

Nessa mesma linha, o Daniel me trouxe dois problemas que ele achou usando a API no front: um professor chamado "A DEFINIR DOCENTE" aparecendo na lista como se fosse real, com mais de 150 disciplinas, e o total da paginação que o front não conseguia ler por causa de uma configuração de CORS. Eu corrigi os dois nessa semana. Acho que isso mostra bem como a colaboração está agora: cada um testa o trabalho do outro de verdade, e os feedbacks chegam rápido e bem explicados, o que facilita muito pra quem vai corrigir.

# 5-Que responsabilidades técnicas você tem assumido, e como você tem lidado com elas?

Nessa release eu fiquei com a agenda do professor, com o SDK em Python e com a paginação e busca nas listas de disciplinas e professores, além de várias correções que apareceram quando a gente começou a usar dados reais do SIGAA. Fora isso, continuo como Scrum Master, registrando as reuniões e as retrospectivas, e revisando PRs dos colegas.

No começo eu tentava fazer tudo ao mesmo tempo e acabava me perdendo. Agora tenho conseguido lidar melhor, porque eu foco em uma coisa por vez e priorizo o que trava os outros, como o que o Daniel precisava no backend pra conseguir terminar as telas. A parte de Scrum Master também me ajuda nisso, porque acompanhando o planejamento das sprints fica mais fácil ver o que é urgente e o que pode esperar. O que ainda é difícil é equilibrar o tempo entre programar e revisar, mas percebi que revisar com cuidado evita muito retrabalho depois, então tenho tentado não deixar essa parte de lado.
