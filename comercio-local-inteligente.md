# Comércio Local Inteligente

**Documento de produto, plano de validação e pesquisa jurídica sobre a viabilidade no Brasil**

Data: 1º de outubro de 2026. A pesquisa usou fontes públicas consultadas nesta data (lista completa na seção 16).

> **Aviso.** A seção 14 é um levantamento de pesquisa. Ela não substitui um parecer jurídico. Antes de lançar, leve a um(a) advogado(a) as perguntas da seção 14.17.

---

## Sumário

0. Resumo em uma página
1. Problemas centrais e decisões
2. O que já existe (e o que isso muda)
3. A tese
4. O produto da fase 1
5. Como o dado deixa de ser o problema
6. Modelo de negócio
7. Partida a frio
8. B2B (fase 2)
9. Inteligência de demanda (fase 3)
10. Eventos e emergências
11. Confiança e segurança proporcionais à fase
12. Plano de validação e roadmap
13. Recursos: quem constrói
14. Pesquisa jurídica
15. Riscos que continuam abertos
16. Fontes

---

## 0. Resumo em uma página

A ideia de comércio local inteligente cabe em cinco negócios diferentes: comparador de preços, ofertas relâmpago, marketplace B2B, inteligência de demanda e alertas de eventos. Tentar os cinco ao mesmo tempo, com comerciantes digitando preços à mão, não funciona. A pesquisa trouxe dois fatos que definem por onde começar:

1. **No Rio Grande do Sul, o comparador de preços para consumidor já existe, é gratuito e usa nota fiscal eletrônica.** É o Menor Preço Nota Gaúcha, da Receita Estadual, no ar desde 2019. Competir de frente nessa função é perder, porque o governo tem o dado real das vendas registradas em nota e você não tem.
2. **O próprio app do governo diz que não mostra ofertas.** Ele mostra preços já praticados em vendas passadas. Esse é o espaço vazio: o que está em oferta *agora*, o que *acabou de chegar*, e por quanto tempo.

As decisões são estas:

- **Núcleo do produto:** um "cartaz digital do bairro". O comércio publica o que está em oferta ou acabou de chegar, com meta de 30 segundos por publicação. Recebe o aviso só quem mora perto e pediu aquele tipo de produto.
- **Por onde começar:** perecíveis (açougue, hortifrúti, padaria, minimercado), em um único bairro de Caxias do Sul.
- **Prova pela nota fiscal:** o consumidor escaneia o QR code da NFC-e depois da compra. Isso comprova a visita para o comerciante, confere se o preço anunciado foi o cobrado e libera a avaliação.
- **Sem pagamento dentro do app nas fases 1 e 2.** A plataforma continua sendo vitrine, e isso reduz o risco de responder solidariamente pelo CDC. Também a mantém, em princípio, fora do conceito de "plataforma digital" da reforma tributária e fora da regulação de pagamentos do Banco Central.
- **Receita:** cobrar do comerciante por alcance e por visitas medidas, não por comissão sobre a venda.
- **B2B e inteligência de demanda viram fases posteriores**, com regras de concorrência e sanitárias definidas desde o desenho.
- **Sem alerta de clima para comerciantes.** No lugar dele entra um modo emergência que protege contra preço abusivo.
- **Validar antes de programar:** 4 a 6 semanas com um canal de WhatsApp ou Instagram operado à mão.

**Veredito jurídico em uma frase:** não encontrei impedimento legal ao modelo. Os riscos sérios aparecem em cinco situações:

- virar intermediador de pagamento sem estrutura para isso;
- usar dados de preço de concorrentes para orientar preços;
- listar produto de origem animal fora da área permitida pela inspeção sanitária;
- tratar localização e notas fiscais sem minimizar os dados;
- deixar um alerta de clima estimular preço abusivo.

---

## 1. Problemas centrais e decisões

| # | Problema | Decisão | Risco que continua |
|---|---|---|---|
| 1 | Catálogo de preços cadastrado à mão fica velho, e o consumidor perde a confiança | Sem catálogo. Só publicações com prazo, que expiram sozinhas. Publicação por foto, com meta de 30 s. Conferência posterior pela NFC-e | O comerciante parar de publicar |
| 2 | O comparador de preços já existe de graça, feito pelo governo e com dado melhor | Não competir nisso. Apontar para o Menor Preço e ocupar o espaço de ofertas ativas e novidades | O governo passar a mostrar ofertas |
| 3 | Num comparador, quem pagaria (o comerciante mais caro) é quem perde com a comparação | Nada de ranking de lojas por preço. O comerciante escolhe o que publica e paga por alcance e por visita medida | O comerciante não ver valor em pagar |
| 4 | Uma plataforma com quatro lados ao mesmo tempo esbarra no problema do ovo e da galinha | Um lado por vez: oferta primeiro, em raio pequeno. Cada loja traz os próprios clientes com um QR no balcão | Densidade insuficiente no bairro |
| 5 | O B2B esbarra em desintermediação, inspeção sanitária, nota fiscal e logística | Adiado para a fase 2. Cobrança por assinatura, não por negócio. O valor está em conformidade: rastreabilidade, inspeção e NF-e | A Ceasa Serra e as relações que já existem |
| 6 | "Sinais de demanda" de um app pequeno medem só os poucos usuários dele | Entram só com volume mínimo, limiares e tamanho de amostra visíveis | Demora a ter volume |
| 7 | Um alerta de chuva para comerciantes serve também para subir preço em emergência | No lugar dele, um modo emergência: prioriza disponibilidade, trava aumentos, aponta os canais de denúncia | Monetiza pouco |
| 8 | Painel com faixas de preço da concorrência é risco no CADE | Regras de desenho: nada de preço sugerido, nada de dado não público de concorrente, agregação com defasagem | Interpretação do CADE |
| 9 | MVP grande demais e antifraude pesado (biometria, liveness) antes de ter escala | Segurança proporcional à fase: CNPJ, visita presencial, avaliação só com nota fiscal | Fraude quando houver escala |
| 10 | Preço do serviço definido sem números | Modelo com hipóteses que dá para testar e a conta que o comerciante faz | O preço ser aceito |
| 11 | Ainda não está definido quem constrói | A fase 0 não exige código. A seção 13 lista as perguntas | Continua aberto |

---

## 2. O que já existe (e o que isso muda)

### 2.1 Comparadores públicos baseados em nota fiscal

**Menor Preço Nota Gaúcha (RS).** É feito pela Receita Estadual do RS e integrado ao programa Nota Fiscal Gaúcha.

- **Como funciona:** usa NF-e e NFC-e, e o preço entra no app assim que a nota é emitida.
- **Cobertura:** cobre os mais de 300 mil estabelecimentos credenciados ao programa.
- **Acesso:** exige cadastro na Nota Fiscal Gaúcha.
- **Recursos:** filtro por data e distância, e listas de compras.
- **O que ele não faz:** o FAQ do programa afirma que os valores são de vendas efetivas e que o objetivo não é apresentar ofertas. À pergunta sobre se a loja é obrigada a cobrar o preço exibido, o próprio FAQ responde que o valor é o do momento daquela venda e que, quanto mais recente a nota, maior a chance de ainda valer.
- **Limite de cobertura:** um texto do governo gaúcho indica que a comparação usa notas emitidas com CPF. Ou seja, a cobertura depende de o consumidor pedir CPF na nota.

**Menor Preço Brasil.** É a mesma tecnologia (Receita Estadual do RS e Procergs), oferecida a outros estados.

- Já é usada por 16 unidades da federação, contando o RS.
- O governo gaúcho informa que já comparou preços de 40 bilhões de documentos fiscais.
- Um teste feito em Brasília encontrou variação média de 25% entre estabelecimentos.

**Preço da Hora Bahia** (Sefaz-BA/Prodeb).

- Cobre cerca de 240 mil estabelecimentos e mais de 500 mil produtos.
- Passou de 1 milhão de downloads em 2025.
- Tem alerta de preço, listas de compras e histórico de preços.

**Menor Preço Nota Paraná.** Está no ar desde 2016. A lista de compras indica qual estabelecimento tem o menor total para o conjunto de produtos.

**O que isso muda.** Busca de preço, alerta de preço, lista de compras com total por mercado e histórico de preços já existem de graça nos apps estaduais (nem todo recurso em todos os estados), com dado melhor do que qualquer cadastro manual. Não construa nada disso como diferencial.

A variação de 25% mostra que comparar pode valer a pena, mas quem tem o dado é o governo. O que esses apps não fazem:

- avisar antes da venda acontecer;
- mostrar o que acabou de chegar;
- informar quantidade disponível;
- informar até quando vale a oferta.

### 2.2 Excedentes de alimentos: Food To Save

**Números da empresa** (segundo reportagens de 2026; os números variam entre fontes):

- foi fundada em 2021 e começou vendendo "sacolas surpresa" pelo Instagram, antes de ter app; o aplicativo veio um ano depois;
- já vendeu cerca de 9 milhões de sacolas e projeta faturar R$ 220 milhões em 2026;
- reúne mais de 5 mil estabelecimentos parceiros em 118 cidades;
- oferece descontos de até 70%;
- declarou prioridade em capitais e regiões metropolitanas e começou a entrar no interior de São Paulo em setembro de 2026.

**Como funciona:** o comerciante não cadastra item por item. Ele separa o excedente e monta uma sacola. O consumidor paga no app e retira na loja ou recebe por entrega, onde houver.

**O que isso muda:**

1. Confirma que comerciantes aceitam vender excedente com desconto por aplicativo.
2. Mostra que dá para validar com Instagram antes de ter app, porque foi assim que ela começou.
3. Indica que o esforço do comerciante é um atrito central. A sacola surpresa existe justamente para não exigir cadastro de itens.

Se o app pedir que o comerciante descreva cada item, ele pede mais trabalho do que o concorrente pede. A única resposta aceitável é publicar por foto, em segundos (seção 4.2).

**Verifique se a Food To Save já opera em Caxias do Sul antes de começar.**

### 2.3 O concorrente invisível: WhatsApp e Instagram

Comerciantes já postam ofertas no Status do WhatsApp e nos stories do Instagram. É gratuito e chega a quem já segue a loja. A plataforma só vale se fizer algo que esses canais não fazem:

- **Alcance novo:** chegar a quem mora perto e pediu aquele tipo de produto, mas não segue a loja.
- **Medição:** mostrar quem realmente apareceu, pela nota fiscal.
- **Descoberta no bairro:** juntar as ofertas de várias lojas próximas num lugar só.

Se, no teste, os comerciantes disserem que o Status já resolve, isso é uma resposta, não um obstáculo a contornar.

### 2.4 B2B regional: Ceasa Serra

- Em Caxias do Sul fica a Ceasa Serra, o maior centro de comercialização de hortifrutigranjeiros do interior do RS. Ela é administrada por um consórcio de 11 municípios.
- Em 2024 tinha cerca de 250 produtores associados, e as chuvas daquele ano atingiram aproximadamente 80% deles.
- A prefeitura usa a cotação da Ceasa Serra como referência no programa Ponto de Safra.

**O que isso muda.** Em Caxias, o encontro entre produtor e comprador de hortifrúti já tem lugar físico e preço de referência. A hipótese de que o produtor "não encontra compradores", portanto, precisa ser provada para hortifrúti em Caxias, não presumida. O espaço mais provável está em dois grupos:

- produtores que não estão na Ceasa;
- compras pequenas e recorrentes de minimercados e restaurantes.

---

## 3. A tese

### 3.1 Em uma frase

> **Um cartaz digital do bairro: o comércio publica em segundos o que está em oferta ou acabou de chegar hoje, e só recebe o aviso quem mora perto e pediu aquele tipo de produto.**

O problema de origem é este: *"o mercado colocou um cartaz de carne em promoção, mas só quem passa na frente sabe."* O produto resolve esse problema primeiro. B2B e inteligência de demanda ficam para fases posteriores (seções 8 e 9).

### 3.2 O que o app faz

- publicações com prazo (minutos ou horas), que expiram sozinhas;
- seguir lojas e categorias, com raio e horários definidos pelo consumidor;
- reserva opcional sem pagamento ("segurar por 30 minutos");
- comprovação pela nota fiscal: visita, preço honrado e avaliação;
- um painel simples de resultados para o comerciante.

### 3.3 O que o app não faz (decisões, não esquecimentos)

- não é comparador geral de preços; aponta para o Menor Preço;
- não processa pagamentos nas fases 1 e 2;
- não sugere preço a comerciante;
- não mostra a um comerciante dados não públicos de outro;
- não ranqueia lojas como "melhores";
- não aceita produto vencido nem produto de origem animal sem inspeção compatível com o local de venda;
- não aceita publicações de bebida alcoólica e tabaco na fase 1 (motivo na seção 14.12).

### 3.4 Por que essa tese resolve o conflito de incentivos

**Quem publica é quem ganha publicando.** É o comerciante com perecível perto do fim ou com novidade para anunciar.

**Publicar uma oferta não expõe o resto da tabela de preços.** O mercado mais caro não é punido pela plataforma. Ele apenas não precisa publicar.

**Quem paga é quem recebe clientes medidos.**

Um comparador cobraria justamente de quem perde com ele, o comerciante mais caro. Este modelo cobra de quem ganha.

---

## 4. O produto da fase 1

### 4.1 Tipos de publicação

| Tipo | Exemplo | Duração típica | Campos obrigatórios |
|---|---|---|---|
| Oferta relâmpago | "Frango inteiro R$ X/kg, uns 40 kg, até as 19h" | 1 a 4 h | produto, preço, unidade (kg/un.), quantidade aproximada, horário de término |
| Chegou / fresco | "Pão sai às 17h", "Chegou bergamota da serra" | até 1 dia | produto, horário |
| Fim do dia | "Restaram 12 pães, 50% até fechar" | até o fechamento | produto, preço, quantidade |
| Encomenda | "Aceitamos pedidos de costela para sábado" | alguns dias | produto, prazo, condição |

**Regras automáticas:**

- **Expiração:** toda publicação expira sozinha. Nada fica no ar com preço velho.
- **Validade:** se o comerciante marcar "próximo do vencimento", a data de validade aparece em destaque. Alguns estados exigem isso em promoções; no RS não encontrei lei equivalente (seção 14.4), mas o destaque fica como padrão.
- **Produto vencido:** não pode ser publicado. O termo de uso proíbe e o comerciante declara a validade.
- **Origem animal:** é pedido o selo de inspeção (SIF, SIE, SIM, SISBI ou SUSAF) do produto. Se o selo for só SIM, a loja precisa estar no mesmo município do estabelecimento inspecionado (seção 14.7).
- **Identificação da loja:** nome empresarial, CNPJ e endereço do estabelecimento aparecem sempre (Decreto 7.962/2013).
- **Publicidade:** toda publicação paga aparece com o rótulo "Patrocinado" (CDC, art. 36).

### 4.2 Fluxo de publicação (meta: 30 segundos)

1. O comerciante fotografa o produto, ou o cartaz de papel que ele já fez.
2. O app lê a foto e propõe o preenchimento: produto, preço e unidade.
3. O comerciante confirma a quantidade e o horário de término com botões ("1h", "2h", "até fechar").
4. Publica.

**Alternativa sem app:** o comerciante manda a foto para um número de WhatsApp da plataforma. Isso é útil na fase 0 e para quem não quer instalar nada.

**A meta de 30 segundos precisa ser medida com cronômetro, com comerciantes reais, no balcão, em horário de movimento.** Se passar de um minuto, a Food To Save vence pelo esforço menor.

### 4.3 Consumidor

- **Entrada sem cadastro pesado:** a pessoa escolhe o bairro, o raio e as categorias. Login só é pedido para reservar, escanear nota ou avaliar.
- **Seguir lojas:** o QR code no balcão leva direto para "seguir esta loja".
- **Controle de notificações:**
  - um teto diário com padrão baixo, por exemplo 3;
  - janelas de horário;
  - opção de silenciar categorias.
- **Feed do bairro:** mostra as publicações ativas de todas as lojas do bairro, ordenadas por proximidade e prazo, não por preço. Publicações pagas aparecem no topo, sempre marcadas como "Patrocinado" (seção 6.2).
- **Reserva opcional:** "segurar por 30 minutos", sem pagamento. O comerciante liga ou desliga a função. O risco é o cliente não aparecer, e isso precisa ser medido.

### 4.4 Comprovação pela nota fiscal (o diferencial técnico)

Toda NFC-e traz um QR code que abre a consulta pública da Secretaria da Fazenda, com os itens e valores da compra. Esse serviço foi feito para o consumidor conferir a própria nota. Vários apps privados já leem esse QR para organizar gastos.

**Quatro usos:**

1. **Visita comprovada.** O consumidor escaneia a nota depois da compra. O app confirma o CNPJ e a data e conta uma visita para o comerciante. Esse é o número que justifica a cobrança.
2. **Oferta honrada.** Se o item anunciado aparece na nota com o preço anunciado, a oferta ganha o selo "honrada". Se o preço foi outro, o app pergunta ao consumidor e registra a divergência. A taxa de ofertas honradas vira a reputação da loja.
3. **Avaliação verificada.** Só avalia quem tem nota daquele CNPJ nos últimos X dias. Isso reduz bastante o problema de avaliações falsas, sem biometria e sem análise de texto.
4. **Incentivo ao consumidor.** Pode ser um benefício oferecido pela própria loja, como desconto na próxima compra. **Evite sorteios:** distribuição gratuita de prêmios por sorteio exige autorização prévia (seção 14.14).

**Limitações:**

- **Descrição diferente:** a descrição do item na nota nem sempre bate com a oferta. O código de barras ajuda, mas hortifrúti a granel não tem.
- **Nota que não sai:** nem todo comércio emite NFC-e em toda venda.
- **Dependência técnica:** a consulta da Sefaz pode ter captcha, instabilidade ou mudanças sem aviso.
- **CPF na nota:** a nota pode trazer o CPF do consumidor, e esse dado deve ser descartado.

**Minimização de dados:** por padrão, guardar só CNPJ do emitente, data, valor e os itens que casam com ofertas. O resto do carrinho e o CPF são descartados, a menos que o consumidor consinta para algum recurso extra.

### 4.5 Painel do comerciante (fase 1)

- **Por publicação:**
  - quantos receberam o aviso;
  - quantos abriram;
  - quantas reservas houve;
  - quantas visitas foram comprovadas;
  - se a oferta foi honrada.
- **Seguidores:** total de seguidores da loja e as categorias que eles seguem, sempre em agregado.
- **Concorrentes:** nada. A decisão vale para toda a fase 1 (seção 9).

### 4.6 Fora da fase 1

Ficam de fora:

- lista com total por mercado (o governo já faz);
- mapa geral de preços;
- pagamento (fase 4, se fizer sentido);
- B2B (fase 2);
- inteligência de demanda (fase 3);
- alertas de clima para comerciantes (descartados; ver seção 10);
- biometria e prova de estoque por vídeo (seção 11).

---

## 5. Como o dado deixa de ser o problema

- **Prazo em vez de catálogo.** O que não é atualizado some sozinho. Nunca há um preço de três semanas atrás na tela.
- **Volume pequeno por comerciante:** algumas publicações por dia ou por semana, não milhares de itens.
- **Foto em vez de digitação.** A leitura automática corta o trabalho.
- **Conferência posterior.** A NFC-e mostra se o preço foi cumprido. Isso disciplina o comerciante sem fiscalização manual.
- **Preço de referência geral.** Se um dia fizer sentido mostrar "último preço registrado em nota", isso precisa vir de convênio formal com a Receita Estadual e a Procergs, não de raspagem (seção 14.15).

---

## 6. Modelo de negócio

### 6.1 Princípios

- O consumidor não paga.
- O comerciante paga pelo que dá para medir: alcance qualificado e visitas comprovadas.
- **Não há comissão por venda nas fases 1 e 2.** O motivo jurídico é que comissão aproxima a plataforma do papel de intermediador: responsabilidade solidária pelo CDC e possível enquadramento na LC 214/2025 (seções 14.2 e 14.8). O motivo prático é que comissão exige saber o valor de cada venda, o que na prática pede pagamento dentro do app.

### 6.2 Estrutura proposta (hipótese a testar)

| Plano | Para quem | O que inclui |
|---|---|---|
| Grátis | qualquer comércio verificado | até N publicações por semana; aparece no feed do bairro; notificação só para seguidores da loja |
| Bairro (mensal) | quem quer clientes novos | notificação também para não seguidores interessados na categoria; publicações ilimitadas; painel com visitas comprovadas |
| Destaque (avulso) | quem quer prioridade num horário | topo do feed por algumas horas, sempre com o rótulo "Patrocinado" |

**Cuidado com o destaque pago.** Na tese do STF sobre o Marco Civil, anúncio pago tem presunção relativa de culpa quando veicula conteúdo ilícito (seção 14.3). Publicação patrocinada precisa passar por regras automáticas mais rígidas ou por revisão antes de ir ao ar.

### 6.3 A conta que o comerciante vai fazer

Exemplo ilustrativo. Os números são hipóteses, não dados pesquisados.

- Um açougue rebaixa ou descarta X kg por semana.
- Se o app transformar metade disso em venda com desconto moderado, o ganho semanal é: *kg recuperados × margem recuperada por kg*.
- O preço do plano precisa ser uma fração pequena desse ganho.

**Descubra X e a margem nas entrevistas da fase 0.** Sem esses dois números, o preço é chute.

### 6.4 A sua conta

**Receita mensal** = comerciantes pagantes × preço médio.

**Custos:**

- infraestrutura;
- notificações;
- leitura de fotos por IA;
- consulta de notas;
- suporte;
- acima de tudo, o seu tempo de venda porta a porta.

Antes da fase 1, calcule quantos pagantes por bairro são necessários para cobrir o custo de abrir um bairro. **Se esse número for maior que o total de comércios relevantes no bairro, o modelo não fecha.** Melhor descobrir isso numa planilha do que depois de seis meses de desenvolvimento.

---

## 7. Partida a frio

- **Um lado por vez: oferta antes de demanda.** Sem pelo menos 10 a 15 comércios ativos num raio de 1 a 2 km (o mesmo número da fase 0, a confirmar no teste), o feed fica vazio e o consumidor não volta.
- **Cada loja traz a própria plateia.** Um cartaz com QR no balcão diz "receba as ofertas desta loja". Quem segue uma loja passa a ver as outras do bairro. É dessa descoberta cruzada que nasce o efeito de rede.
- **Canais do bairro:** grupos de condomínio, associação de moradores, paróquia e escolas, sempre com permissão de quem administra.
- **Densidade antes de área.** Não abra o segundo bairro antes de o primeiro passar nos critérios da seção 12.

---

## 8. B2B (fase 2)

### 8.1 Obstáculos e respostas

**Desintermediação.** Não cobre por negócio fechado. Cobre assinatura do comprador pelas ferramentas: pedidos recorrentes, histórico e documentos prontos. Aceite que parte dos contatos vai sair da plataforma. O que segura o usuário é a utilidade depois do primeiro contato, não uma trava.

**Inspeção de produtos de origem animal.** O selo é campo obrigatório. A plataforma filtra o alcance pela área permitida: SIM só no município, SIE e SUSAF-RS no estado, SIF e SISBI no país. Nada sem inspeção (seção 14.7).

**Rastreabilidade de vegetais frescos.** A bergamota, por exemplo, é citros, e citros está entre os produtos com rastreabilidade obrigatória pela INC 02/2018. A plataforma pode gerar o registro que a norma pede: produtor, lote, quantidade e comprador. **Esse é um motivo concreto para continuar usando a plataforma depois do primeiro negócio.**

**Nota fiscal.** No RS, a NF-e é obrigatória para todos os produtores rurais desde 5 de janeiro de 2026, e o talão em papel está vedado desde 1º de maio de 2026. A plataforma pode deixar os dados da venda prontos para o produtor emitir a nota, por exemplo no app gratuito Nota Fiscal Fácil. Isso ajuda quem ainda está se adaptando.

**Logística.** Fica fora do escopo inicial. A plataforma só registra "entrega até X km". Frete compartilhado é outro negócio.

**Ceasa Serra.** É complemento, não substituto. A cotação que ela divulga pode servir de referência. Vale conversar sobre parceria antes de ser visto como concorrente.

### 8.2 Forma do produto

- **Quadro de pedidos:** o comprador publica produto, quantidade, prazo e raio.
- **Disponibilidade semanal** do produtor.
- **Combinação por compatibilidade:** produto, quantidade, distância e abrangência sanitária.
- **Negociação em chat.** O preço combinado não aparece para outros compradores (seção 14.6).
- **Sem pagamento dentro da plataforma.**

### 8.3 Validar antes de construir

Entreviste 10 minimercados ou restaurantes e 10 produtores que não estão na Ceasa. Pergunte:

- como compram ou vendem hoje;
- com que frequência;
- o que costuma dar errado;
- quanto tempo gastam nisso.

Se a resposta for "ligo para o mesmo fornecedor há 15 anos e funciona", o B2B não é prioridade.

---

## 9. Inteligência de demanda (fase 3)

### 9.1 O que mostrar

- **Ao comerciante, os resultados dele mesmo.**
- **Interesse agregado dos consumidores por categoria, no raio.** Exemplo: "142 pessoas a até 2 km seguem 'peixe'; 3 lojas publicaram peixe esta semana."
- **Faixas de preço**, se houver, só a partir de ofertas que já foram públicas para consumidores. Sempre agregadas, com número mínimo de fontes e com defasagem.

### 9.2 Limiares (pontos de partida; ajustar com advogado)

- **Mínimo de fontes:** nenhum número de interesse é exibido com menos de N consumidores (por exemplo, 30), e nenhuma faixa de preço com menos de M estabelecimentos (por exemplo, 5).
- **Defasagem:** agregados de preço sempre atrasados (por exemplo, a semana anterior). Nunca em tempo real por concorrente.
- **Amostra visível:** o tamanho da amostra aparece sempre. Nada de "58% priorizam preço" sem dizer de quantas pessoas e como foi medido.

### 9.3 O que nunca fazer

- preço sugerido;
- alerta do tipo "seu concorrente subiu o preço";
- ferramenta que ajusta preço automaticamente com base em concorrentes;
- painel que mostra preços negociados no B2B entre outras partes.

O motivo está no caso Aprix (seção 14.6). É exatamente o tipo de intermediário comum que o CADE já tratou como risco.

---

## 10. Eventos e emergências

Uma ideia óbvia seria avisar o comerciante: "vai chover forte, prepare o estoque de água". Ela tem dois problemas:

1. **Pouco valor:** o comerciante já sabe que vende mais água antes de temporal.
2. **Risco alto:** numa calamidade, um aviso de "a demanda vai subir" convida a subir o preço, e preço abusivo foi exatamente o que o Ministério Público do RS autuou nas enchentes de 2024 (seção 14.10).

Por isso esse alerta fica de fora.

**Modo emergência.** Entra já na fase 1, porque é uma proteção e não um recurso de venda. É acionado por alerta oficial da Defesa Civil ou por decreto de calamidade.

- **Trava de preço:** publicações de itens essenciais (água, gás, alimentos básicos, combustível, higiene) ficam retidas para revisão quando o preço supera em mais de um limite (por exemplo, 10%) o último preço publicado pela mesma loja.
- **Disponibilidade primeiro:** o feed prioriza "tem água aqui agora" e "esgotou" em vez de desconto.
- **Denúncia:** um botão "denunciar preço abusivo" encaminha ao canal oficial (Procon ou Ministério Público). A plataforma não julga o caso; apenas encaminha.
- **Limite por cliente:** a loja pode exibir um limite de quantidade. Procons já admitiram essa prática em emergências, como nas enchentes de 2024.
- **No B2B (a partir da fase 2):** a pergunta passa a ser "quem ainda tem produto e consegue entregar". Isso é útil quando estradas do interior ficam bloqueadas, como em 2024.

Assim, o tema mais arriscado vira um argumento de confiança. O modo emergência monetiza pouco, mas é o tipo de coisa que faz um bairro defender o app.

---

## 11. Confiança e segurança proporcionais à fase

| Fase | O que entra | O que fica de fora |
|---|---|---|
| 0–1 | verificação de CNPJ (dados abertos da Receita Federal) e visita presencial a cada loja; avaliação só com nota fiscal; botão de denúncia; moderação manual; termos de uso, política de privacidade e regras de publicação; canal de notificação e recurso | biometria, liveness, detecção automática de comportamento coordenado |
| 2 | verificação do produtor (CPF ou CNPJ, inscrição estadual, NF-e emitida); histórico de negociações; avaliação comercial separada da avaliação de consumidor | prova de estoque por vídeo |
| 3+ | detecção de padrões coordenados, se houver volume que justifique | decisões automáticas sem revisão humana |

**Evite:**

- **Biometria e liveness.** Biometria é dado sensível na LGPD (art. 5º, II, e art. 11), com custo de conformidade alto e ganho pequeno nas fases iniciais.
- **Prova de estoque por vídeo.** É caro de operar e fácil de contornar. A taxa de ofertas honradas pela NFC-e mede a mesma coisa (se o comerciante cumpre o que anuncia) com dado real.
- **Suspensão decidida só por algoritmo.** O titular tem direito de pedir revisão (LGPD, art. 20), e a tese do STF exige devido processo de moderação.

**Penalidades graduais:** advertência, limitação temporária, remoção de conteúdo, suspensão e, em casos graves ou reincidentes, encerramento da conta. Cada passo tem registro, prazo de recurso e decisão humana.

---

## 12. Plano de validação e roadmap

### Fase 0 — sem código (4 a 6 semanas)

**Montagem:**

- Escolha um bairro de Caxias do Sul com comércio denso, onde você consiga visitar todas as lojas a pé.
- Feche com 10 a 15 comércios: açougue, hortifrúti, padaria e minimercado.
- Crie um canal ou lista de transmissão do bairro no WhatsApp (ou um perfil no Instagram) e coloque um cartaz com QR em cada loja.
- Os comerciantes mandam a foto e você publica por eles.

**O que medir:**

- publicações por semana por comerciante **sem você pedir**;
- inscritos no canal e quantos saem;
- visitas atribuídas, pelo relato do comerciante e por um código simples ("mostre esta mensagem no caixa");
- respostas das entrevistas:
  - quanto a loja perde por semana;
  - quanto pagaria pelo serviço;
  - por que publicaria aqui e não no Status do WhatsApp.

**Critérios para seguir em frente.** São pontos de partida: defina antes de começar e não mude no meio do teste.

- pelo menos 60% dos comércios publicando duas ou mais vezes por semana na quarta semana, sem você lembrar;
- em média, pelo menos 1 visita atribuída por publicação, ou relato consistente de venda;
- pelo menos metade dos comerciantes dizendo que pagaria, e citando um valor;
- saída do canal abaixo de 10% ao mês.

**Critério para parar ou mudar.** Se os comerciantes param de mandar ofertas quando você para de lembrar, o problema não é o app. É o incentivo, e programar não resolve isso.

### Fase 1 — MVP (só se a fase 0 passar)

**Escopo:** a seção 4 e o modo emergência (seção 10).

**Também entram:**

- termos de uso;
- política de privacidade;
- regras de publicação;
- canal de notificação e recurso;
- registro de acessos por 6 meses (seção 14.3).

**Métricas:** as mesmas da fase 0, agora medidas pela NFC-e.

### Fase 2 — segundo bairro e B2B leve

- Abra o segundo bairro só depois de o primeiro sustentar os números por 2 a 3 meses.
- O B2B entra como quadro de pedidos, sem pagamento (seção 8).

### Fase 3 — inteligência agregada

- Inteligência agregada com os limiares da seção 9.
- Conversa formal com a Receita Estadual e a Procergs sobre uso de dados de preço.
- Revisão de concorrência com advogado antes de liberar qualquer agregado de preço.

### Fase 4 — pagamento (se e somente se fizer sentido)

- Só por meio de instituição de pagamento parceira, com split, sem que a plataforma toque no dinheiro do comerciante (seção 14.9).
- Entram as obrigações da LC 214/2025 (seção 14.8).

---

## 13. Recursos: quem constrói

Sem saber quem constrói, o roadmap é uma lista de desejos. Antes da fase 1, responda:

- Você programa? Quantas horas por semana pode dedicar?
- Existe orçamento para infraestrutura, IA de leitura de foto e envio de notificações?
- Quem faz a venda porta a porta? Nas fases 0 e 1, esse é o trabalho principal, e não é técnico.
- Você está disposto a passar 4 a 6 semanas operando um canal à mão antes de escrever código?

A fase 0 exige só tempo. É o lugar certo para descobrir essas respostas sem gastar dinheiro.

---

## 14. Pesquisa jurídica

### 14.1 Veredito

**Não encontrei impedimento legal ao modelo.** Ele é viável no Brasil. Quase todos os riscos dependem de escolhas de desenho, e por isso este documento já toma essas escolhas.

Do mais grave para o menos grave, na minha avaliação:

1. **Concorrência.** Usar dados de preço de comerciantes para orientar outros comerciantes. As sanções são pesadas e o desenho errado é difícil de desfazer depois.
2. **Responsabilidade civil como intermediador.** Ocorre se a plataforma processar pagamento ou cobrar comissão por venda.
3. **Sanitário.** Produto de origem animal oferecido fora da área permitida pela inspeção.
4. **LGPD.** Localização, histórico de interesses e notas fiscais.
5. **Preço abusivo em emergência.**
6. **Obrigações procedimentais da tese do STF:** autorregulação, transparência e representante no Brasil.

### 14.2 Vitrine ou intermediador: a decisão jurídica mais importante

**O que diz a jurisprudência:**

- **STJ.** O tribunal distingue o site que apenas exibe anúncios ou resultados de busca do site que intermedeia a venda. O primeiro, em regra, não responde pelo negócio do anunciante. O segundo, que recebe comissão e torna a transação possível pelo próprio ambiente, integra a cadeia de consumo.
  - Essa distinção aparece no REsp 1.444.008/RS.
  - Também aparece num caso de 2022, em que a 3ª Turma afastou a responsabilidade de um site de classificados por fraude na venda de um veículo.
  - E aparece em decisões envolvendo o Buscapé (AREsp 144.823/RJ).
- **STF (2025).** A tese sobre o Marco Civil afirma que provedores que funcionam como marketplace respondem civilmente segundo o CDC.
- **Procon-MG/MPMG.** A Nota Técnica 05/2025 defende responsabilidade solidária do marketplace que participa da transação.
- **Tribunais estaduais.** Há muitos julgados reconhecendo solidariedade de plataformas que processam pagamento e recebem comissão (CDC, arts. 7º, parágrafo único, e 25, § 1º).

**Consequência para o desenho.** Nas fases 1 e 2, a plataforma:

- não processa pagamento;
- não cobra comissão por venda;
- não define os termos da venda (quem define é o comerciante);
- não usa frases como "garantido pela plataforma".

Isso não elimina toda a responsabilidade. A plataforma continua respondendo por falha do próprio serviço, como exibir um preço errado por erro dela. Mas reduz bastante o risco de responder solidariamente pelo produto do comerciante.

### 14.3 Marco Civil da Internet e moderação

**O que o STF decidiu.** O julgamento dos Temas 987 e 533 terminou em 26 de junho de 2025, e o acórdão foi publicado em 6 de novembro de 2025. O STF declarou o art. 19 do Marco Civil parcialmente inconstitucional. Na prática:

- **Regra geral:** o provedor pode responder por conteúdo ilícito de terceiros depois de notificação extrajudicial, sem precisar de ordem judicial.
- **Crimes contra a honra:** continua valendo o art. 19 (responsabilidade só depois de ordem judicial), mas a plataforma pode remover por notificação.
- **Anúncios pagos e impulsionamento:** há presunção relativa de culpa por conteúdo ilícito, mesmo sem notificação. A plataforma se livra provando que agiu com diligência e rapidez.
- **Sem responsabilidade objetiva** na aplicação da tese.

**Deveres adicionais para provedores de aplicação:**

- autorregulação com sistema de notificações, devido processo e relatórios anuais de transparência sobre notificações extrajudiciais, anúncios e impulsionamentos;
- canais de atendimento acessíveis;
- sede e representante no Brasil.

**O que isso significa para o app:**

- **Regras públicas.** Publique as regras de publicação e avaliação, com formulário de denúncia, prazo de resposta e recurso.
- **Remoção após notificação.** Publicação ilícita (produto vencido, sem inspeção, enganosa) sai depois de notificação, e tudo fica registrado.
- **Patrocinados com cuidado redobrado**, por causa da presunção de culpa.
- **Avaliações.** Uma avaliação ofensiva tende a cair no regime de crimes contra a honra (art. 19). Mesmo assim, ofereça direito de resposta ao comerciante e remoção por notificação quando houver afirmação factual falsa.
- **Relatório anual de transparência**, mesmo que curto, proporcional ao porte.

**Guarda de registros.** O provedor de aplicação organizado como pessoa jurídica, com atividade econômica, deve guardar os registros de acesso por 6 meses (Marco Civil, art. 15).

### 14.4 Código de Defesa do Consumidor

**Quem oferta é o comerciante.** Oferta suficientemente precisa vincula quem a faz (art. 30), e o consumidor pode exigir o cumprimento (art. 35).

- **Erro grosseiro.** O STJ (REsp 1.794.991/SE, 2020) admitiu que erro sistêmico grosseiro, comunicado rapidamente ao consumidor, pode afastar a vinculação.
- **Desenho que decorre disso:**
  - botão "corrigir ou cancelar" que avisa na hora quem recebeu a oferta;
  - registro do horário de cada publicação;
  - a expressão "enquanto durar o estoque", com quantidade aproximada, sempre visível.

**Identificação do fornecedor.** O Decreto 7.962/2013 exige identificar o fornecedor (nome empresarial, CNPJ, endereço) nos meios eletrônicos usados para oferta.

**Publicidade:**

- **Identificação (art. 36):** toda publicidade precisa ser identificável, daí o rótulo "Patrocinado".
- **Enganosa (art. 37):** é proibida. Avaliação forjada ou comprada por comerciante é risco dele e motivo de penalidade na plataforma.
- **Crime (arts. 66 e 67):** o CDC também tipifica como crime a afirmação falsa e a publicidade enganosa.

**Vencidos e próximos do vencimento:**

- Produto vencido é impróprio para consumo (art. 18, § 6º, I). Vender, expor ou guardar para venda configura crime (Lei 8.137/1990, art. 7º, IX).
- Produto próximo do vencimento pode ser vendido, com informação clara.
- **Leis estaduais e municipais** exigem destacar a validade em promoções. Por exemplo:
  - Paraná, Lei 17.478/2013 (produtos que vencem em até 10 dias);
  - Rio de Janeiro, Lei 9.910/2022;
  - Mato Grosso do Sul, Lei 4.250;
  - Campinas, lei municipal.
- **Não encontrei lei equivalente no RS.** Confirme a situação no RS e em Caxias do Sul. Mesmo assim, o app adota o destaque como padrão (seção 4.1).

**Preço:**

- **Preço abusivo:** é proibido elevar o preço sem justa causa (art. 39, X). Detalhes na seção 14.10.
- **Afixação de preço:** as regras da Lei 10.962/2004 e do Decreto 5.903/2006 obrigam o comerciante. O app deve exibir o preço e a unidade de venda (por kg ou por unidade), sem ambiguidade.

### 14.5 LGPD

**Que dados pessoais existem.** Localização, lojas e categorias seguidas e itens da nota fiscal são dados pessoais. Hábitos de consumo podem até revelar dados sensíveis indiretamente. Por isso o padrão é minimizar.

**Base legal por finalidade** (sugestão para validar com advogado):

| Finalidade | Base provável |
|---|---|
| Conta, feed local, reserva | execução de contrato (art. 7º, V) |
| Notificações promocionais | consentimento específico, revogável com um toque |
| Antifraude e segurança | legítimo interesse (art. 7º, IX), com teste de balanceamento documentado, como orienta o guia da ANPD de 2024 |
| Leitura da nota fiscal | consentimento no momento do escaneamento, guardando o mínimo (seção 4.4) |

**Localização:**

- No MVP, use o bairro escolhido mais a localização no momento do uso. Nada de rastreamento em segundo plano.
- Ao guardar, reduza a precisão (por exemplo, arredonde para algumas centenas de metros).

**Dados agregados:**

- Dado anonimizado sai do alcance da LGPD (art. 12).
- Mas a ANPD, no guia de anonimização que colocou em consulta pública, reconhece que nenhuma técnica é plenamente eficaz e recomenda análise por risco.
- Localização agregada em área pequena pode reidentificar pessoas. É por isso que existem os limiares da seção 9.

**Dados sensíveis.** Biometria é dado sensível (art. 5º, II, e art. 11). Por isso fica fora das fases iniciais (seção 11).

**Decisões automatizadas.** O titular pode pedir revisão de decisão tomada só por tratamento automatizado (art. 20). Por isso suspensão por antifraude passa por revisão humana (seção 11).

**Estrutura mínima:**

- encarregado de dados;
- registro das operações de tratamento (art. 37);
- relatório de impacto quando for o caso (art. 38);
- plano para incidentes, conforme o regulamento de comunicação de incidentes da ANPD.

**Regime de pequeno porte.** A ANPD tem regime simplificado para agentes de pequeno porte (Resolução CD/ANPD nº 2/2022). Verifique se o tratamento de localização se enquadra como de alto risco, o que retira parte das dispensas.

### 14.6 Concorrência (CADE)

**A lei.** A Lei 12.529/2011 (art. 36) trata como infração, entre outras condutas, acordar preços entre concorrentes e promover ou influenciar a adoção de conduta comercial uniforme.

**Troca de informações sensíveis.** O CADE trata a troca de informações concorrencialmente sensíveis como possível infração autônoma. Isso inclui preços, descontos, quantidades, margens e clientes. As medidas usuais de mitigação são:

- agregação;
- anonimização;
- defasagem temporal.

**Caso Aprix.** É o precedente mais próximo do que este produto poderia virar na fase 3.

- O software "Aprix", da Intelprice, era usado por postos de combustível e sugeria preços a partir de dados compartilhados pelos próprios postos.
- A investigação foi suspensa com um Termo de Compromisso de Cessação homologado pelo CADE.
- Segundo análise de escritório de advocacia, foi a primeira vez que o CADE analisou possível colusão algorítmica ligada a uma ferramenta de precificação.
- Uma análise publicada em 2026 relata que o CADE exigiu a abertura do modelo de precificação, inclusive do código-fonte.

**Investigação no setor aéreo (2026).** O CADE abriu processo contra Gol e Latam por possível alinhamento de preços. O foco é o uso de fornecedores comuns de inteligência tarifária como canal indireto de troca de informações.

**O que isso significa para o app.** Um painel de "visão da sua região", com faixa de preço por produto e "procura alta", seria exatamente o tipo de intermediário comum que o CADE observa.

- **Risco baixo:** ofertas que o próprio comerciante tornou públicas para consumidores.
- **Risco alto:** dados internos, preços de compra e preços negociados no B2B.

**Regras do produto:**

- as proibições da seção 9.3;
- preços negociados no B2B nunca visíveis a outros compradores;
- nenhuma agregação de preços de compra de concorrentes;
- registro das regras do sistema, para poder mostrá-las se alguém perguntar;
- revisão por advogado de concorrência antes da fase 3.

### 14.7 Sanitário

**Produtos de origem animal.** Carne, leite, ovos, mel, pescado e embutidos exigem inspeção oficial, e a área de venda depende do selo:

| Selo | Onde pode vender |
|---|---|
| SIM (municipal) | só no município |
| SIE (estadual) | no estado |
| SUSAF-RS (adesão estadual de estabelecimento com SIM) | no estado |
| SIF (federal) | no país e para exportação |
| SISBI-POA (equivalência) | amplia a área de quem aderiu |

- A base legal é a Lei 7.889/1989 e o RIISPOA (Decreto 9.013/2017).
- **No RS:** a Secretaria da Agricultura reafirmou em 2023 que é proibido o trânsito intermunicipal de produtos registrados só no SIM. A exceção é a adesão do estabelecimento ao SUSAF-RS ou ao SISBI.

**O que fazer:**

- **No varejo:** o app pede o selo do produto (seção 4.1), e o termo de uso proíbe publicar produto sem inspeção, com denúncia e remoção.
- **No B2B:** o selo é campo obrigatório e o filtro geográfico é automático.

**Vegetais frescos:**

- A INC 02/2018 (MAPA/Anvisa) tornou obrigatória a rastreabilidade de vegetais frescos listados na norma, entre eles citros, maçã, uva, batata, alface, repolho, tomate e pepino.
- Cada elo registra de quem comprou e para quem vendeu, e os registros ficam guardados por 18 meses.
- A IN 69/2018 fixa padrões mínimos de qualidade para venda no atacado e no varejo: produto limpo, firme, sem podridão, entre outros.

**Fora do escopo inicial:** alimentos processados de agroindústria (doces, conservas), que têm regras próprias de vigilância sanitária.

### 14.8 Fiscal e tributário

**Produtor rural no RS:**

- NF-e obrigatória em operações internas para todos os produtores desde 5 de janeiro de 2026;
- talão em papel (modelo 4) vedado desde 1º de maio de 2026;
- alternativas gratuitas: o app Nota Fiscal Fácil e a Nota Fiscal Avulsa eletrônica.

**Reforma tributária.** A LC 214/2025 (arts. 21 a 23), ajustada pela LC 227/2026, cria regras próprias para "plataformas digitais".

**Quem é plataforma digital pela lei:** quem intermedeia fornecedores e compradores e controla pelo menos um elemento essencial da operação:

- cobrança;
- pagamento;
- definição dos termos e condições;
- entrega.

**Quem fica de fora, em princípio:** comparadores de preço e plataformas de publicidade.

**Obrigações de quem está dentro:**

- inscrição no cadastro do IBS e da CBS;
- responsabilidade solidária quando o fornecedor não emite nota ou não presta as informações exigidas;
- dever de informar dados para o split payment quando o pagamento começa na plataforma;
- possibilidade de assumir a emissão da nota, com anuência do fornecedor.

**O app nas fases 1 e 2.** A plataforma não controla nenhum desses elementos e, em princípio, fica de fora. Um ponto de atenção: se a plataforma padronizar regras de reserva, isso pode ser lido como "definir termos e condições". Pergunte isso a um tributarista.

**Tributação da receita da própria plataforma** (assinaturas e destaques). Hoje há ISS municipal e tributos federais, com transição para IBS e CBS ao longo de 2026 a 2033. O enquadramento (Simples Nacional, atividade) é assunto para contador.

### 14.9 Pagamentos

**O enquadramento.** A plataforma que recebe o dinheiro do comprador e repassa ao vendedor tende a ser enquadrada como subcredenciador nos arranjos de pagamento (Resolução BCB 150/2021, alterada pela Resolução BCB 522/2025). Isso traz:

- contratos com credenciadoras e bandeiras;
- obrigações de liquidação conforme o volume.

**A saída** é não tocar no dinheiro do comerciante:

- nas fases 1 e 2, o pagamento é feito na loja;
- depois, se for preciso, usar uma instituição de pagamento parceira com split, em que cada parte recebe a sua parcela diretamente.

Receber a assinatura da própria plataforma é normal e não cria esse problema.

### 14.10 Emergências e preço abusivo

**O que a lei proíbe.** O CDC proíbe elevar preço sem justa causa (art. 39, X), e órgãos de defesa do consumidor aplicam isso com rigor em calamidades.

**Enchentes de 2024 no RS:**

- O Ministério Público do RS montou uma força-tarefa a partir de 4 de maio de 2024.
- Recebeu cerca de 680 denúncias e autuou 65 estabelecimentos, a maioria mercados e postos de combustível.
- Houve galão de 20 litros de água vendido a R$ 80 e duas prisões em um posto.

**Protocolo do Procon RS.** Em 2024, o Procon RS criou um Protocolo de Defesa do Consumidor em Calamidade, focado em itens de primeira necessidade como água, alimentos e combustível.

**Risco para a plataforma:**

- hospedar ou impulsionar oferta abusiva pode render responsabilização depois de notificação;
- no caso de publicação paga, vale a presunção de culpa (seção 14.3);
- o dano de reputação vem antes de qualquer processo.

**A resposta do produto** é o modo emergência descrito na seção 10.

### 14.11 Doação de excedentes (oportunidade, não risco)

**O que a lei permite.** A Lei 14.016/2020 autoriza estabelecimentos a doar excedentes ainda próprios para consumo: alimentos in natura, industrializados e refeições prontas, dentro da validade e nas condições de conservação.

- A doação não configura relação de consumo.
- A responsabilidade do doador termina na primeira entrega.
- O doador só responde nas esferas civil e administrativa se agir com dolo, e na penal só com dolo específico de causar dano à saúde.
- Se houver contraprestação em favor do estabelecimento, sai desse regime.

**Ideia de recurso:** "não vendeu até fechar? doe". O app conecta o comerciante a entidades e bancos de alimentos cadastrados.

**Cuidados:**

- não dar pontos, descontos ou vantagens ao comerciante em troca da doação, porque isso pode descaracterizar o regime;
- confirmar com advogado se a plataforma se encaixa como "intermediário" na lei.

### 14.12 ECA Digital

**O que é.** A Lei 15.211/2025 está em vigor desde 17 de março de 2026.

- Vale para serviços digitais direcionados a crianças e adolescentes ou de **acesso provável** por eles.
- É fiscalizada pela ANPD, com multas de até R$ 50 milhões por infração.
- Quem oferece conteúdo, produto ou serviço impróprio para menores de 18 anos precisa de mecanismos confiáveis de verificação de idade. Autodeclaração não basta.

**Aplicação ao app:**

- Um app de ofertas de comércio de bairro não é direcionado a menores e tende a ser pouco atrativo para eles. Mesmo assim, documente a avaliação de "acesso provável".
- O ponto concreto são **bebidas alcoólicas e tabaco**. Uma oferta de cerveja num app sem verificação de idade cria exposição. A solução mais simples na fase 1 é não aceitar esse tipo de publicação.

### 14.13 Inteligência artificial

O marco legal da IA (PL 2338/2023) foi aprovado no Senado em 10 de dezembro de 2024 e continua na Câmara aguardando parecer. O relator anunciou que a votação fica para depois das eleições de outubro de 2026. **Nada dele está em vigor.**

O que vale hoje para a leitura de fotos e para o antifraude:

- LGPD (especialmente o art. 20);
- CDC: se a IA ler o preço errado, a plataforma pode responder pela falha do próprio serviço. Por isso o comerciante sempre confirma antes de publicar. Quem responde quando ele confirma sem perceber o erro é uma das perguntas para o advogado (seção 14.17).

### 14.14 Promoções com sorteio

A distribuição gratuita de prêmios por sorteio, vale-brinde ou concurso exige autorização prévia do Ministério da Fazenda (Lei 5.768/1971). Para incentivar o escaneamento de notas, use benefícios diretos, como desconto na próxima compra. Não use sorteio.

### 14.15 Dados públicos e de terceiros

- **Menor Preço e outros dados da Sefaz.** Não faça raspagem. Busque convênio formal com a Receita Estadual e a Procergs. Uma postagem pública afirma que a API do Menor Preço do Paraná teria regras proibindo o uso por terceiros. Não consegui verificar, mas reforça a regra de usar só com autorização.
- **NFC-e:**
  - só a consulta iniciada pelo próprio consumidor, ao escanear a própria nota;
  - uma consulta por nota, sem automação em massa;
  - respeito a captcha e limites;
  - CPF descartado.
- **CNPJ.** A Receita Federal publica dados abertos de empresas, que servem para verificar estabelecimentos.
- **Mapas.** Se usar Google Maps ou Places, siga os termos de uso, incluindo atribuição e a proibição de usar dados do Places em mapas de outros fornecedores.

### 14.16 Checklist jurídico por fase

| Item | Fase 0 | Fase 1 | Fase 2 | Fase 3 | Fase 4 |
|---|---|---|---|---|---|
| Empresa constituída (CNPJ), contador | recomendável | sim | sim | sim | sim |
| Termos de uso e regras de publicação | simples | sim | revisar para B2B | revisar | revisar |
| Política de privacidade e base legal por finalidade | simples (canal) | sim | sim | sim | sim |
| Encarregado de dados e registro de operações | — | sim | sim | sim | sim |
| Autorregulação, notificação, recurso e relatório anual (tese do STF) | — | sim | sim | sim | sim |
| Guarda de registros de acesso por 6 meses (MCI, art. 15) | — | sim | sim | sim | sim |
| Identificação do fornecedor em cada oferta (Decreto 7.962/2013) | sim | sim | sim | sim | sim |
| Rótulo "Patrocinado" e revisão de patrocinados | — | sim | sim | sim | sim |
| Bloqueio de produtos vencidos | sim | sim | sim | sim | sim |
| Bloqueio de álcool e tabaco | sim | sim | reavaliar com verificação de idade | reavaliar | reavaliar |
| Selo de inspeção e filtro geográfico | manual | sim | obrigatório no B2B | sim | sim |
| Rastreabilidade de vegetais (INC 02/2018) | — | — | sim | sim | sim |
| Modo emergência | manual | sim | sim | sim | sim |
| Revisão de concorrência antes de agregados de preço | — | — | — | sim | sim |
| Instituição de pagamento parceira com split; LC 214 | — | — | — | — | sim |

### 14.17 Perguntas para levar ao advogado

1. Padronizar regras de reserva (sem pagamento) faz a plataforma "definir termos e condições" para fins do art. 22 da LC 214/2025?
2. Como redigir os termos para manter a posição de vitrine e reduzir o risco de solidariedade pelo CDC?
3. Que limiares de agregação e defasagem são defensáveis perante o CADE para a fase 3?
4. Qual a melhor base legal para notificações promocionais e para a leitura da NFC-e? O tratamento de localização impede o regime de agente de pequeno porte?
5. O app precisa de avaliação formal de "acesso provável" pelo ECA Digital? A proibição de álcool e tabaco é suficiente?
6. Existe lei estadual ou municipal (RS e Caxias do Sul) sobre validade em promoções ou afixação de preços em meio digital?
7. A plataforma se enquadra como "intermediário" da Lei 14.016/2020?
8. Qual o formato mínimo aceitável de autorregulação e de relatório de transparência para uma empresa pequena, à luz da tese do STF?
9. Quem responde se a leitura automática da foto erra o preço e o comerciante confirma sem perceber?

---

## 15. Riscos que continuam abertos

Este documento resolve problemas de desenho, mas não garante que o negócio funcione. Estes riscos continuam, em ordem do que mais me preocupa:

1. **O comerciante preferir o Status do WhatsApp.** Se o alcance extra e a medição não valerem o esforço, ele volta ao que já usa. Só a fase 0 responde isso.
2. **O esforço de publicar.** Se publicar levar mais de um minuto, a sacola surpresa da Food To Save vence.
3. **O consumidor não escanear a nota.** Sem escaneamento, não há medição, oferta honrada nem avaliação verificada. O incentivo ao escaneamento precisa ser testado cedo.
4. **Dependência da consulta pública da Sefaz.** Uma mudança técnica pode quebrar o diferencial principal. Tenha um plano B: código no caixa ou confirmação do comerciante.
5. **Concorrentes com mais recursos.** O governo pode passar a mostrar ofertas, ou a Food To Save pode chegar à Serra (ou crescer nela, se já estiver lá) com publicação por item.
6. **Fadiga de notificação.** Um teto baixo protege o consumidor, mas reduz o alcance que você vende ao comerciante. Essa tensão não some.
7. **Tamanho do mercado por bairro.** Pode não haver comércios pagantes suficientes num raio pequeno (seção 6.4).
8. **Capacidade de execução.** Se for uma pessoa só, a venda porta a porta e o desenvolvimento competem pelo mesmo tempo.

---

## 16. Fontes

**Concorrentes e dados de preço**
- Nota Fiscal Gaúcha — Menor Preço: https://nfg.sefaz.rs.gov.br/site/MenorPreco.aspx
- Nota Fiscal Gaúcha — Perguntas e respostas do Menor Preço: https://nfg.sefaz.rs.gov.br/site/duvidas_menor_preco.html
- Governo do RS — Menor Preço Nota Gaúcha no Dia dos Namorados: https://www.estado.rs.gov.br/menor-preco-nota-gaucha-se-consolida-como-aliado-dos-consumidores-nas-compras-para-o-dia-dos-namorados
- Governo do RS — Menor Preço Brasil, 40 bilhões de documentos fiscais e 16 unidades da federação: https://estado.rs.gov.br/desenvolvido-no-rs-aplicativo-menor-preco-brasil-ja-comparou-40-bilhoes-de-notas-fiscais-para-15-estados-e-df
- Sefaz-BA — Preço da Hora passa de 1 milhão de downloads em 2025: https://www.sefaz.ba.gov.br/destaque/preco-da-hora-bahia-supera-1-milhao-de-downloads-em-2025-e-amplia-aprovacao-dos-usuarios/
- Sefaz-BA — Histórico de preços no Preço da Hora: https://www.sefaz.ba.gov.br/destaque/preco-da-hora-bahia-ajuda-consumidor-a-acompanhar-variacao-de-precos-e-comprar-melhor/
- Sefaz-PR — Menor Preço entra na rotina dos consumidores: https://www.fazenda.pr.gov.br/Noticia/Aplicativo-Menor-Preco-entra-na-rotina-de-consumidores-e-ajuda-paranaenses-economizar
- TabNews — comentário sobre a API do Menor Preço PR (não verificado): https://www.tabnews.com.br/jeronimofsneto/2c52b5ea-871e-4b73-90fe-a367c98f466c
- Portal da NF-e — Manual do DANFE NFC-e e QR Code: https://www.nfe.fazenda.gov.br/portal/exibirArquivo.aspx?conteudo=k/IuuaW4YiY%3D
- Anotadíssimo (exemplo de app privado que lê o QR da NFC-e): https://anotadissimo.app/
- Google — Termos e atribuições do SDK do Places: https://developers.google.com/places/android-sdk/attributions?hl=pt-br
- Seu Dinheiro — Food To Save, 9 milhões de sacolas: https://www.seudinheiro.com/2026/seu-negocio/9-milhoes-de-sacolas-surpresa-como-a-food-to-save-transformou-desperdicio-de-comida-em-negocio-cbcb/
- Diário do Litoral — Food To Save em 118 cidades: https://www.diariodolitoral.com.br/diario-mais/app-que-vende-comida-com-ate-70-de-desconto-vira-febre-em-mais-de-100/
- Food To Save — Como funciona: https://www.foodtosave.com.br/blog/o-que-e-a-food-to-save/
- Mobile Time — Food To Save, entregas e base de estabelecimentos: https://www.mobiletime.com.br/tapps/15/06/2026/dica-de-app-food-to-save/
- Sala da Notícia — Food To Save no interior de SP: https://portal.saladanoticia.com.br/noticia/68823/food-to-save-chega-a-tiete-e-inicia-expansao-pelo-interior-de-sao-paulo
- Prefeitura de Caxias do Sul — Ceasa Serra: https://caxias.rs.gov.br/noticias/2025/07/ceasa-serra-tem-novo-gerente-operacional
- Rádio Caxias — Chuvas atingiram 80% dos produtores da Ceasa Serra: https://www.radiocaxias.com.br/cerca-de-80-dos-agricultores-associados-ao-ceasa-serra-foram-atingidos-pelas-fortes-chuvas/
- Rádio Solaris — Ponto de Safra usa cotação da Ceasa Serra: https://radiosolaris.com.br/ponto-de-safra-ja-esta-em-funcionamento-na-epi-floresta-em-caxias-do-sul/

**Responsabilidade de plataformas e Marco Civil**
- STF — Material explicativo sobre a tese do art. 19: https://www.stf.jus.br/arquivo/cms/noticiaNoticiaStf/anexo/Informac807a771oa768SociedadeArt19MCI_vRev.pdf
- Conjur — STF fixa tese (26/6/2025): https://conjur.com.br/2025-jun-26/supremo-fixa-tese-sobre-responsabilizacao-de-plataformas-por-conteudo-de-usuarios/
- Machado Meyer — STF muda regime de responsabilização: https://www.machadomeyer.com.br/pt/inteligencia-juridica/publicacoes-ij/direito-digital/stf-muda-regime-de-responsabilizacao-das-plataformas
- Teletime — Acórdão publicado e deveres adicionais: https://teletime.com.br/06/11/2025/stf-publica-decisao-sobre-o-art-19-do-marco-civil-da-internet/
- Conjur — Presunção de culpa em anúncios pagos: https://conjur.com.br/2026-jun-17/stf-amplia-responsabilidade-das-plataformas-digitais-e-redefine-aplicacao-do-marco-civil-da-internet/
- JusDocs — Os quatro regimes e a data do acórdão: https://jusdocs.com/blog/responsabilidade-civil-plataformas-digitais-stf-art-19-marco-civil-internet
- STJ — Site de anúncios não responde por fraude do vendedor (2022): https://www.stj.jus.br/sites/portalp/Paginas/Comunicacao/Noticias/2022/31082022-Terceira-Turma-afasta-responsabilidade-de-site-de-anuncio-por-fraude-na-venda-de-veiculo.aspx
- STJ — AREsp 144.823/RJ (Buscapé): https://www.stj.jus.br/websecstj/cgi/revista/REJ.cgi/MON?seq=66156666&tipo=0&nreg=201200284649&SeqCgrmaSessao=&CodOrgaoJgdr=&dt=20161205&formato=PDF&salvar=false
- VLF Advogados — REsp 1.444.008/RS (busca × intermediação): https://vlf.adv.br/noticia_aberta.php?id=1082
- Procon-MG/MPMG — Nota Técnica 05/2025 sobre marketplaces: https://www.mpmg.mp.br/data/files/FA/00/0B/DD/B483B91002A442B9B9A8F9C2/Nota%20Tecnica%20n%205_Responsabilidade%20solidaria%20de%20marketplaces%20por%20vicios%20e%20defeitos%20em%20produtos%20e%20servicos%20de%20parceiros_Procon-MPMG_19%20dez%202025.pdf
- STJ — REsp 1.794.991/SE (erro grosseiro de preço): https://processo.stj.jus.br/jurisprudencia/externo/informativo/?aplicacao=informativo&acao=pesquisar&livre=%40cnot%3D017616

**Consumidor, validade e emergências**
- Procon-SP — Texto do CDC (2025): https://www.procon.sp.gov.br/wp-content/uploads/2025/02/CDC_2025.pdf
- IDEC — Validade dos alimentos e crime da Lei 8.137/1990: https://idec.org.br/consultas/dicas-e-direitos/prazo-de-validade-dos-alimentos-deve-estar-claro-aos-consumidores
- Jornal do Oeste — Lei 17.478/2013 do Paraná: https://jornaldooeste.com.br/geral/supermercados-devem-destacar-data-de-validade-de-produtos-em-promocao
- Diário do Rio — Lei 9.910/2022 do RJ: https://diariodorio.com/nova-lei-determina-que-supermercados-devem-avisar-sobre-condicoes-de-produtos-em-promocao/
- JusBrasil — Lei 4.250 do MS: https://www.jusbrasil.com.br/noticias/supermercado-deve-divulgar-validade-de-produtos-em-promocao/100060551
- Sul21 — MPRS autua 65 estabelecimentos (2024): https://sul21.com.br/noticias/geral/2024/05/ministerio-publico-autua-65-estabelecimentos-por-precos-abusivos-em-meio-a-enchentes/
- CNN Brasil — MPRS e preços abusivos: https://www.cnnbrasil.com.br/nacional/mp-do-rs-autua-estabelecimentos-por-venda-abusiva-em-meio-a-enchentes/
- Procon RS — Protocolo para calamidades: https://www.procon.rs.gov.br/protocolo-do-estado-estabelece-diretrizes-para-controle-de-precos-abusivos-em-calamidades
- Procon Canoas — Art. 39, X em calamidade: https://www.canoas.rs.gov.br/noticias/procon-canoas-notifica-estabelecimentos-por-precos-abusivos/
- Hora Hiper — Limitação de quantidade por cliente em emergência: https://horahiper.com.br/geral/procon-orienta-29-mercados-e-distribuidoras-de-agua-sobre-aumento-injustificavel-de-precos-devido-as-enchentes-no-rio-grande-do-sul-20485
- Dizer o Direito — Comentários à Lei 14.016/2020: https://www.dizerodireito.com.br/2020/06/comentarios-lei-140162020-que-autoriza.html
- Senado Notícias — Lei 14.016/2020: https://www12.senado.leg.br/noticias/materias/2020/06/24/fornecedores-de-alimentos-poderao-doar-excedentes-a-pessoas-necessitadas

**Dados pessoais, crianças e IA**
- ANPD — Estudo técnico sobre anonimização: https://www.gov.br/anpd/pt-br/centrais-de-conteudo/documentos-tecnicos-orientativos/estudo_tecnico_sobre_anonimizacao_de_dados_na_lgpd___analise_juridica.pdf/@@display-file/file
- Cescon Barrieu — Consulta da ANPD sobre o guia de anonimização: https://cesconbarrieu.com.br/anpd-abre-consulta-a-sociedade-sobre-proposta-de-guia-de-anonimizacao-e-pseudonimizacao-para-protecao-de-dados-pessoais/
- Machado Meyer — ECA Digital em vigor: https://www.machadomeyer.com.br/pt/inteligencia-juridica/publicacoes-ij/direito-digital/estatuto-digital-da-crianca-e-do-adolescente-lei-n-15-211-2025-entra-em-vigor-em-17-de-marco-de-2026
- Demarest — Cartilha do ECA Digital: https://www.demarest.com.br/wp-content/uploads/2026/03/Cartilha-ECA-Digital_V2.pdf
- Legishub — ECA Digital, ANPD e multas: https://blog.legishub.com.br/eca-digital/
- Câmara dos Deputados — Tramitação do PL 2338/2023: https://www.camara.leg.br/proposicoesWeb/fichadetramitacao?idProposicao=2487262
- LCF Consulting — Votação do PL 2338 depois das eleições: https://monitor.lcfconsulting.com.br/proposicoes/pl-2338-2023/

**Concorrência**
- Lefosse — Caso Aprix/Intelprice: https://lefosse.com/newsletter/o-uso-de-algoritmos-de-precificacao-no-radar-do-cade-intelprice-celebra-tcc-no-caso-do-software-aprix/
- Conjur — Compliance algorítmico e jurisprudência do CADE (2026): https://www.conjur.com.br/2026-jun-03/compliance-algoritmico-as-licoes-da-jurisprudencia-recente-do-cade/
- WebAdvocacy — Critérios no caso Aprix: https://webadvocacy.com.br/2026/04/27/cade-colusao-algoritmica/
- News Rondônia — CADE investiga Gol e Latam: https://newsrondonia.com.br/noticias/2026/04/29/cade-investiga-gol-e-latam-por-possivel-alinhamento-de-precos-em-rotas-domesticas
- CADE — Guia de Leniência 2025 (consulta pública): https://cdn.cade.gov.br/Portal/centrais-de-conteudo/publicacoes/guias-do-cade/Consulta%20P%C3%BAblica_Guia%20Leniencia%20do%20Cade%202025_setembro.pdf

**Sanitário e agro**
- Seapi-RS — Produtos com SIM e trânsito intermunicipal: https://www.agricultura.rs.gov.br/secretaria-da-agricultura-e-da-saude-emitem-nota-tecnica-sobre-comercializacao-de-produtos-de-origem-animal-registrados-no-sim
- Food Safety Brazil — SIF, SIE e SIM: https://foodsafetybrazil.org/atualizacao-servicos-de-inspecao-produtos-de-origem-animal-sif-sie-sim/
- Laborgene — SIM, SIE, SIF, SISBI e RIISPOA: https://www.laborgene.com.br/inspecao-sanitaria-brasileira-de-produtos-de-origem-animal-sim-sie-sif-e-sisbi-poa/
- LegisWeb — Texto da INC 02/2018: https://www.legisweb.com.br/legislacao/?id=356508
- Canal Rural — IN 69/2018 e produtos da INC 02/2018: https://www.canalrural.com.br/agricultura/hortifruti/ministerio-normas-comercializacao-hortifrutis/
- Controlare — Rastreabilidade e registros por 18 meses: https://www.controlare.com.br/blog/anvisa/rastreabilidade-de-frutas-e-verduras-para-o-comercio/

**Fiscal, tributário e pagamentos**
- Sefaz-RS — NF-e do produtor e prazo do talão em papel: https://fazenda.rs.gov.br/produtores-rurais-poderao-usar-nota-fiscal-em-papel-remanescentes-ate-30-de-abril
- Agrimídia — Talão vedado a partir de maio de 2026: https://agrimidia.com.br/negocios/2026/04/24/nota-fiscal-eletronica-passa-a-ser-obrigatoria-para-produtores-rurais-no-rio-grande-do-sul-a-partir-de-maio/
- Reforma Tributária (portal) — Conceito de plataforma digital e exclusão de comparadores: https://www.reformatributaria.com/opiniao/reforma-tributaria-e-plataformas-digitais-da-intermediacao-a-responsabilidade-pelo-ibs-e-cbs
- Conjur — Responsabilidade tributária das plataformas (arts. 21 a 23): https://www.conjur.com.br/2025-dez-29/responsabilidade-tributaria-das-plataformas-digitais-na-reforma/
- Conjur — Split payment e emissão pela plataforma: https://www.conjur.com.br/2025-jul-08/plataformas-digitais-entenda-as-alteracoes-provocadas-pela-reforma-tributaria-no-setor/
- LegisWeb — Resolução BCB 150/2021 (com redação da Res. BCB 522/2025): https://www.legisweb.com.br/legislacao/?id=421572
- Moip — Marketplace com split × marketplace que repassa: https://moip.com.br/blog/tudo-que-voce-precisa-saber-sobre-nova-regulamentacao-do-banco-central-para-marketplaces/
