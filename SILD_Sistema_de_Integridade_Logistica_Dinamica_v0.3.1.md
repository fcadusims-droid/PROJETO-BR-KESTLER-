# SILD — Sistema de Integridade Logística Dinâmica

## Protocolo Progressivo de Evidência Logística baseado em Confiança Zero

## Versão v0.5.6 — Arquitetura-Alvo de Campo e Padrão Global de Evidência
## Subversão operacional: v0.4.1 — MVP-0 Executável

## Como ler este documento

O SILD é descrito em duas escalas que não devem ser confundidas. A **arquitetura-alvo** é o mapa completo de campo e a transição para padrão global de evidência logística. O **MVP-0** é o recorte mínimo executável: auditoria de saída, registro de evidência, ingestão de glosa em template padrão e geração de dossiê de defesa e regresso.

Para separar uma escala da outra ao longo da leitura, cada seção é marcada por uma trilha — explicada logo abaixo, em "Convenção de leitura". Quem só vai operar o ciclo zero lê as seções `[MVP-0]` e `[BASE]`; as seções `[ALVO]` e `[PADRÃO]` orientam o roadmap.

---

## Convenção de leitura

Este é um documento único e propositalmente extenso. Para que o leitor não confunda **o que já é produto** com **o que é visão**, cada seção é marcada por uma trilha:

- **[MVP-0]** — pertence ao ciclo zero executável. É o que se constrói, vende e mede agora.
- **[ALVO]** — pertence à arquitetura-alvo de campo. Orienta o futuro; não é requisito do MVP-0.
- **[PADRÃO]** — pertence à ambição de padrão global, certificação e governança.
- **[BASE]** — fundamento conceitual, ético ou de vocabulário que vale para todas as trilhas.

A regra de ouro de leitura é:

> **Se você só tem 20 minutos e vai operar o ciclo zero, leia apenas as seções [MVP-0] e [BASE]. As seções [ALVO] e [PADRÃO] existem para orientar o roadmap, não para serem implementadas no piloto.**

Quem precisa de uma leitura ainda mais curta para reunião comercial deve ir direto às seções 1, 8.1, 63, 64, 69, 89 e 95, ou ao Apêndice B (Commercial Brief).

---

## Mapa de partes

O documento se organiza em sete partes temáticas. Os números entre colchetes são as seções.

- **Parte I — Fundamentos e tese** [1–7]: o que é o SILD, suas três camadas, ambição de padrão, vocabulário global, problema enfrentado, princípios de Confiança Zero e limites de identidade.
- **Parte II — Protocolo progressivo e captura** [8–20]: a escada de MVPs, Origin Snap, entrada de dados, níveis de captura C0–C2, Snap App, PACC Lite, classes de dispositivo, hub e âncoras, tempo e reboot.
- **Parte III — Objeto físico e simetria** [21–30]: lacre verificável, níveis de lacre, PIP Duplex Lite, Symmetry, tipos de destino, QR, WebSnap, objeto-evento-ator.
- **Parte IV — Modelo probatório** [31–53]: Evidence Object, estados por fase, classes internas, níveis de conformidade L0–L5, pacote de evidência, register e ledger, reconciliação, Fast Track, colisão probatória, Mesa Humana, RPI, Claim Intake, retenção, relatório e sistemas legados.
- **Parte V — Elegibilidade e operação** [54–62]: APIs, contingência, MEP, topologias, índices de cooperação e granularidade, disputas internas, relação com GR, governança financeira.
- **Parte VI — Comercial e piloto** [63–76]: defesa de receita, promessa do MVP-0, playbook, valor vs canhoto, separação arquitetura/MVP/piloto, roadmap, piloto recomendado, inviabilidade, métricas, arquitetura mínima, eventos, reason codes, LGPD, retenção.
- **Parte VII — Padrão, impacto e visão** [77–95]: governança do padrão, limites técnicos, decisões por fase, CTM, inteligência de rede, impacto sobre mercados ilícitos, negação logística, multimodal, modelo comercial, adoção, segmentação, formulações institucionais, valor unilateral antes da rede, seguradora como âncora de adoção, ameaças ao protocolo, saturação probatória adversarial e proteção de fluxo, inteligência federada e base legal, comunicação estratégica, segmentação ampliada e síntese.
- **Apêndices [A–D]**: recortes internos do mesmo documento — A (Field Spec técnico do MVP-0), B (Brief comercial do MVP-0), C (Tese de protocolo institucional) e D (Matriz de escopo congelado do MVP-0). São vistas filtradas; o corpo prevalece em caso de divergência.

---

## Índice navegável por trilha

> Os títulos abaixo são rótulos curtos para leitura rápida; o cabeçalho de cada seção no corpo pode trazer a forma completa.

**Parte I — Fundamentos e tese**
1. Definição geral · [BASE/MVP-0]
2. SILD como Protocolo, Plataforma e Certificação · [PADRÃO]
3. Ambição institucional de padrão global · [PADRÃO]
4. Vocabulário global e equivalência documental · [BASE]
5. Problema enfrentado · [BASE]
6. Princípios fundamentais · [BASE]
7. O que o SILD não é · [BASE]

**Parte II — Protocolo progressivo e captura**
8. Protocolo progressivo de evidência · [MVP-0 → ALVO]
9. Função central · [BASE]
10. SILD Origin Snap · [MVP-0 → ALVO]
11. Objeto do Origin Snap · [MVP-0 → ALVO]
12. Entrada de dados sem gargalo de TI · [MVP-0]
13. Níveis de captura: C0, C1 e C2 · [MVP-0 → ALVO]
14. SILD Snap App completo · [ALVO]
15. PACC Lite · [ALVO]
16. Fora do MVP-0 · [MVP-0]
17. Classes de dispositivo · [ALVO]
18. Smartphone como coletor oportunístico · [BASE]
19. SILD Hub e âncoras de ambiente · [ALVO]
20. Tempo local, reboot e reconciliação técnica · [ALVO]

**Parte III — Objeto físico e simetria**
21. Lacre verificável · [BASE/MVP-0]
22. Níveis de lacre por fase · [MVP-0 → ALVO]
23. PIP Duplex Lite · [ALVO]
24. SILD Symmetry · [ALVO]
25. Destino próprio · [ALVO]
26. Destino terceiro cooperativo · [ALVO]
27. Destino não cooperativo · [MVP-0/ALVO]
28. QR do lacre e QR de recebimento · [ALVO]
29. WebSnap · [ALVO]
30. Objeto, evento e ator · [BASE]

**Parte IV — Modelo probatório**
31. SILD Evidence Object · [BASE]
32. Estados externos por fase · [MVP-0 + ALVO]
33. Critérios de Custódia Concluída · [ALVO]
34. Matriz de uso interno, operacional e externo · [ALVO]
35. Classes internas · [ALVO]
36. Níveis de conformidade SILD L0–L5 · [PADRÃO]
37. Pacote de evidência · [MVP-0 → ALVO]
38. Evidence Register e Custody Ledger · [MVP-0 + ALVO]
39. Reconciliação assíncrona · [ALVO]
40. Evidências compensatórias · [ALVO]
41. Fast Track de reconciliação · [ALVO]
42. Colisão probatória · [MVP-0 + ALVO]
43. Mesa Humana · [ALVO]
44. RPI completa · [ALVO]
45. Severidade da RPI · [ALVO]
46. Ciclo de vida da RPI · [ALVO]
47. Janelas temporais da RPI · [ALVO]
48. SILD Claim Intake · [MVP-0 → ALVO]
49. Dados mínimos de uma glosa · [MVP-0]
50. Vínculo entre glosa, operação e RPI · [MVP-0 + ALVO]
51. Armazenamento, cold storage e legal hold · [ALVO]
52. Relatório SILD · [MVP-0 → ALVO]
53. Sistemas legados · [BASE]

**Parte V — Elegibilidade e operação**
54. Interoperabilidade e APIs · [ALVO]
55. Contingência · [BASE]
56. MEP — Motor de Elegibilidade Probatória · [MVP-0 + ALVO]
57. Topologias operacionais · [MVP-0 + ALVO]
58. Índice de Cooperação do Destino · [ALVO]
59. Índice de Granularidade da Custódia · [BASE]
60. Disputas internas à unidade lacrada · [BASE]
61. Relação com Gerenciamento de Risco · [BASE]
62. Governança financeira e bloqueio de faturamento · [BASE]

**Parte VI — Comercial e piloto**
63. Defesa de receita e regresso · [MVP-0]
64. Promessa comercial do MVP-0 · [MVP-0]
65. Playbook de reunião comercial · [MVP-0]
66. Valor contra canhoto tradicional · [MVP-0]
67. Separação entre arquitetura-alvo, MVP técnico e piloto · [BASE]
68. Roadmap de MVPs · [MVP-0 → PADRÃO]
69. Piloto comercial recomendado · [MVP-0]
70. Critérios de inviabilidade do piloto · [MVP-0]
71. Métricas de sucesso · [MVP-0 + ALVO]
72. Arquitetura mínima do MVP-0 · [MVP-0]
73. Eventos mínimos do backend · [MVP-0 + ALVO]
74. Reason codes internos · [MVP-0 + ALVO]
75. Segurança, LGPD e direito de imagem · [BASE]
76. Política de retenção e acesso · [BASE]

**Parte VII — Padrão, impacto e visão**
77. Governança do Padrão SILD · [PADRÃO]
78. Limites técnicos · [BASE]
79. Decisões operacionais por fase · [MVP-0 + ALVO]
80. CTM e mutações topológicas · [ALVO]
81. Inteligência de rede · [ALVO/PADRÃO]
82. Mecanismo de impacto sobre mercados ilícitos · [PADRÃO]
83. Núcleo de Negação Logística Ilícita · [PADRÃO]
84. Multimodal · [ALVO]
85. Modelo comercial · [MVP-0 → PADRÃO]
86. Adoção institucional · [PADRÃO]
87. Segmentação de mercado · [MVP-0]
88. Formulação institucional revisada · [BASE]
89. Valor unilateral antes da rede · [BASE/MVP-0]
90. Seguradora como âncora de adoção · [MVP-0 → PADRÃO]
91. Ameaças ao próprio protocolo · [BASE]
91-A. Saturação Probatória Adversarial e Proteção de Fluxo · [BASE/PADRÃO]
92. Inteligência de rede federada e base legal · [ALVO/PADRÃO]
93. Comunicação estratégica: visão interna versus mensagem de mercado · [BASE]
94. Segmentação ampliada por valor da prova · [MVP-0]
95. Síntese final · [BASE]

---

# PARTE I — FUNDAMENTOS E TESE

## 1. Definição geral · [BASE/MVP-0]

O **SILD — Sistema de Integridade Logística Dinâmica** é um protocolo progressivo de evidência logística. Em sua arquitetura-alvo, ele aplica princípios de Confiança Zero à cadeia de custódia. Sua função é medir, registrar e classificar a confiabilidade da narrativa operacional de uma carga, começando pelo estado inicial da custódia e evoluindo para simetria origem-destino, certificação probatória, reconciliação comercial e inteligência de rede apenas quando a operação demonstrar maturidade suficiente.

Esta versão v0.5.6 deve ser lida como **Arquitetura-Alvo de Campo e Padrão Global de Evidência**, não como promessa de implementação integral no primeiro ciclo. A subversão operacional **v0.4.1 — MVP-0 Executável** permanece como o recorte mínimo de produto para validação inicial: auditoria de saída, registro simples de evidência, ingestão padronizada de glosa e geração de dossiê de defesa/regresso.

O SILD não promete provar que uma carga é lícita, não certifica pureza material do conteúdo e não substitui inspeções físicas, perícia, fiscalização pública, gerenciamento de risco, seguradora ou autoridade competente. Sua função central é mais específica: **calcular quão confiável é a evidência que sustenta a história logística de uma carga**.

O SILD pleno não confia isoladamente no operador, no smartphone, no lacre, no WMS, no TMS, no cliente ou no sistema legado. Ele combina sessão viva, objeto verificável, ambiente ancorado, dispositivo conhecido, ator identificado, evidência física e reconciliação auditável para medir a força da narrativa logística.

No **MVP-0**, essa promessa deve ser reduzida: o produto ainda não implementa Confiança Zero plena. Ele organiza evidência operacional de origem e vincula essa evidência a uma glosa posterior para gerar defesa, seguro, auditoria ou regresso contra transportadora. A captura C0 é conformidade documental organizada, não prova antifraude forte.

A expressão **Confiança Zero** é um princípio do protocolo-alvo e não deve aparecer em material operacional ou comercial do MVP-0. Vender o ciclo zero como "Confiança Zero", "antifraude" ou "segurança logística" cria expectativa que o produto não cumpre. A descrição técnica interna do MVP-0 é **estruturador de prova de origem para defesa e regresso**; a comunicação comercial usa a linguagem de valor da seção 64, nunca a do protocolo.

A lógica central do SILD é:

> **A fraude logística raramente depende de um único evento falso. Ela depende da manutenção artificial de uma história coerente entre carga, lacre, veículo, rota, manifesto, operador, destino e evidência.**

O SILD torna essa história mensurável.

Em vez de perguntar apenas “há algo ilegal dentro da carga?”, o sistema pergunta:

> **A carga, o veículo, o lacre, o manifesto, a rota, os eventos de custódia e as evidências capturadas continuam formando uma narrativa logisticamente coerente e tecnicamente confiável?**

O SILD não torna a fraude impossível. Ele torna a mentira logística **mais cara, mais complexa, mais auditável e mais difícil de sustentar sem contradições**.

O SILD nasce por recorte. No primeiro estágio executável, registra NF, manifesto ou pedido, lacre, foto de contexto traseiro, foto aproximada do lacre e glosas recebidas pelo financeiro em template SILD. Em ciclos posteriores, adiciona PACC Lite, captura híbrida, Symmetry, G2 Lite, PIP Duplex Lite, RPI completa, SILD Hub, Fast Track, cold storage e inteligência de rede.

### Resumo executivo do MVP-0 (leitura de reunião)

> Este quadro é a leitura honesta do ciclo zero, sem a ambição das partes [ALVO] e [PADRÃO]. Quem só precisa entender o que se constrói e se vende agora pode parar aqui.

**O que o MVP-0 faz, em uma frase:** captura a evidência mínima de saída de uma carga (lacre serializado vinculado à NF + foto do lacre + foto de contexto), importa a glosa que chega ao financeiro em um template padrão, cruza as duas coisas e gera um dossiê de defesa em minutos.

**Para quem o dinheiro aparece primeiro:** regresso contra a transportadora e instrução de sinistro junto à seguradora. Esses são os dois fluxos onde o dossiê tem efeito financeiro imediato, porque dependem de contrato bilateral e de exigência probatória, não da boa vontade de um marketplace.

**O que o MVP-0 honestamente não faz:** não implementa Confiança Zero plena, não prova chegada, não prova conteúdo interno, não detecta fraude e não obriga marketplace a aceitar a versão do embarcador.

**Por que vale mesmo assim:** hoje, toda entrega contestada vira uma investigação improvisada de canhoto, foto de WhatsApp, e-mail e ligação. O MVP-0 troca essa caça manual por um dossiê estruturado, preservado no Dia 0, pronto para regresso, seguro ou negociação.

**O degrau é pequeno de propósito.** Tudo o que aparece depois — captura atestada, simetria origem-destino, granularidade por pallet, RPI, certificação, padrão global, inteligência de rede — é visão de roadmap. Importante para orientar o futuro, irrelevante para a primeira venda. Misturar as duas coisas numa reunião inicial transforma um produto honesto em algo que soa como promessa exagerada.

## 2. SILD como Protocolo, Plataforma e Certificação · [PADRÃO]

Para ambição global, o SILD deve ser compreendido em três camadas complementares, separadas conceitualmente e compatíveis tecnicamente.

### SILD Protocol

O **SILD Protocol** é o padrão de evidência de custódia. Ele define vocabulário, eventos, objetos probatórios, reason codes, estados externos, estados internos, classes de captura, classes de cadeia, critérios de elegibilidade, regras de reconciliação, estrutura de dossiê e limites de uso da evidência.

O protocolo deve poder ser implementado por diferentes plataformas, integradores, embarcadores, seguradoras, operadores logísticos, WMS, TMS, ERP, portais e sistemas de auditoria, desde que preservem os requisitos mínimos de conformidade.

### SILD Platform

A **SILD Platform** é a implementação operacional do protocolo. Ela pode incluir Console Web, Captura C0/C1/C2, Evidence Register, Custody Ledger, Claim Intake, RPI, Dossiê PDF, Snap App, SILD Hub, APIs, relatórios, integrações e inteligência de rede.

A plataforma executa o protocolo, mas não deve se confundir com ele. O SILD deve poder evoluir para padrão mesmo quando parte do mercado implementar apenas subconjuntos certificados do protocolo.

### SILD Certification

A **SILD Certification** é a camada de conformidade. Ela certifica componentes, fluxos, integrações e organizações quanto à aderência ao protocolo.

Podem existir certificações para:

- lacres;
- etiquetas e PIP Kits;
- docas;
- pátios;
- dispositivos de captura;
- SILD Hub;
- transportadoras;
- centros de distribuição;
- operadores logísticos;
- seguradoras;
- WMS, TMS, ERP e GR;
- integradores;
- relatórios e dossiês probatórios;
- fluxos de Claim Intake.

A regra é:

> **Produto resolve operação. Protocolo cria linguagem comum. Certificação transforma linguagem comum em padrão de mercado.**

O SILD MVP-0 continua sendo produto mínimo. A arquitetura-alvo passa a orientar um padrão global de evidência logística.

## 3. Ambição institucional de padrão global · [PADRÃO]

Em sua maturidade plena, o SILD pretende funcionar como **padrão de evidência de custódia para cadeias de entrega**.

Essa ambição não significa que o SILD deva fiscalizar, acusar, punir ou substituir autoridades públicas. Significa que o SILD deve criar uma linguagem técnica comum para que atores logísticos distintos consigam produzir, consumir, auditar e comparar evidências de custódia com critérios consistentes.

A formulação institucional é:

> **O SILD é um padrão progressivo de evidência de custódia para cadeias de entrega. Ele mede a confiabilidade da narrativa logística e define como eventos de custódia devem ser registrados, classificados, reconciliados, certificados e preservados.**

A ambição global do SILD depende de cinco condições:

1. vocabulário probatório padronizado;
2. objetos de evidência interoperáveis;
3. níveis de conformidade verificáveis;
4. governança de uso e privacidade;
5. adoção por atores que pagam por prova, seguro, defesa de receita, auditoria e redução de disputa.

A regra é:

> **O SILD não nasce global pelo tamanho da promessa. Ele se torna global se sua gramática probatória for adotável por muitas topologias, jurisdições e cadeias logísticas.**

## 4. Vocabulário global e equivalência documental · [BASE]

O SILD deve operar no Brasil sem ficar preso a conceitos exclusivamente brasileiros.

Termos como NF, DANFE, CNPJ, romaneio, canhoto e glosa são essenciais para o MVP nacional, mas o protocolo global deve trabalhar com abstrações equivalentes.

| Termo local ou operacional | Abstração global do SILD |
| --- | --- |
| NF, DANFE, invoice, fatura ou documento fiscal | shipment document / commercial document |
| CNPJ, tax ID ou cadastro equivalente | party identifier |
| manifesto, romaneio ou lista de carga | transport manifest |
| lacre | seal |
| transportadora | carrier |
| destinatário | consignee |
| pátio, doca, portaria, hub ou CD | controlled logistics node |
| pallet, gaiola, roll container, ULD, contêiner ou caixa | custody unit |
| canhoto, POD ou comprovante de entrega | proof-of-delivery artifact |
| glosa, chargeback, abatimento ou contestação | commercial claim |
| dossiê de defesa/regresso | evidence dossier |

A regra é:

> **O SILD deve aceitar documentos locais, mas seu protocolo deve falar a linguagem universal de objeto, evento, ator, contexto, evidência, claim e custódia.**

## 5. Problema enfrentado · [BASE]

Mercados ilícitos, desvios internos, fraudes documentais, roubos de carga, contaminação de remessas, avarias, faltas, chargebacks e disputas de entrega exploram uma fragilidade comum: a cadeia logística depende de declarações distribuídas entre muitos atores.

Em uma operação típica, diferentes partes controlam fragmentos da verdade:

- o embarcador declara o conteúdo;
- o armazém separa e libera a carga;
- o conferente atesta volumes;
- o motorista assume o transporte;
- a transportadora registra rota e eventos;
- a gerenciadora de risco monitora o veículo;
- o destinatário confirma recebimento;
- o cliente pode contestar depois;
- o financeiro pode travar faturamento;
- a seguradora analisa sinistros depois do fato.

Cada parte produz dados, mas esses dados nem sempre são completos, padronizados, independentes ou confiáveis. Em caso de falha, a pergunta crítica é difícil de responder:

> **Em que ponto a custódia da carga perdeu integridade ou deixou de ser comprovável?**

Na prática, muitas empresas só descobrem a fragilidade da prova quando já existe contestação, glosa, sinistro, chargeback, cobrança interna ou litígio. A equipe de logística precisa reconstruir a história da entrega depois do fato, buscando canhoto físico, foto de WhatsApp, rastro da GR, baixa de TMS, planilha, ligação com transportadora, e-mail do cliente e confirmação de portaria.

O SILD existe para reduzir essa investigação improvisada. Ele organiza a defesa da entrega no momento da operação.

## 6. Princípios fundamentais · [BASE]

O SILD opera sob o princípio de **Confiança Zero aplicada à logística**.

Isso significa que o sistema não presume automaticamente que uma evidência é confiável porque veio de um operador autorizado, de um aplicativo, de um manifesto, de um smartphone, de um lacre, de uma transportadora, de uma gerenciadora de risco, de um WMS, de um TMS ou de um sistema corporativo.

Cada dado é avaliado conforme sua qualidade probatória, origem, contexto, independência, materialidade e coerência com os demais eventos.

As regras centrais do SILD são:

> **Imagem valida objeto. Contexto valida evento. Ator valida independência.**

> **Operador aciona a evidência; não autentica a verdade sozinho.**

> **Offline mantém a operação; âncora local fortalece a prova.**

> **Reconciliação explica a perda probatória; não purifica o passado.**

> **WMS, TMS, GR e EDI podem corroborar a narrativa; não apagam violação física observada.**

A primeira regra separa o que uma imagem mostra do que ela consegue provar. Uma foto pode mostrar um lacre correto, mas não comprova sozinha que a foto foi feita no destino, no horário correto ou por ator independente.

A segunda regra impede que o operador do pátio ou do destino seja tratado como raiz absoluta de confiança. Operador autorizado é condição necessária, não suficiente. Captura forte exige sessão viva, mídia direta, âncora de ambiente, dispositivo conhecido e objeto verificável.

A terceira regra reconhece a realidade de pátios com baixa conectividade. Falhas de internet não devem travar a logística, mas também não devem receber força probatória máxima sem sequência local íntegra, contexto válido e sincronização controlada.

A quarta regra impede a criação retroativa de uma história perfeita. Evidência posterior pode explicar, reconciliar e encerrar uma disputa operacional, mas não apaga a lacuna original.

A quinta regra define a relação com sistemas legados. Um WMS pode confirmar recebimento comercial. Um TMS pode corroborar cronologia. Uma GR pode indicar permanência compatível no destino. Nenhum desses sistemas, isoladamente, elimina um corte físico, lacre rompido, stretch refeito ou divergência material observada pelo SILD.

## 7. O que o SILD não é · [BASE]

O SILD não é um scanner universal de contrabando.

O SILD não é um sistema de bloqueio automático de caminhões.

O SILD não é uma ferramenta privada de fiscalização pública.

O SILD não é uma promessa de ausência de ilícitos.

O SILD não substitui polícia, alfândega, perícia, seguradora, autoridade regulatória ou inspeção física autorizada.

O SILD não transforma smartphones, lacres, vídeos, GPS, documentos, TMS, GR ou assinaturas humanas em prova absoluta.

O SILD não certifica conteúdo interno da carga sem inspeção material.

O SILD não presume culpa a partir de baixa qualidade de evidência.

O SILD não deve criar listas negras opacas, acusações automáticas ou negativas automáticas de cobertura.

O SILD é uma infraestrutura de **evidência, coerência e defesa operacional**.

Ele mede a força da evidência que sustenta a história logística de uma carga.

---

# PARTE II — PROTOCOLO PROGRESSIVO E CAPTURA

## 8. Protocolo progressivo de evidência · [MVP-0 → ALVO]

O SILD deve ser implantado em camadas. A força probatória aumenta apenas quando a operação real suporta a camada seguinte.

Este documento descreve a arquitetura-alvo e a transição para padrão global de evidência. O MVP-0 executável é apenas a primeira fatia dessa arquitetura.

### 8.1 MVP-0 — Auditoria de Saída e Defesa de Regresso

Registra a evidência mínima de saída e a conecta a uma glosa posterior recebida pelo embarcador.

Escopo:

- criar operação por NF, pedido ou manifesto;
- vincular lacre;
- capturar foto aproximada do lacre;
- capturar foto de contexto traseiro;
- armazenar evidência em registro operacional simples;
- importar glosa em template padrão SILD;
- vincular glosa à operação;
- gerar dossiê de defesa, seguro ou regresso.

O MVP-0 não implementa Confiança Zero plena, não depende de destino, não usa WebSnap, não exige SILD Hub, não opera G2 Lite e não promete vencer glosa de marketplace dominante. Seu valor é reduzir a caça manual a evidências e apoiar direito de regresso contra transportadora, seguro, auditoria e defesa comercial.

### 8.2 MVP-1 — Captura Atestada

Adiciona PACC Lite, câmera direta, bloqueio de galeria, captura guiada, hash de mídia, controle de sessão e melhor qualidade técnica de captura.

### 8.3 MVP-2 — Symmetry e Granularidade

Adiciona observação de destino quando houver destino próprio ou cooperativo. Quando a dor envolver pallet, gaiola ou volume crítico, adiciona G2 Lite e PIP Duplex Lite.

### 8.4 MVP-3 — Plataforma Probatória

Adiciona RPI completa, Fast Track documental e visual validado, Storage Lifecycle Manager, SILD Hub opcional, integrações, cold storage, legal hold, Claim Intake avançado e inteligência de rede.

### 8.5 SILD Origin Snap

Registra o estado inicial da custódia no momento da saída: manifesto, veículo, unidade logística, lacre, fechamento físico e captura em sessão controlada.

No MVP-0, o Origin Snap é Basic/C0: foto do lacre, foto de contexto, vínculo com documento e hash simples de mídia.

### 8.6 SILD Symmetry

Adiciona observação de destino, formando simetria origem-destino. Quando o destino é próprio, a confirmação deve ser feita por aplicativo autenticado. Quando o destino é terceiro cooperativo, pode haver WebSnap com controles, evento de WMS, EDI, portal ou canal oficial. Quando o destino não coopera, o SILD reduz o escopo.

Symmetry não pertence ao MVP-0.

### 8.7 SILD G2 Lite — Pallet Snap

Adiciona granularidade por pallet, gaiola, roll container ou volume crítico. É aplicável quando a dor principal não está apenas na integridade do baú ou carreta, mas em glosas, faltas, avarias, inversões de SKU e disputas internas à unidade de transporte.

G2 Lite não pertence ao MVP-0. Entra depois que o gesto de origem e o vínculo com glosa provarem valor.

### 8.8 SILD Proof

Gera certificado probatório de custódia para operações logisticamente elegíveis, com origem e destino suficientemente controlados, atores identificados, lacres vinculados, eventos coerentes, PACC válido, evidência independente e granularidade compatível com a promessa.

### 8.9 SILD Reconciliation

Gerencia exceções, falhas técnicas, mídia cega, ausência de geolocalização, divergências, evidências compensatórias e reconciliação assíncrona sem apagar a falha original.

### 8.10 SILD Intelligence

Camada futura, aplicada apenas após volume, governança e base jurídica. Mede padrões recorrentes de baixa qualidade probatória em rotas, nós logísticos, transportadoras, operadores, veículos, dispositivos, docas e destinos.

A ordem correta de construção é:

> **auditoria de saída → dossiê de regresso → captura atestada → simetria → granularidade → reconciliação avançada → inteligência de rede.**

## 9. Função central · [BASE]

A função central do SILD é criar uma trilha auditável de custódia logística e classificar a qualidade dessa trilha.

O sistema busca responder:

- se a operação possui estrutura mínima para produzir evidência;
- qual manifesto ou documento foi associado à saída;
- qual veículo ou unidade logística assumiu a operação;
- qual lacre foi vinculado ao evento;
- se a carga saiu com fechamento físico registrado;
- quem capturou a evidência;
- qual dispositivo produziu a evidência;
- se a captura ocorreu em sessão controlada;
- qual âncora física ou ambiental validou o local;
- onde e quando a evidência foi registrada;
- se a chegada foi confirmada por ator independente;
- se houve divergência de lacre, placa, manifesto, pallet, destino ou unidade logística;
- se a mídia capturada é nítida, cega, incompleta ou insuficiente;
- se a prova é forte, limitada, incompleta ou contraditória;
- se a operação precisou de reconciliação;
- quais evidências compensatórias foram usadas;
- quais limites probatórios permanecem.

O produto inicial não é uma acusação e não é uma liberação automática. É um **dossiê mínimo de custódia**. Nas operações G2 Lite, esse dossiê passa a incluir identidade de pallet, face observável, fechamento do stretch, etiqueta duplex e estado físico externo da unidade logística intermediária.

## 10. SILD Origin Snap · [MVP-0 → ALVO]

O **SILD Origin Snap** é o modo inicial do SILD. Ele registra o estado físico e documental da custódia no momento de saída da carga.

Sua finalidade é provar, com baixo atrito, que determinada carga saiu de uma origem controlada associada a um manifesto, veículo, unidade logística e lacre.

O Origin Snap não prova entrega.

O Origin Snap não prova conteúdo interno.

O Origin Snap não depende de app no celular do motorista.

O Origin Snap não fotografa o rosto do motorista no MVP.

O Origin Snap não exige integração com TMS, ERP ou GR para rodar o piloto.

O Origin Snap deve ser executado por operador do pátio, conferente, lacrador, portaria ou agente autorizado do embarcador.

A regra é:

> **Motorista terceirizado não é usuário do SILD. Ele é parte observada da operação por meio dos ativos físicos que conduz.**

O Origin Snap pode operar em dois modos.

### Origin Snap Basic

Registra manifesto, placa traseira ou unidade logística, lacre, fechamento físico e contexto traseiro.

É adequado para operações de baixo e médio risco, cargas lacradas como unidade única e pilotos que precisam validar o gesto mínimo de captura.

### Origin Snap Plus

Adiciona metadados de maior criticidade, como cavalo mecânico, portaria, balança, OCR de cancela, GR, câmera fixa ou evento externo de saída.

É indicado para cargas visadas, eletrônicos, fármacos, químicos sensíveis e operações em que a tração ou troca de cavalo mecânico seja risco relevante.

A regra é:

> **Em carga visada, a unidade de carga é o objeto principal, mas o cavalo mecânico é metadado crítico de continuidade operacional.**

## 11. Objeto do Origin Snap · [MVP-0 → ALVO]

Na arquitetura-alvo, o Origin Snap pode registrar:

- operação;
- manifesto, DANFE ou documento equivalente;
- placa traseira da carreta ou unidade logística;
- lacre instalado;
- integridade física observável do lacre;
- porta ou baú fechado;
- origem;
- destino esperado;
- transportadora;
- operador do pátio;
- dispositivo de captura;
- sessão PACC Lite;
- âncora de ambiente, quando disponível;
- horário de servidor ou hub local;
- horário local declarado;
- local de origem;
- hash da mídia;
- frames congelados;
- clipe auxiliar curto;
- status da saída.

No MVP-0, esse conjunto é reduzido a documento, lacre, foto aproximada do lacre, foto de contexto traseiro, usuário, horário, hash simples e vínculo com NF, pedido ou manifesto.

A presença do motorista é consequência operacional do veículo liberado, não raiz de confiança do sistema.

O SILD observa ativos logísticos, não rostos de terceiros.

## 12. Entrada de dados sem gargalo de TI · [MVP-0]

O SILD não deve exigir integração com TMS, ERP, WMS ou GR para rodar o piloto.

A operação inicial pode ser criada por:

- leitura do código de barras do DANFE ou manifesto com leitor USB comum;
- leitura de QR ou código do documento;
- upload simples de CSV;
- seleção manual de destino e transportadora por lista curta;
- colagem de chave ou ID apenas como fallback;
- API apenas em fase posterior.

A entrada manual deve ser minimizada porque placas, números de lacre e chaves de documentos longas são fontes frequentes de erro operacional.

A regra é:

> **O SILD não deve comparar captura física contra dado digitado manualmente como se o dado digitado fosse verdade superior.**

OCR é conveniência, não raiz de verdade. A raiz mínima de identificação deve ser leitura direta de identificador físico robusto: QR, NFC, código de barras, serial curto ou lacre de alta legibilidade.

O lacre deve ser preferencialmente vinculado no pátio, no momento físico da lacração, por leitura direta do lacre instalado.

O MVP não deve depender de OCR heroico sobre caracteres pequenos, metálicos, sujos, reflexivos ou desgastados.

## 13. Níveis de captura: C0, C1 e C2 · [MVP-0 → ALVO]

A captura deve ocorrer com o menor número possível de gestos e deve respeitar a realidade do pátio: sol, chuva, ruído, EPI, pressa, fila, baixa conectividade e operadores sob carga operacional.

O erro de produto é obrigar o ciclo zero a operar como se já fosse captura probatória completa. Por isso, o SILD separa níveis de captura.

### C0 — Captura simples de auditoria

É o padrão do MVP-0.

Fluxo:

1. operador abre a operação por NF, pedido, manifesto ou lista curta;
2. captura uma foto aproximada do lacre;
3. captura uma foto de contexto traseiro da unidade logística;
4. confirma a saída;
5. o sistema salva mídia, hash, operador, horário, documento e lacre.

C0 não implementa Confiança Zero plena. Não deve ser vendido como captura antifraude forte. Sua função é organizar evidência operacional para dossiê posterior.

### C1 — Captura guiada leve

É o primeiro avanço após validação do MVP-0.

Pode incluir:

- validação simples de foco e iluminação;
- leitura de QR ou serial curto;
- câmera direta pelo app;
- bloqueio de galeria quando tecnicamente viável;
- hash e metadados de sessão.

### C2 — Captura híbrida assistida

É o padrão da arquitetura-alvo, não do MVP-0.

A captura híbrida assistida usa frames congelados em alta resolução dentro de uma sessão viva, acompanhados por clipe auxiliar curto de baixa resolução.

Fluxo C2:

1. Operador abre a viagem no app pelo manifesto, placa ou lista de operações pendentes.
2. O app inicia sessão PACC Lite e obtém desafio efêmero do servidor ou do hub local.
3. O operador aponta a câmera para a placa traseira ou unidade logística.
4. O app exige congelamento de aproximadamente 1 segundo para capturar frame nítido.
5. O operador aproxima a câmera do lacre ou QR/NFC.
6. O app exige novo congelamento para leitura e auditoria visual.
7. O operador enquadra a porta, baú ou fechamento físico em plano de contexto.
8. O app exige congelamento final e salva clipe auxiliar de continuidade.
9. O operador confirma saída.

A prova primária são os frames congelados. O clipe auxiliar apenas demonstra continuidade contextual entre os enquadramentos.

Metas de desempenho devem ser tratadas como hipóteses de piloto, não como promessa comercial inicial:

- no MVP-0, medir apenas se a captura não trava a fila; o MVP-0 não é avaliado por p50/p95 (ver seção 71);
- a partir dos ciclos com captura atestada, medir p50 e p95 numa semana de linha de base;
- buscar p50 abaixo de 25 segundos apenas após estabilização do fluxo;
- buscar p95 abaixo de 60 segundos no início desses ciclos;
- reduzir p95 após ajuste de processo, treinamento, lacres legíveis e âncoras locais.

O SILD não sobrevive se virar ritual burocrático.

## 14. SILD Snap App completo — fase futura (MVP-1) · [ALVO]

O **SILD Snap App completo** pertence ao MVP-1, não ao MVP-0.

No MVP-0, a captura pode ser feita por interface simples de captura C0: operação, foto aproximada do lacre, foto de contexto traseiro, usuário, horário, hash simples e vínculo com NF, pedido ou manifesto. O MVP-0 não exige PACC Lite, clipe auxiliar, congelamento assistido, bloqueio robusto de galeria ou âncora técnica de ambiente.

No MVP-1, o Snap App passa a ser o aplicativo de captura controlado pelo SILD, preferencialmente em aparelho corporativo do pátio ou do CD, não no celular pessoal do motorista.

Características do Snap App completo:

- login do operador ou turno;
- seleção de viagem pendente;
- câmera direta pelo app;
- bloqueio de upload de galeria quando tecnicamente viável;
- captura guiada leve ou captura híbrida assistida;
- frames congelados de alta resolução;
- clipe auxiliar curto;
- leitura de QR, NFC, código de barras ou OCR quando possível;
- confirmação visual assistida;
- fila local para falhas de conexão;
- sincronização posterior;
- assinatura local do pacote quando disponível;
- registro de dispositivo;
- hash de mídia;
- timestamp de servidor ou hub local quando disponível;
- registro de âncora de ambiente quando disponível.

O app deve guiar o operador, não transformá-lo em perito.

O operador não declara integridade plena. Ele produz mídia estruturada para que o sistema, a auditoria ou a reconciliação classifiquem a força da evidência.

A regra é:

> **MVP-0 captura evidência simples. MVP-1 começa a controlar a sessão de captura.**

## 15. PACC Lite — Pacote de Atestação Contextual de Captura · [ALVO]

O **PACC Lite** é o pacote mínimo de atestação contextual da captura na arquitetura-alvo. Ele não é requisito do MVP-0.

Sua função é impedir que o evento dependa apenas da declaração do operador ou de uma foto isolada. O pacote combina desafio efêmero, câmera direta, bloqueio de galeria, frames congelados, hash de mídia, metadados de dispositivo, operador, horário, âncora física do local e leitura verificável do lacre ou unidade logística.

Componentes da arquitetura-alvo:

- nonce ou desafio efêmero;
- câmera direta pelo app;
- bloqueio de upload de galeria;
- frames congelados em alta resolução;
- clipe curto auxiliar;
- hash dos arquivos;
- ID do operador;
- ID do dispositivo;
- versão do app;
- timestamp local;
- timestamp de servidor ou hub local;
- âncora de ambiente;
- status de conectividade;
- reason codes;
- resultado de leitura do QR, NFC, código de barras ou OCR assistido.

Componentes opcionais, não bloqueantes:

- assinatura local do pacote;
- atestação nativa do sistema operacional;
- chave protegida por hardware;
- detecção básica de integridade do dispositivo;
- análise visual simples;
- comparação automática origem-destino.

O PACC Lite não transforma o smartphone em equipamento forense absoluto. Ele aumenta a força da captura ao demonstrar que a evidência foi produzida em uma sessão viva, por dispositivo conhecido, em ambiente compatível e vinculada a um objeto logístico verificável.

No MVP-0, o equivalente operacional é muito mais simples: captura C0, hash de mídia, operador, horário, documento e vínculo com lacre. Essa evidência é útil para auditoria e regresso, mas não deve ser vendida como Confiança Zero plena.

A regra é:

> **MVP-0 organiza evidência. MVP-1 começa a atestar captura. MVP-2 aumenta força probatória.**

## 16. Fora do MVP-0 · [MVP-0]

O MVP-0 deve evitar vaidade tecnológica e falsos positivos operacionais.

Ficam fora do MVP-0:

- PACC Lite obrigatório;
- SILD Hub;
- G2 Lite;
- PIP Duplex Lite;
- Pallet Registry;
- WebSnap;
- Symmetry obrigatória;
- Fast Track;
- Mesa Humana formal;
- RPI completa com ciclo de vida;
- cold storage automatizado;
- Storage Lifecycle Manager;
- EDI obrigatório;
- API;
- integrações com marketplace;
- parser de múltiplos layouts de glosa;
- análise decisória por acelerômetro ou giroscópio;
- uso de IMU como prova de continuidade óptica;
- IA local pesada para detectar maquete, tela ou fraude óptica sofisticada;
- inferência automática de fraude por movimento anômalo;
- assinatura criptográfica obrigatória baseada em hardware seguro universal;
- microvídeo contínuo pesado como prova principal;
- sensores premium obrigatórios;
- rede de inteligência;
- score de operadores;
- blacklist;
- bloqueio financeiro automático;
- "Confiança Zero" como linguagem comercial;
- mapper visual de planilhas;
- parser nativo de layout de marketplace;
- reconciliação manual de glosa em tela;
- OCR avançado;
- IA de imagem ou IA de legibilidade de foto;
- auditoria visual em tempo real;
- leitura prévia de lacre como vínculo probatório;
- troca obrigatória de lacre metálico já travado;
- homologação obrigatória de novo lacre para o piloto.

Acelerômetro, giroscópio e sinais de movimento podem ser pesquisados em fase futura, mas não devem impactar status operacional no MVP.

A regra é:

> **No ciclo zero, o app deve capturar evidência simples e gerar dossiê; não tentar julgar a cadeia logística inteira.**

## 17. Classes de dispositivo · [ALVO]

O SILD deve classificar dispositivos conforme sua força técnica, sem presumir que todo aparelho corporativo possui hardware seguro.

### D0 — Dispositivo não confiável

Sem gestão corporativa, integridade desconhecida, alto risco. Não deve operar piloto forte.

### D1 — Dispositivo registrado

ID conhecido, app instalado, operador autenticado, sem garantia forte de hardware.

### D2 — Dispositivo gerenciado

MDM, app controlado, bloqueio de galeria, logs, políticas mínimas de segurança e rastreabilidade.

### D3 — Dispositivo atestado

Atestação de integridade disponível, chave protegida quando suportada e ambiente menos vulnerável.

### D4 — Hub ou coletor dedicado

Hardware controlado em doca, pátio ou portaria, com emissão local de desafio, ancoragem física e controle operacional superior.

A regra é:

> **A ausência de hardware seguro não invalida a operação; apenas reduz a classe técnica da captura e exige compensação por ambiente, lacre, destino ou reconciliação.**

## 18. Smartphone como coletor oportunístico · [BASE]

O smartphone é tratado como coletor oportunístico, não como raiz absoluta de confiança.

Na arquitetura-alvo, a força da captura aumenta quando o dispositivo é corporativo, autenticado, online e associado a um ponto controlado. A força diminui quando o evento é offline, quando há falha de leitura, quando a mídia é ruim, quando há divergência ou quando o ator não é independente.

O smartphone pode:

- capturar mídia;
- ler QR ou OCR;
- registrar metadados;
- assinar pacote localmente quando possível;
- guiar o operador;
- enviar evidência ao servidor.

O smartphone não deve, sozinho, definir a classe final da cadeia probatória.

A regra é:

> **A classe da mídia mede a força da captura. A classe da cadeia mede a força da custódia.**

## 19. SILD Hub e âncoras de ambiente · [ALVO]

O **SILD Hub** é parte da arquitetura-alvo, não requisito do MVP-0.

O modo offline existe para preservar o fluxo operacional, não para preservar força probatória máxima sem contexto. Na operação brasileira, pátios cobertos por telhas metálicas, docas afastadas e zonas industriais com conectividade instável não devem ser tratados como exceção rara.

No MVP-0, a âncora deve ser **software-first** e de baixo atrito.

### Âncora S0 — Registro simples

Operador, documento, lacre, mídia, horário de servidor e operação vinculada.

### Âncora S1 — Software contextual

Pode incluir geofence quando disponível, rede conectada, IP corporativo, dispositivo conhecido, local selecionado, histórico de operação e horário de servidor.

### Âncora S2 — Rede corporativa

Wi-Fi controlado, MDM, estação conhecida ou dispositivo gerenciado.

### Âncora S3 — SILD Hub

Beacon, QR rotativo, NFC fixo, gateway local, roteador configurado, tablet de doca ou mini-servidor.

### Âncora S4 — Infraestrutura dedicada

Portaria, cancela, balança, câmera fixa, OCR local, WMS de doca ou integração física de pátio.

### Offline esperado

Ocorre em pátio previamente conhecido como zona de baixa conectividade, com dispositivo registrado, operador autenticado, sequência local íntegra, âncora de ambiente detectada e sincronização posterior dentro da janela configurada.

Pode receber o status:

> **Saída Validada Localmente — Sincronizada**

### Offline anômalo

Ocorre quando há dispositivo desconhecido, sequência quebrada, atraso excessivo, reboot suspeito, ausência de âncora, mídia incoerente, operação incompatível ou sincronização tardia sem justificativa.

Recebe status pendente de reconciliação ou divergente conforme a materialidade.

A regra é:

> **O SILD Hub aumenta a força probatória em pátios offline; não é dependência do MVP-0.**

## 20. Tempo local, reboot e reconciliação técnica · [ALVO]

O SILD não deve confiar cegamente no relógio local do smartphone.

O app deve registrar sinais técnicos auxiliares:

- horário local declarado;
- último horário de servidor ou hub local conhecido;
- delta entre relógio local e servidor na última sincronização;
- índice incremental local de eventos;
- identificador do dispositivo;
- ocorrência de reboot quando detectável;
- sequência de capturas;
- horário real de recebimento no servidor;
- hash de mídia;
- operação vinculada;
- âncora de ambiente detectada;
- status de conectividade;
- motivo de sincronização tardia.

O tempo monotônico do sistema pode resetar após reinicialização do aparelho. Por isso, o app deve manter um estado local persistente e um indexador próprio de eventos. Se houver reboot, o servidor deve tratar como evento técnico a reconciliar, não como fraude automática.

O desafio pré-gerado offline não deve ser vendido como anti-replay forte sem ambiente confiável de tempo e atestação. Quando houver SILD Hub, o desafio local aumenta a força da sessão, mas continua sendo parte de um conjunto probatório, não prova absoluta.

---

# PARTE III — OBJETO FÍSICO E SIMETRIA

## 21. Lacre verificável · [BASE/MVP-0]

O lacre é componente de continuidade, não prova de pureza da carga.

Sua função é vincular o evento de origem ao fechamento físico do veículo, pallet, contêiner, caixa ou unidade logística.

O lacre pode incluir:

- número único;
- QR code de alto contraste;
- NFC opcional;
- lote;
- vínculo com manifesto;
- vínculo com veículo;
- vínculo com evento de origem;
- evidência de violação;
- comparação origem-destino;
- controle de reutilização;
- registro de ruptura, substituição ou divergência.

O lacre não prova que o conteúdo é lícito. Ele prova continuidade externa após o fechamento, dentro dos limites do próprio lacre.

O SILD distingue dois estados:

### Lacre identificado

QR, NFC, serial ou código do lacre foi lido e associado à operação.

### Integridade física do lacre observada

A zona mecânica de fechamento foi capturada: pino, cordoalha, haste, fecho, encaixe, ponto destrutível ou região de ruptura.

A regra é:

> **QR intacto não prova lacre íntegro se a zona mecânica de fechamento não foi observada.**

A categoria correta para muitos eventos será:

> **origem logisticamente coerente, cadeia externa preservada, conteúdo interno não certificado.**

## 22. Níveis de lacre por fase · [MVP-0 → ALVO]

O SILD deve operar com níveis de lacre proporcionais ao risco, ao valor protegido e à granularidade da operação.

### Nível 1 — Lacre operacional serializado revisado

Número único, QR grande, alto contraste, número curto humano, lote e controle de reutilização. Serve para vínculo operacional, leitura rápida e registro básico.

É o nível padrão do MVP-0.

No MVP-0, o lacre Nível 1 é usado para registrar a saída e compor o dossiê de defesa ou regresso. Não há comparação obrigatória com destino. O MVP-0 **aceita o lacre que o cliente já usa**; não exige homologação de novo insumo nem troca de lacre para começar o piloto.

#### Vínculo de lacre fisicamente realista no MVP-0

O elo mais frágil do C0 não é a qualidade da foto. É a ausência de prova de que **o lacre registrado é o lacre que efetivamente viajou** vinculado àquele documento. Por isso o MVP-0 estrutura o vínculo de lacre com cuidado — mas de forma compatível com a realidade do pátio, onde o lacre frequentemente já chega travado, o QR metálico reflete e a leitura nem sempre é possível.

A regra realista é:

> **No MVP-0, o serial do lacre deve ser preferencialmente lido por identificador físico robusto (QR, código de barras ou NFC) no ponto físico de fechamento. Quando a leitura não for possível, admite-se fallback manual controlado, com `manual_seal_entry` e foto aproximada obrigatória, rebaixando o teto probatório. O vínculo nasce no fechamento, nunca antes.**

Os princípios que tornam esse vínculo honesto e implementável:

- **O vínculo nasce no ponto físico de fechamento.** O evento `seal_bound` só é gerado quando o lacre já está instalado na unidade logística. Pré-leitura — escanear o lacre antes de aplicá-lo — **não** gera vínculo probatório, porque um lacre lido no balcão pode acabar em outra carga. Tentativa de leitura fora do fluxo de fechamento é registrada como `invalid_pre_scan_blocked` e não vincula.
- **Aceitar o lacre existente.** O piloto usa o lacre que o cliente já tem. Lacre dual-readable (QR + serial humano legível) é **recomendação de evolução**, não requisito de piloto.
- **Não obrigar troca de lacre já travado.** Se a leitura automática falhar com o lacre mecanicamente travado, não se exige romper e substituir o lacre. Cai-se para `manual_seal_entry` ou, se nem o serial for legível, `seal_not_verified`. A rejeição e troca de lacre só é permitida **antes** do travamento mecânico.
- **Dupla digitação reduz erro de digitação, não eleva força probatória.** Pedir o serial duas vezes é controle de typo opcional; não muda o teto.
- **Foto aproximada obrigatória em toda contingência manual.** Quando o serial é digitado, a foto aproximada do lacre passa a ser obrigatória, para permitir auditoria visual posterior sob demanda.
- **Captura contra reflexo metálico.** A instrução de captura deve orientar o operador a mitigar reflexo: sem flash, distância de aproximadamente 20 cm, ângulo que evite brilho especular.

O que o vínculo de lacre do MVP-0 **não** promete: não prova integridade mecânica sofisticada, não prova chegada, não substitui Symmetry e não impede conluio de origem. Ele prova, dentro de seus limites, que aquele lacre foi associado àquele documento naquela origem, naquele horário, por aquele operador — suficiente para sustentar regresso e instrução de sinistro.

#### Fluxo do app de pátio no MVP-0

1. **Abrir operação** por NF, pedido ou manifesto.
2. **Ir para fechamento.** O app orienta o operador a estar fisicamente no ponto de lacração.
3. **Leitura do lacre.** A câmera de leitura abre apenas na etapa de fechamento.
4. **Bloqueio de pré-scan.** Tentativa fora do fluxo de fechamento não gera `seal_bound` (`invalid_pre_scan_blocked`).
5. **Leitura OK.** Salva método, serial, mídia e status pleno.
6. **Leitura falha.** Libera contingência manual com um botão único: "Digitar código manual — lacre instalado". O app não pergunta "lacre travado ou não travado".
7. **Entrada manual.** Exige serial digitado e foto aproximada obrigatória.
8. **Dupla digitação.** Opcional, como controle de typo; não aumenta o teto.
9. **Foto aproximada.** Obrigatória; a auditoria visual ocorre depois, sob demanda.
10. **Foto de contexto.** Obrigatória para concluir a evidência mínima.
11. **Saída confirmada.** O sistema salva hash, operador, horário, reason code e teto probatório.

A leitura não permite modo em lote, para preservar o vínculo um-a-um entre lacre e operação.

#### Matriz de estados de lacre do MVP-0

| Cenário | `seal_bind_method` | `seal_bind_stage` | `manual_entry_visual_support` | `probative_ceiling` | Ação |
| --- | --- | --- | --- | --- | --- |
| QR/código/NFC lido no ponto de fechamento | `qr_read` / `barcode_read` / `nfc_read` | `post_lock_installed` | `not_applicable` | `origin_evidence_registered` | Dossiê automático |
| Leitura falhou, serial digitado, foto ainda não auditada | `manual_entry` | `post_lock_installed` | `not_yet_audited` | `origin_evidence_registered_with_observation` | Dossiê com ressalva |
| Serial digitado, auditoria posterior confirma foto nítida | `manual_entry` | `post_lock_installed` | `serial_visible_in_photo` | `origin_evidence_registered_with_observation` | Dossiê mantém ressalva |
| Serial digitado, auditoria posterior acha foto parcial | `manual_entry` | `post_lock_installed` | `serial_partially_visible` | `origin_evidence_registered_with_observation` ou `origin_evidence_incomplete` | Decisão humana pós-glosa |
| Serial digitado, foto cega | `manual_entry` | `post_lock_installed` | `serial_not_visible` | `origin_evidence_incomplete` | Dossiê fraco |
| Pré-escaneamento | bloqueado | `invalid_pre_scan` | `not_applicable` | nenhum | Não gera `seal_bound` |
| Sem leitura, sem serial, sem foto útil | `not_verified` | `post_lock_installed` | `serial_not_visible` | `origin_evidence_incomplete` | Evidência incompleta |

A regra de vínculo é:

> **Pré-leitura não vincula lacre à operação. Só leitura automática ou entrada manual no ponto físico de fechamento pode gerar vínculo de lacre.**

### Nível 2 — Lacre destrutível com evidência visual

Inclui material que demonstra rompimento, foto do lacre instalado, captura da zona mecânica de fechamento, comparação origem-destino e controle de lote.

O Nível 2 completo pertence ao MVP-1/MVP-2, quando houver captura atestada ou Symmetry. No MVP-0, pode-se capturar visualmente a zona mecânica do lacre, mas sem prometer comparação origem-destino.

### Nível 3 — Lacre antifraude reforçado

Pode incluir NFC, QR assinado, padrão físico não trivial, microelemento visual, embalagem controlada e auditoria amostral.

Pertence a ciclos posteriores ou a operações especiais de maior risco.

### Nível 4 — Lacre ou dispositivo testemunha premium

Pode incluir sensor de abertura, luz, movimento, choque, permanência ou ruptura. É aplicável apenas a cargas críticas.

A regra por fase é:

- **MVP-0:** Nível 1 revisado, com captura simples de lacre e contexto.
- **MVP-1:** Nível 1 revisado ou Nível 2 parcial, com captura atestada.
- **MVP-2:** Nível 2 completo quando houver origem-destino ou granularidade maior.
- **MVP-3:** Nível 3 ou Nível 4 para operações críticas.

A regra é:

> **O lacre do MVP-0 deve ser desenhado para leitura operacional, não para exigir OCR heroico ou comparação de destino inexistente.**

## 23. PIP Duplex Lite — padrão físico do G2 Lite · [ALVO]

O **PIP Duplex Lite — Pallet Integrity Pattern** é o padrão físico mínimo de integridade do SILD G2 Lite.

Sua função não é tornar o pallet inviolável, nem provar conteúdo interno caixa a caixa. Sua função é criar uma unidade logística intermediária com identidade dupla observável, fechamento mínimo verificável e baixo custo de aplicação em operação de alto volume.

A regra é:

> **O G2 Lite não duplica lacração; duplica observabilidade.**

O kit físico padrão do PIP Duplex Lite deve conter:

- **Etiqueta A principal**, com QR grande, Pallet ID, número curto humano e identificação da operação ou lote;
- **Etiqueta B espelho**, menor, com o mesmo Pallet ID e marcação de face alternativa;
- **trava de emenda do stretch**, aplicada sobre a emenda final da envelopagem;
- cartela única para aplicação rápida;
- mesmo identificador lógico entre A, B e trava;
- controle de lote do insumo;
- leitura por QR, código de barras, NFC opcional ou serial curto;
- vínculo com NF, pedido, manifesto, romaneio, pallet, gaiola, roll container ou volume crítico.

A etiqueta B não deve ficar no vinco da quina. A quina é zona de raspagem, impacto e atrito durante carregamento, vibração e transporte. A etiqueta B deve ficar na face lateral adjacente, recuada aproximadamente 10 a 15 centímetros da quina, protegida na superfície plana do stretch ou da unidade logística.

A etiqueta B existe para permitir fechamento por face alternativa quando o pallet gira 90 ou 180 graus durante movimentação, carregamento ou descarga. O app deve aceitar captura da face A ou da face B, desde que o Pallet ID seja compatível e a face observada pertença ao mesmo kit físico.

A trava de emenda não deve ser rígida, quebradiça ou sensível à vibração normal. O stretch film é elástico e se acomoda durante transporte rodoviário. A trava correta deve ser flexível à movimentação do filme, mas intolerante ao descolamento.

Especificação física recomendada para a trava de emenda:

- filme flexível, como polipropileno, polietileno ou material equivalente;
- adesivo agressivo de cura rápida;
- resistência à vibração e dilatação térmica comuns;
- deformação aceitável sem ruptura por fadiga normal;
- comportamento destrutivo em tentativa de remoção;
- descolamento que rasgue, marque ou deforme o próprio stretch;
- incompatibilidade visual com reposicionamento limpo.

A regra é:

> **A trava de emenda deve sobreviver à elasticidade do transporte, mas deixar rastro em tentativa de abertura.**

O PIP Duplex Lite pode operar em dois modos.

### G2 Lite Standard

A origem captura a face visível, a etiqueta A ou B e a emenda/trava quando acessível. O destino pode fechar por qualquer face válida A ou B.

É o modo padrão para alto volume e baixo atrito.

### G2 Lite Plus

A origem captura A e B antes do carregamento, quando o pallet ainda está no staging ou em área acessível. O destino pode fechar por qualquer face válida A ou B.

É indicado para carga de maior risco, glosa recorrente ou cliente estratégico.

Se nenhuma face A/B estiver visível no baú antes da descarga, o sistema deve registrar:

> **Face indisponível no veículo. Captura realizada após descarga com observação de custódia.**

A captura após descarga pode ser aceita, mas não deve receber o mesmo teto probatório de uma captura feita com face válida visível ainda na traseira do veículo ou imediatamente no ponto de abertura. O status correto é observacional, não plena conclusão sem ressalva.

### Classe de carga e PIP recomendado

| Classe de carga | PIP recomendado | Uso esperado |
| --- | --- | --- |
| Baixo valor e alto volume | Etiqueta A + etiqueta B simples | Identidade duplex de baixo custo |
| Médio risco ou glosa frequente | A + B + trava de emenda | G2 Lite padrão |
| Alto valor ou furto recorrente | A + B + trava + reforços frontais | G2 Lite Plus ou operação assistida |
| Crítico | PIP completo, NFC, auditoria amostral e possível captura A/B obrigatória | Operação especial |

Pontes de canto, fitas tamper-evident longas, microtextos caros e sensores não devem ser obrigatórios no G2 Lite padrão. Eles pertencem a classes de risco superiores.

#### Economia do insumo: custo-alvo confrontado com a margem

Uma afirmação de que o PIP Duplex Lite é "econômico" não é falsificável sem um número. O insumo físico é aplicado por unidade logística; em carga de baixo valor e alto volume, um insumo caro por pallet pode consumir a margem inteira da operação e inviabilizar o G2 Lite na prática.

Por isso o desenho do kit deve obedecer a um **custo-alvo por pallet** explícito, tratado como restrição de projeto, não como detalhe posterior:

- **G2 Lite Standard (A + B + trava de emenda):** o custo do kit por pallet deve ser uma fração pequena do valor médio em disputa por pallet naquela operação. A diretriz de projeto é que o insumo fique em uma faixa de centavos a poucas unidades de real por pallet, e que o **custo do kit não ultrapasse uma fração de um dígito percentual do valor médio glosado por pallet**. Acima disso, a economia do G2 Lite não fecha para alto volume.
- **G2 Lite Plus (com reforços):** admite custo maior por pallet, justificado por glosa recorrente, alto valor ou cliente estratégico, onde o valor em disputa por pallet é alto o suficiente para absorver o insumo com folga.
- **PIP completo / NFC / sensor:** premium por definição; só se justifica quando o valor protegido por unidade torna o custo do insumo irrelevante frente ao risco.

A regra econômica é:

> **O insumo do G2 Lite padrão só é viável se custar uma fração pequena do que ele protege. Se o kit por pallet se aproxima do valor médio glosado por pallet, a operação não é candidata a G2 Lite — é candidata a G1 documental ou a elevação de granularidade só nas SKUs ou rotas que concentram a perda.**

Em consequência, a decisão de aplicar G2 Lite deve partir de dois números do cliente, levantados na linha de base do piloto: **valor médio em disputa por pallet** e **frequência de glosa por pallet naquela rota/cliente**. Sem esses dois números, o G2 Lite é hipótese, não recomendação.

O custo relevante não é só o do material. É o **custo total de aplicação**: insumo mais o tempo de operador para aplicar A, B e trava, mais o impacto na cadência da doca. Por isso:

- a cronoanálise do PIP (tempo p50/p95 de aplicação por pallet) é trabalho de **P1 analítico**, não do MVP-0;
- o kit físico só deve ser desenhado **depois** de medir a cadência real da doca;
- o roadmap deve posicionar um **modelo "valor protegido vs fricção de doca"** antes de qualquer PIP físico;
- as métricas futuras incluem tempo p50/p95 de aplicação de PIP;
- critério de inviabilidade: **se o tempo de aplicação do PIP quebrar a cadência da doca, o G2 Lite não é elegível** naquela operação, por melhor que seja a economia de material.

A regra é:

> **O PIP completo é premium. O PIP Duplex Lite é o padrão econômico de campo — desde que seu custo total de aplicação permaneça uma fração pequena do valor que protege e não quebre a cadência da doca.**

## 24. SILD Symmetry · [ALVO]

O **SILD Symmetry** é a fase que adiciona observação de destino ao Origin Snap, formando simetria origem-destino.

A simetria aumenta a força probatória porque compara o estado da carga na saída com o estado observado na chegada.

A regra é:

> **Sem observação independente no destino, não há simetria probatória forte.**

O SILD Symmetry deve ser aplicado quando houver destino próprio ou destino terceiro cooperativo.

## 25. Destino próprio · [ALVO]

No MVP-0, o destino próprio pode existir na operação real, mas não é requisito do produto.

Quando o destino é próprio, controlado ou pertencente à mesma organização do embarcador, o padrão deve ser o **SILD Snap App autenticado**.

Não se deve usar WebSnap anônimo em ambiente próprio.

O destino próprio deve registrar:

- conferente ou turno logado;
- aparelho corporativo;
- geolocalização do ponto;
- placa traseira ou unidade logística;
- lacre na chegada;
- condição do lacre;
- horário;
- comparação com origem.

A regra é:

> **Quanto maior o controle sobre o destino, menor a tolerância a evidência anônima.**

## 26. Destino terceiro cooperativo · [ALVO]

No MVP-0, destino cooperativo não é requisito.

Destino terceiro cooperativo pode usar WebSnap, app autenticado, portal, PIN, e-mail corporativo, API, WMS ou confirmação por canal oficial.

A força probatória depende de:

- geolocalização;
- canal oficial;
- independência do ator;
- dispositivo usado;
- prazo do evento;
- evidência visual;
- coerência com rota e horário.

O destino terceiro não precisa começar com integração pesada. Mas, sem ator independente e contexto válido, não deve fechar prova forte.

## 27. Destino não cooperativo · [MVP-0/ALVO]

No MVP-0, destino não cooperativo apenas confirma que o produto deve limitar-se à evidência de origem e ao Claim Intake posterior.

Destino não cooperativo não destrói o SILD. Ele apenas reduz o escopo.

Quando o destinatário não aceita app, WebSnap, confirmação oficial, leitura de lacre ou qualquer colaboração mínima, o sistema pode emitir relatório de evidência parcial.

Esse relatório pode comprovar bem a saída, mas não deve afirmar simetria forte de chegada.

A regra é:

> **Destino não cooperativo impede prova forte de chegada; não invalida a evidência de origem.**

## 28. QR do lacre e QR de recebimento · [ALVO]

A distinção entre QR de lacre e QR de recebimento pertence principalmente a ciclos com Symmetry. No MVP-0, usa-se apenas o QR ou serial do lacre quando disponível.

O SILD distingue dois tipos de QR.

### QR do lacre

Identifica lacre, operação ou unidade logística. Pode viajar com a carga porque pertence ao objeto físico lacrado.

### QR de recebimento

Ativa evento de destino. Não deve viajar com a carga.

O QR de recebimento deve ser:

- ativo fixo da doca, portaria ou local de recebimento;
- token gerado pelo sistema do destino;
- link enviado por canal oficial;
- código temporário emitido na abertura da janela de descarga;
- credencial associada ao recebedor ou ao local.

A regra é:

> **QR de recebimento não pode viajar com a carga.**

Se o mesmo QR que está com o motorista permite fechar entrega, o motorista possui chave suficiente para simular recebimento.

## 29. WebSnap · [ALVO]

WebSnap não pertence ao MVP-0 e não deve ser vendido como solução para grandes marketplaces ou varejistas dominantes.

O **WebSnap** é um mecanismo leve de captura via navegador, voltado a destinos terceiros cooperativos ou parcialmente cooperativos.

Ele não é o padrão para destino próprio.

O WebSnap deve exigir:

- geolocalização no momento da captura;
- câmera direta do navegador quando possível;
- bloqueio ou mitigação de upload de galeria;
- link com validade limitada;
- vínculo com operação;
- verificação de raio do destino;
- verificação de dispositivo quando possível;
- detecção de uso por aparelho associado ao motorista;
- registro de IP, horário e metadados disponíveis.

Sem localização válida, o WebSnap não fecha o evento de destino.

Foto perfeita sem contexto válido é anexo visual, não evento de recebimento.

## 30. Objeto, evento e ator · [BASE]

O SILD avalia cada evidência em três dimensões:

### Objeto

A mídia mostra o lacre, a placa, a porta, o manifesto ou a unidade logística esperada?

### Evento

A captura ocorreu no local, horário, etapa e contexto compatíveis com a narrativa logística?

### Ator

Quem produziu a evidência é independente, autorizado ou controlado pela parte correta?

A regra é:

> **Imagem valida objeto. Contexto valida evento. Ator valida independência.**

Um lacre visualmente correto fotografado fora do destino não confirma recebimento.

Uma foto feita pelo motorista não possui a mesma força de uma foto feita por conferente do destino.

Uma confirmação de TMS não possui a mesma força de uma captura física autenticada.

---

# PARTE IV — MODELO PROBATÓRIO

## 31. SILD Evidence Object — objeto probatório universal · [BASE]

O **SILD Evidence Object** é o átomo técnico do protocolo SILD.

Cada captura, confirmação, divergência, reconciliação, glosa, RPI, dossiê ou evento de custódia deve poder ser representado como um objeto probatório estruturado, ainda que nem todos os campos existam no MVP-0.

O SILD Evidence Object não é apenas uma imagem. Ele é a unidade mínima de narrativa probatória.

Campos conceituais:

- **object_type:** carga, veículo, lacre, pallet, gaiola, roll container, contêiner, caixa, documento, claim ou evento sistêmico;
- **object_identifier:** lacre, placa, NF, manifesto, Pallet ID, SSCC, pedido, operação ou identificador equivalente;
- **custody_event_type:** saída, chegada, abertura, lacração, captura, divergência, reconciliação, claim, RPI, transbordo, mutação ou encerramento;
- **actor_type:** operador de origem, conferente de destino, backoffice, sistema legado, transportadora, seguradora, auditoria ou terceiro cooperativo;
- **actor_independence:** próprio, independente, interessado, terceiro, sistêmico, anônimo ou não verificado;
- **capture_channel:** Console Web, Snap App, WebSnap, API, WMS, TMS, EDI, upload, SILD Hub, câmera fixa ou integração;
- **context:** local, horário, origem, destino, doca, geofence, IP, rede, hub, dispositivo e janela operacional;
- **media_reference:** foto, frame, clipe, documento, arquivo, evento de sistema ou anexo;
- **media_integrity:** hash, assinatura, trilha de alteração, versão, armazenamento e status de retenção;
- **device_context:** classe D0–D4, app, versão, MDM, atestação, hub ou ausência de dispositivo conhecido;
- **evidence_quality:** nítida, limitada, incompleta, cega, divergente, manual, reconciliada ou insuficiente;
- **internal_status:** classe técnica, evento interno, reason code e teto probatório;
- **external_status:** linguagem defensável exibida para operação, cliente, seguradora, auditoria ou jurídico;
- **probative_limit:** o que a evidência permite afirmar e o que ela não permite afirmar;
- **links:** evento anterior, operação, documento, lacre, claim, RPI, dossiê, reconciliação ou ledger.

No MVP-0, o SILD Evidence Object é reduzido a documento, lacre, foto do lacre, foto de contexto, hash simples, usuário, data/hora, glosa vinculada e dossiê.

Na arquitetura-alvo, o mesmo objeto se expande para PACC Lite, Symmetry, G2 Lite, RPI completa, Fast Track, Storage Lifecycle, legal hold e inteligência de rede.

A regra é:

> **O MVP pode ser simples. O objeto probatório não deve ser conceitualmente frágil.**

## 32. Estados externos por fase · [MVP-0 + ALVO]

O SILD deve separar estados do MVP-0 de estados da arquitetura-alvo. O erro de produto é apresentar estados de Symmetry, G2 Lite, Fast Track ou RPI completa como se fossem parte do ciclo zero.

### Estados externos do MVP-0

O MVP-0 deve usar poucos estados, ligados à auditoria de saída, ingestão de glosa e geração de dossiê.

#### Operação Criada

NF, pedido, manifesto ou referência operacional foi registrada.

#### Evidência de Saída Registrada

A operação possui foto do lacre, foto de contexto traseiro e vínculo documental mínimo.

#### Evidência de Saída Incompleta

Falta foto do lacre, foto de contexto, lacre vinculado ou documento mínimo.

#### Glosa Importada

Uma glosa, abatimento, chargeback ou contestação foi importada no template padrão SILD.

#### Glosa Vinculada à Evidência de Saída

A glosa foi associada a uma operação com evidência de saída registrada.

#### Glosa Sem Evidência de Origem

A glosa foi importada, mas não encontrou operação capturada correspondente.

#### RPI Lite Aberta por Claim Match

Uma ressalva documental foi aberta porque a glosa foi vinculada à evidência de saída. No MVP-0, essa RPI Lite não possui ciclo de vida completo.

#### Dossiê de Defesa/Regresso Gerado

O sistema gerou relatório factual com operação, lacre, mídia, documento, glosa e vínculo de defesa.

### Estados externos da arquitetura-alvo

Os estados abaixo pertencem a ciclos posteriores e não devem ser exigidos no MVP-0.

#### Saída Registrada

Houve captura mínima de origem, mas sem PACC completo ou sem força suficiente para validação plena.

#### Saída Validada Online

Manifesto, veículo, lacre e fechamento foram registrados corretamente na origem, em sessão validada pelo servidor.

#### Saída Validada Localmente

Manifesto, veículo, lacre e fechamento foram registrados corretamente na origem, com validação por âncora local ou SILD Hub, antes da sincronização central.

#### Saída Validada Localmente — Sincronizada

A captura ocorreu em modo offline esperado ou localmente ancorado, e foi sincronizada posteriormente com sequência íntegra e sem contradição.

#### Saída Validada com Observação

A saída foi registrada, mas houve detalhe operacional: OCR falhou, lacre foi digitado manualmente, conexão oscilou, mídia teve limitação não crítica ou houve pequena limitação técnica.

#### Saída Pendente de Reconciliação

Faltou elemento relevante, mas a operação ainda pode ser reconciliada por evidência adicional.

#### Saída Divergente

Há incompatibilidade objetiva: lacre reutilizado, lacre cancelado, placa divergente contra fonte confiável, manifesto incompatível, tentativa inválida de mídia ou contradição física relevante.

#### Custódia Concluída

Origem e destino foram registrados com contexto e ator válidos.

#### Custódia Concluída e Reconciliada

A operação foi encerrada com evidência compensatória independente, preservando registro de que o evento original teve limitação técnica.

#### Custódia Pendente

A cadeia ainda depende de evidência complementar ou análise.

#### Custódia Divergente

Há contradição relevante entre origem, destino, lacre, veículo, localização, ator ou tempo.

#### Pallet Identificado

A unidade G2 foi lida por etiqueta, QR, NFC, SSCC ou código equivalente, mas sem evidência suficiente da envelopagem.

#### Pallet Envelopado Observado

Etiqueta e stretch film foram capturados, mas sem observação suficiente do fechamento ou da trava de emenda.

#### Pallet com Fechamento Observado

Etiqueta, stretch film e emenda/trava de fechamento foram capturados.

#### Pallet com Integridade Duplex Observada

Etiqueta A ou B foi lida, a face observável foi capturada, o fechamento foi observado e não houve divergência aparente.

#### Pallet com Observação Técnica

A unidade G2 foi registrada, mas houve limitação não crítica: reflexo, baixa luz, etiqueta secundária ausente, face parcialmente obstruída ou captura após descarga.

#### Pallet Pendente de Reconciliação

Faltou elemento relevante: nenhuma face legível, mídia cega, ausência de emenda/trava, etiqueta danificada ou impossibilidade de avaliar integridade externa.

#### Pallet Face Indisponível no Veículo

Nenhuma face A/B estava acessível antes da descarga. O evento pode ser capturado após retirada do pallet, mas recebe observação de custódia.

#### Pallet Capturado Após Descarga com Observação

A unidade G2 foi identificada e registrada depois da retirada do veículo. A evidência é utilizável, mas possui teto probatório menor do que a captura feita com face válida visível no ponto de abertura.

#### Pallet Divergente

Há contradição objetiva: ID incompatível, etiqueta ausente sem explicação, stretch cortado, reembalagem aparente, trava de emenda violada, pallet diferente ou evidência conflitante.

## 33. Critérios de Custódia Concluída · [ALVO]

Custódia Concluída exige observação de origem e destino. Portanto, não é status do MVP-0.

O status **Custódia Concluída** deve ser reservado para operações em que origem e destino foram registrados com força contextual suficiente.

Critérios mínimos:

- Origin Snap válido;
- manifesto, DANFE ou documento equivalente associado;
- lacre válido, não cancelado e não reutilizado;
- placa traseira ou unidade logística capturada;
- captura de origem feita por operador autorizado;
- dispositivo corporativo ou ponto controlado na origem;
- destino registrado por app autenticado, canal independente forte ou sistema confiável do destino;
- localização compatível com origem e destino;
- horário compatível com a cronologia operacional;
- ausência de divergência relevante entre lacre, placa, manifesto, origem e destino;
- ausência de reconciliação por perda contextual essencial.

Quando houver perda contextual relevante, mesmo que depois reconciliada por evidência independente, o teto externo deve ser **Custódia Concluída e Reconciliada**.

A regra é:

> **Custódia Concluída exige continuidade observada. Custódia Reconciliada exige explicação independente da lacuna.**

## 34. Matriz de uso interno, operacional e externo · [ALVO]

Esta matriz organiza a arquitetura-alvo. No MVP-0, os estados válidos são os listados na seção 32 para auditoria de saída, glosa e dossiê.

O SILD deve separar linguagem técnica, linguagem operacional e linguagem externa.

| Evento interno | Status operacional | Status externo | Uso permitido |
| --- | --- | --- | --- |
| `origin_snap_validated` | Saída Validada | Evidência de origem registrada | Encerrar evento de saída |
| `seal_manual_entry` | Saída Validada com Observação | Saída registrada com confirmação manual | Monitorar qualidade de leitura |
| `offline_expected_local_sync` | Saída Validada Localmente — Sincronizada | Evidência capturada em modo offline esperado com âncora local e sincronização íntegra | Aceitar como validação local controlada |
| `arrival_context_missing` | Custódia Pendente | Fechamento de destino pendente de evidência | Acionar reconciliação |
| `auto_reconciled_via_wms` | Custódia Concluída e Reconciliada | Fechamento confirmado por evidência independente | Encerrar disputa operacional |
| `legacy_only_insufficient` | Custódia Pendente | Evidência externa insuficiente | Exigir fonte independente |
| `websnap_geolocation_missing` | Custódia Pendente | Confirmação de destino sem contexto suficiente | Reconciliar ou manter pendência |
| `websnap_outside_geofence` | Custódia Divergente | Evento de destino incompatível | Escalar exceção |
| `driver_controlled_evidence_rejected` | Custódia Pendente ou Divergente | Evidência não independente rejeitada | Impedir fechamento por ator interessado |
| `custody_divergent` | Custódia Divergente | Divergência objetiva de custódia | Acionar revisão, jurídico ou auditoria |

A linguagem externa deve ser factual e defensável. Ela não deve ocultar eventos relevantes, mas também não deve transformar limitação técnica em confissão comercial desnecessária.

## 35. Classes internas · [ALVO]

As classes internas V0–V4 e C0–C4 pertencem à arquitetura-alvo. No MVP-0, podem existir apenas como rascunho analítico, não como motor de status.

As classes técnicas podem existir no motor do SILD, mas não devem dominar a interface do MVP.

### Classes de captura V0–V4

Medem a qualidade técnica da mídia, do dispositivo e da sessão.

### Classes de cadeia C0–C4

Medem a força total da custódia, considerando origem, destino, contexto, ator, lacre, rota, independência e reconciliação.

Nos ciclos posteriores, essas classes devem ser usadas internamente para cálculo, auditoria e evolução de produto. O usuário operacional deve ver estados simples.

## 36. Níveis de conformidade SILD · [PADRÃO]

Os níveis de conformidade SILD organizam a força probatória de forma compreensível para mercado, auditoria, seguro e contratos.

Eles não substituem os MVPs. MVP é sequência de produto. Nível de conformidade é classe de aderência probatória.

### SILD L0 — Registered Evidence

Evidência documental simples.

Inclui operação criada, documento vinculado, lacre ou referência associada, foto mínima, hash simples, usuário, horário e dossiê.

É o nível compatível com o MVP-0.

### SILD L1 — Controlled Capture

Captura controlada leve.

Inclui câmera direta quando viável, validação simples de foco, leitura de QR ou serial, operador autenticado, dispositivo registrado e reason codes de qualidade.

É o nível compatível com evolução C1.

### SILD L2 — Attested Capture

Captura atestada.

Inclui PACC Lite, sessão viva, nonce, hash de mídia, dispositivo conhecido, metadados de sessão, bloqueio de galeria quando tecnicamente viável e contexto de captura.

É o primeiro nível em que a captura deixa de ser apenas evidência organizada e passa a ser evidência tecnicamente atestada.

### SILD L3 — Symmetric Custody

Custódia simétrica.

Inclui origem e destino observados, ator independente ou controlado, contexto válido, lacre ou unidade logística compatível, horário plausível e comparação origem-destino.

É o nível mínimo para falar em custódia concluída com força probatória relevante.

### SILD L4 — Granular Custody

Custódia granular.

Inclui pallet, gaiola, roll container, caixa, volume crítico ou unidade intermediária identificada, com PIP Duplex Lite, face observável, fechamento físico e vínculo com claim, NF, pedido, SKU, lote ou SSCC quando aplicável.

É o nível indicado para disputas internas à unidade lacrada.

### SILD L5 — Certified Custody Network

Rede de custódia certificada.

Inclui RPI completa, reconciliação madura, Mesa Humana, Fast Track controlado, Storage Lifecycle, legal hold, APIs, governança, auditoria, certificação de componentes e inteligência de rede federada.

É o nível de referência para adoção institucional e padrão de mercado.

A regra é:

> **O SILD não é aprovado ou reprovado de forma binária. Ele opera por níveis de conformidade, cada um com promessa probatória proporcional.**

## 37. Pacote de evidência · [MVP-0 → ALVO]

Cada evento SILD gera um pacote de evidência estruturado.

No MVP-0, esse pacote é reduzido: operação, documento, lacre, foto do lacre, foto de contexto, hash simples, usuário, data/hora, glosa vinculada quando houver e dossiê PDF.

Nos ciclos posteriores, o pacote cresce para incluir PACC Lite, PIP Duplex Lite, Symmetry, RPI completa, Claim Intake avançado, cold storage e legal hold.

O pacote não é apenas um conjunto de fotos. Ele é um transcrito probatório da operação, contendo mídia, contexto, ator, dispositivo, objeto observado, reason codes, vínculos operacionais e decisões posteriores.

O pacote pode conter:

- ID da operação;
- manifesto, DANFE, NF, pedido, romaneio ou documento equivalente;
- hash do documento quando disponível;
- placa capturada;
- unidade logística capturada;
- lacre capturado;
- integridade mecânica do lacre, quando observada;
- frames congelados em alta resolução;
- clipe auxiliar curto;
- PACC Lite associado;
- nonce ou desafio de captura;
- âncora local, SILD Hub, geofence ou ponto de doca;
- operador;
- dispositivo;
- classe de dispositivo D0–D4;
- origem ou destino;
- timestamp de servidor;
- timestamp de hub local quando aplicável;
- timestamp local declarado;
- status da captura;
- metadados técnicos;
- hash da mídia;
- resultado de QR, NFC, código de barras ou OCR assistido;
- reason codes;
- vínculo com eventos anteriores;
- classificação externa;
- classificação interna;
- teto probatório aplicado.

Em operações G2 Lite, o pacote também pode conter:

- Pallet ID;
- SSCC;
- etiqueta A capturada;
- etiqueta B capturada;
- face A ou B usada no fechamento;
- trava de emenda capturada;
- estado visual da envelopagem;
- evento de face indisponível no veículo;
- captura após descarga com observação;
- vínculo com NF, pedido, SKU, lote, pallet, gaiola, roll container ou volume crítico;
- estado do PIP Duplex Lite.

Em casos de divergência, reconciliação, RPI ou glosa, o pacote pode ser enriquecido com:

- decisão da Mesa Humana;
- evidência compensatória;
- recebimento WMS, EDI, portal ou confirmação comercial;
- evento de colisão probatória;
- RPI vinculada;
- claim importado;
- arquivo original de glosa;
- hash do arquivo de Claim Intake;
- dossiê de defesa;
- status de cold storage ou legal hold.

A regra é:

> **O SILD não armazena apenas imagens. Ele preserva uma narrativa técnica verificável da custódia.**

## 38. Evidence Register no MVP-0 e Custody Ledger na arquitetura-alvo · [MVP-0 + ALVO]

O MVP-0 não exige um ledger append-only avançado. Ele exige um **Evidence Register** simples, auditável e suficiente para ligar evidência de saída a uma glosa posterior.

No MVP-0, o Evidence Register deve registrar:

- operação;
- NF, pedido, manifesto ou referência documental;
- lacre vinculado;
- foto aproximada do lacre;
- foto de contexto traseiro;
- hash simples da mídia;
- usuário;
- data e hora;
- glosa vinculada quando houver;
- dossiê gerado.

Esse registro pode ser implementado em banco de dados comum, desde que mantenha trilha mínima de criação, alteração e exportação.

O **Custody Ledger append-only** pertence à arquitetura-alvo. Em ciclos posteriores, eventos não devem ser apagados; correções devem ser feitas por novos eventos.

O ledger maduro deve registrar:

- evento original;
- fonte da evidência;
- ator que produziu;
- canal de captura;
- dispositivo usado;
- horário;
- local;
- status interno;
- status externo;
- razão da decisão;
- correções posteriores;
- reconciliações;
- divergências;
- evidências compensatórias;
- aprovadores quando houver revisão humana.

A regra é:

> **MVP-0 registra evidência operacional suficiente. A arquitetura-alvo transforma essa evidência em cadeia append-only de custódia.**

## 39. Reconciliação assíncrona · [ALVO]

Reconciliação assíncrona não faz parte do MVP-0. No ciclo zero, o pós-fato é tratado por Claim Intake e dossiê de defesa.

A reconciliação assíncrona permite tirar uma viagem do limbo operacional sem reescrever a história probatória.

Princípio:

> **Evidência posterior explica; não purifica.**

Quando um evento falha, por exemplo por ausência de geolocalização no destino, o SILD registra o evento original e abre uma pendência.

A evidência compensatória pode fechar a disputa operacional, mas não transforma retroativamente a captura falha em captura perfeita.

O teto após falha relevante deve ser:

> **Custódia Concluída e Reconciliada.**

Não se deve retornar para Custódia Concluída plena se a validação original perdeu contexto essencial.

## 40. Evidências compensatórias · [ALVO]

Evidências compensatórias pertencem à arquitetura de reconciliação futura. No MVP-0, o sistema apenas anexa evidência de origem, glosa importada e dossiê gerado.

Evidências compensatórias fortes incluem:

- app autenticado do CD próprio;
- WMS do destino;
- registro de portaria do destinatário;
- e-mail corporativo do destino;
- API do comprador;
- registro de balança;
- CFTV com timestamp de sistema;
- conferente cadastrado;
- captura nova dentro do geofence por dispositivo independente.

Evidências médias incluem:

- POD tradicional com metadados;
- canhoto fotografado por terceiro;
- confirmação telefônica gravada por canal oficial;
- GR mostrando permanência compatível no destino;
- baixa no TMS do embarcador, quando não controlado pela transportadora.

Evidências fracas incluem:

- print de WhatsApp;
- foto enviada pelo motorista;
- baixa manual no TMS da transportadora;
- relato verbal;
- foto sem metadados;
- documento escaneado posteriormente;
- assinatura ilegível.

Dado produzido por quem se beneficia da simulação não pode curar a falha sozinho.

## 41. Fast Track de reconciliação · [ALVO]

Fast Track não pertence ao MVP-0. Sem visão computacional validada, Mesa Humana ou fontes compensatórias maduras, o sistema não deve automatizar conclusão de integridade física.

Para evitar paralisia por compliance, o SILD deve possuir uma esteira automatizada de reconciliação.

O **Fast Track** pode fechar automaticamente uma pendência quando houver falha de observabilidade e evidência compensatória forte, nativamente digital, independente e compatível com a topologia.

O Fast Track não deve fechar automaticamente falha de integridade física.

A regra é:

> **Falha de observabilidade pode ser reconciliada automaticamente. Falha de integridade física exige Mesa Humana ou inspeção.**

### Falhas de observabilidade elegíveis

Podem ir para Fast Track, conforme contexto:

- QR ilegível com imagem nítida;
- etiqueta danificada por atrito sem indício de violação;
- face indisponível no baú;
- captura após descarga com contexto preservado;
- falha de sincronização;
- ausência de leitura automática com mídia auditável;
- evento offline esperado com âncora local.

### Falhas que bloqueiam Fast Track

Não devem ir para Fast Track automático:

- lacre removido;
- trava de emenda rompida;
- stretch cortado;
- reembalagem aparente;
- pallet substituído;
- ID incompatível;
- divergência de quantidade, SKU ou lote;
- avaria reportada;
- WMS com ressalva;
- evidência produzida apenas por parte interessada;
- recorrência restrita acima do limite.

### Regra de cegueira da mídia

Se a falha for mídia borrada, escura, saturada por reflexo ou insuficiente para avaliar integridade física, o indicador `no_physical_tamper_indicator` deve ser tratado como **desconhecido**, nunca como verdadeiro.

Imagem nítida com QR ilegível pode ir para Fast Track. Imagem cega exige segundo sinal físico, nova captura ou Mesa Humana.

### Destino próprio

Em destino próprio ou controlado, o Fast Track deve exigir evidência granular: WMS, app autenticado, SSCC, pallet, conferente, estação de recebimento, doca ou evento equivalente.

### Destino terceiro ou marketplace

Em destino terceiro, o SILD pode aceitar EDI, NF, portal, confirmação sem ressalva, geofence, evento de entrega ou documento comercial, mas com teto probatório menor. O sistema deve registrar a qualidade da fonte e não elevar automaticamente a cadeia ao mesmo nível de destino próprio.

### Portas lógicas do Fast Track

O Fast Track só é permitido se todas as portas aplicáveis forem verdadeiras:

1. a falha é de observabilidade, não de integridade;
2. não há indício físico claro de violação;
3. a mídia não está cega, ou existe segundo sinal físico obrigatório;
4. a fonte compensatória é independente ou controlada pelo destino;
5. a evidência é compatível com NF, pedido, manifesto, pallet ou operação;
6. não há divergência de quantidade, SKU, lote, avaria ou ressalva;
7. a janela temporal é compatível;
8. a carga não está em classe crítica que exija Mesa Humana;
9. não há sinal conflitante de GR, portaria, WMS, TMS ou captura física;
10. a recorrência restrita está abaixo do limite.

A mesa humana deve ser acionada quando houver:

- carga de alto valor;
- evidência fraca;
- evidência média dependente de interpretação;
- contradição;
- divergência de lacre;
- histórico recorrente de falhas;
- sinistro;
- disputa judicial;
- cliente estratégico;
- exceção fora do padrão.

### Recorrência restrita

O bloqueio do Fast Track por recorrência não deve depender apenas de rota genérica. Deve considerar combinações restritas:

- motorista;
- placa;
- veículo;
- transportadora;
- operador de pátio;
- dispositivo;
- doca;
- destino;
- motorista + veículo + operador;
- transportadora + destino + tipo de falha.

Duas falhas sequenciais ou três alternadas em janela curta podem suspender o Fast Track para o ativo ou combinação envolvida, mesmo que a rota global esteja estatisticamente saudável.

## 42. Colisão probatória · [MVP-0 + ALVO]

No MVP-0, a colisão é documental: evidência de saída versus glosa posterior. A colisão física completa, entre recebimento sistêmico e anomalia material observada no destino, pertence a ciclos com Symmetry, G2 Lite ou RPI completa.

A **colisão probatória** ocorre quando duas fontes relevantes registram verdades diferentes sobre a mesma operação.

O caso mais importante é a colisão entre evidência física SILD e recebimento sistêmico do cliente.

Exemplo:

- o WMS, EDI, portal ou documento do destinatário registra recebimento sem ressalva;
- o SILD registra trava de emenda rompida, lacre removido, stretch cortado, reembalagem aparente, etiqueta substituída ou divergência física relevante.

Nesse cenário, o SILD não deve escolher uma verdade única e apagar a outra. O sistema deve registrar a colisão como fato auditável.

A regra é:

> **WMS tem primazia para recebimento comercial. Evidência física tem primazia para integridade externa observada.**

O recebimento sistêmico sem ressalva pode confirmar que o cliente aceitou a entrega no seu sistema. Ele não elimina automaticamente uma anomalia física registrada na cadeia de custódia.

O status recomendado é:

> **Custódia Recebida com Divergência Física Não Reconciliada**

ou, em linguagem comercial:

> **Recebimento Sistêmico Confirmado com Divergência Física Registrada**

Esse status não acusa furto, culpa, conluio, má-fé ou responsabilidade de qualquer parte. Ele documenta que houve colisão entre aceite sistêmico e condição física observada.

A redação padrão do relatório deve ser:

> **O pallet, veículo ou unidade logística foi registrado pelo sistema do destinatário como recebido sem ressalva. Contudo, a evidência técnica SILD registra alteração física na integridade externa da unidade logística, conforme reason code associado. Este documento certifica a existência da colisão probatória entre o registro sistêmico e a condição física observada, servindo como Ressalva Preventiva de Integridade para fins de auditoria, direito de regresso, acionamento de seguro ou contestações de inventário futuras. As mídias, metadados e hashes associados foram preservados no dossiê da operação.**

O relatório não deve dizer:

- fraude confirmada;
- furto provável;
- cliente recebeu carga violada;
- motorista responsável;
- WMS inválido;
- entrega íntegra sem ressalvas.

A colisão probatória deve preservar direito, prova e contexto sem transformar o SILD em acusador.

## 43. Mesa Humana · [ALVO]

Mesa Humana formal não pertence ao MVP-0. No ciclo zero, revisões podem ocorrer fora do sistema, mas não devem ser tratadas como módulo obrigatório.

A Mesa Humana existe para decidir casos em que a automação não deve concluir sozinha.

Ela não substitui perícia, jurídico, seguradora ou auditoria. Sua função é classificar a evidência SILD quando o motor encontra ambiguidade, contradição ou risco acima do permitido para Fast Track.

A Mesa Humana deve ser acionada quando houver:

- indício físico de violação;
- mídia cega sem segundo sinal físico suficiente;
- divergência de quantidade, SKU, lote ou avaria;
- WMS com ressalva;
- recebimento sistêmico incompatível com evidência física;
- carga crítica;
- cliente estratégico;
- sinistro potencial;
- recorrência restrita acima do limite;
- falha de captura recorrente em mesmo motorista, veículo, operador, doca, transportadora ou destino;
- contestação comercial vinculada a operação com RPI.

A Mesa Humana deve escolher uma conclusão padronizada:

### Falso positivo físico descartado

A anomalia visual foi explicada por reflexo, dobra natural do stretch, etiqueta danificada por atrito sem abertura, baixa luz ou erro de captura.

Status externo possível:

> **Custódia Concluída e Reconciliada**

### Suspeita física inconclusiva

Há limitação relevante, mas não há materialidade suficiente para classificar violação.

Status externo possível:

> **Custódia Recebida com Observação Física**

### Divergência física confirmada sem falta comercial reportada

Há anomalia física relevante, mas o cliente registrou recebimento sem ressalva.

Status externo possível:

> **Custódia Recebida com Divergência Física Não Reconciliada**

### Divergência física com falta, avaria ou glosa

A evidência física e a contestação comercial apontam para ruptura operacional compatível.

Status externo possível:

> **Custódia Divergente**

A Mesa Humana não deve apagar o evento original. Deve acrescentar decisão, motivo, aprovador, data, evidências consideradas e teto probatório.

## 44. RPI completa — Ressalva Preventiva de Integridade · [ALVO]

Esta seção descreve a RPI completa. No MVP-0 existe apenas RPI Lite: uma flag documental aberta por claim match.

A **RPI — Ressalva Preventiva de Integridade** é uma entidade de ciclo de vida criada quando há divergência física relevante, colisão probatória ou risco de contestação futura.

A RPI transforma um alerta estático em um processo controlado. Ela preserva evidência, controla prazos, monitora glosas, aciona áreas internas e mantém a operação protegida contra cobranças tardias.

A RPI não é acusação de fraude. Ela é uma reserva formal de integridade.

A RPI deve ser aberta quando houver:

- trava de emenda rompida;
- lacre removido, substituído ou incompatível;
- stretch cortado;
- reembalagem aparente;
- etiqueta A/B incompatível;
- pallet com sinais físicos de violação;
- recebimento sistêmico sem ressalva conflitante com evidência física;
- mídia ou evidência crítica que justifique preservação de direitos;
- evento que possa gerar glosa tardia, seguro, auditoria ou direito de regresso.

A frase operacional é:

> **A RPI preserva a divergência física antes que ela vire disputa comercial.**

A RPI pode servir para:

- auditoria;
- direito de regresso;
- aviso preventivo de sinistro;
- contestação de glosa;
- preservação de CFTV;
- revisão de transportadora;
- análise de conluio;
- dossiê de defesa contra chargeback tardio.

## 45. Severidade da RPI completa · [ALVO]

A severidade da RPI não pertence ao MVP-0. No ciclo zero, a RPI Lite não possui severidade operacional formal.

A RPI deve possuir severidade proporcional à materialidade do evento.

### RPI baixa

Eventos de baixa severidade:

- etiqueta arranhada;
- QR parcialmente degradado;
- etiqueta B ausente, mas etiqueta A válida;
- mídia limitada sem indício físico de violação;
- dano de atrito sem alteração do stretch;
- falha de leitura compensada por evidência forte.

Ação padrão:

- registrar observação;
- preservar evidência normal;
- não acionar alerta crítico;
- monitorar recorrência.

### RPI média

Eventos de média severidade:

- stretch frouxo;
- emenda deslocada;
- etiqueta gêmea ausente sem explicação clara;
- captura após descarga em contexto sensível;
- face probatória inacessível;
- divergência física leve sem falta reportada.

Ação padrão:

- manter em Observação Comercial;
- vincular ao pedido, NF, pallet ou SSCC;
- aguardar eventual glosa ou inventário;
- preservar mídia conforme política ampliada.

### RPI crítica

Eventos de alta severidade:

- trava de emenda rompida;
- lacre substituído;
- lacre removido;
- lona, stretch ou fechamento cortado;
- reembalagem aparente;
- pallet com violação física clara;
- colisão forte entre prova física SILD e WMS sem ressalva.

Ação padrão:

- abrir alerta crítico interno;
- recomendar preservação de CFTV;
- recomendar aviso preventivo de sinistro quando aplicável;
- marcar operação para inventário ou revisão prioritária;
- bloquear Fast Track futuro para combinação de risco quando houver recorrência;
- preservar mídia, hashes e metadados com retenção ampliada.

A regra é:

> **RPI crítica não aguarda passivamente o cliente reclamar. Ela preserva prova e direito no Dia 0.**

## 46. Ciclo de vida da RPI completa · [ALVO]

Este ciclo de vida não pertence ao MVP-0. No ciclo zero, a RPI Lite nasce por claim match e serve apenas para marcar o dossiê.

A RPI possui ciclo de vida próprio.

### RPI Aberta

Criada no momento em que a divergência física, colisão probatória ou risco relevante é registrado.

### RPI Crítica — Ação Imediata

Estado aplicado quando a severidade exige preservação de prova, compliance interno, GR, jurídico, seguro ou CFTV.

### RPI em Observação Comercial

Estado aplicado após ações iniciais. O caso sai da fila crítica, mas permanece monitorado até o fim da janela comercial.

### RPI Reforçada por Contestação

Estado aplicado quando chega glosa, chargeback, cobrança, abatimento, falta, avaria, divergência de inventário ou contestação relacionada à operação.

### Janela Comercial Encerrada — Respiro de Integração

Estado aplicado ao fim do prazo contratual do cliente, antes do encerramento definitivo, para absorver atrasos de portal, EDI, financeiro, conciliação ou importação.

### RPI Encerrada sem Contestação Recebida

Estado aplicado quando termina a janela comercial e o período de respiro sem que o embarcador tenha recebido contestação vinculada.

### Contestação Tempestiva Recebida em Atraso

Estado aplicado quando a contestação chegou ao embarcador depois da janela, mas o documento do cliente demonstra que ela foi aberta dentro do prazo contratual.

### Contestação Pós-Janela — Tempestividade Não Comprovada

Estado aplicado quando a contestação chega depois da janela e a data efetiva de abertura pelo cliente não é comprovada.

### Contestação Extemporânea — Dossiê de Recusa de Débito

Estado aplicado quando a contestação foi aberta fora do prazo contratual ou comercial aplicável.

### RPI Arquivada com Retenção Probatória

Estado aplicado quando o alerta sai da operação ativa, mas o dossiê permanece preservado para auditoria, seguro, defesa comercial, histórico de recorrência ou litígio.

A regra é:

> **O alerta operacional expira; a evidência permanece.**

## 47. Janelas temporais da RPI completa · [ALVO]

As janelas temporais completas da RPI pertencem ao MVP-3. O MVP-0 pode registrar a data da glosa e a data da importação, mas não gerencia ciclo de vida completo.

A RPI deve controlar três janelas temporais.

### Janela operacional curta

Serve para ação imediata:

- preservar CFTV;
- notificar compliance interno;
- acionar GR;
- avisar jurídico;
- recomendar aviso preventivo de sinistro;
- marcar inventário cíclico;
- preservar mídia quente temporariamente.

### Janela comercial média

Serve para aguardar:

- glosa;
- chargeback;
- abatimento;
- divergência de inventário;
- cobrança por falta interna;
- contestação do cliente;
- retorno de portal ou marketplace.

O prazo deve ser configurável por cliente, contrato, marketplace, rota ou tipo de operação.

Exemplo:

```text
customer_claim_window_days = 90
```

### Janela de respiro comercial

Após o fim da janela contratual, o SILD deve aguardar um período adicional antes de encerrar a RPI como sem contestação recebida.

Exemplo:

```text
cooling_off_days = 7
rpi_observation_until = delivery_date + customer_claim_window_days + cooling_off_days
```

Essa janela evita falso arquivamento quando a glosa foi aberta pelo cliente dentro do prazo, mas ainda está em trânsito entre portal, EDI, financeiro e sistema do embarcador.

### Janela probatória longa

Serve para retenção do dossiê:

- seguro;
- auditoria;
- direito de regresso;
- defesa contra glosa;
- litígio;
- análise de recorrência.

A fórmula geral é:

```text
rpi_active_until = max(
  customer_claim_window_days,
  marketplace_dispute_window_days,
  internal_audit_window_days,
  insurance_notice_followup_window_days
) + cooling_off_days

evidence_retention_until = max(
  rpi_active_until,
  contractual_retention_days,
  legal_hold_if_any
)
```

Nenhuma RPI crítica deve ser descartada enquanto houver janela aberta de glosa, seguro, auditoria ou disputa.

## 48. SILD Claim Intake · [MVP-0 → ALVO]

O **SILD Claim Intake** é o módulo de ingestão de glosas, chargebacks, abatimentos, divergências financeiras e contestações comerciais recebidas pelo embarcador.

No **MVP-0**, o Claim Intake deve aceitar apenas **um template padrão SILD**. O embarcador é responsável por copiar, exportar ou formatar os dados da glosa para esse modelo antes do upload.

A regra do MVP-0 é:

> **Um layout. Um upload. Um vínculo com a evidência de origem.**

O MVP-0 não deve tentar interpretar automaticamente planilhas específicas da Amazon, Mercado Livre, Carrefour, Magalu, B2W, ERP interno, EDI financeiro ou portal de fornecedor. Isso pertence a fases posteriores.

O SILD não deve depender de API de marketplace, WMS do destinatário ou EDI obrigatório para provar valor no primeiro ciclo.

A regra comercial é:

> **O SILD não integra primeiro com o marketplace. Ele integra primeiro com a dor do embarcador: a glosa que chegou ao financeiro.**

No MVP-0, o SILD **não faz limpeza de planilha bruta**. A conversão da glosa bruta do cliente para o template SILD válido é **atividade operacional do cliente**, assistida apenas na implantação inicial. A plataforma recebe somente o template SILD válido; não absorve a bagunça documental do marketplace no ciclo zero.

> **No MVP-0, a plataforma recebe apenas o template SILD válido. A conversão de planilhas brutas do cliente para o template é atividade operacional do cliente, assistida apenas na implantação inicial.**

Para apoiar essa conversão sem inchar o produto, o SILD fornece uma **planilha-matriz de conversão** como **artefato de implantação** — um guia externo que mapeia colunas comuns de portais e ERPs para o template oficial. Esse artefato não é módulo de software, não roda dentro da plataforma e não deve ser confundido com o "mapper visual de planilhas", que fica fora do MVP-0 (seção 16).

Canal suportado no MVP-0:

- upload CSV/XLSX no template oficial SILD.

Canais futuros:

- layouts recorrentes por cliente;
- arquivo exportado de portal de fornecedor;
- planilha financeira de abatimento;
- relatório de cobrança;
- EDI importado manualmente;
- SFTP para clientes maduros;
- API;
- conectores com ERP, TMS, WMS ou financeiro.

O upload manual não deve ser planilha livre sem controle. Ele deve possuir:

- template oficial;
- validação de colunas;
- validação de datas;
- deduplicação simples;
- usuário responsável pelo upload;
- armazenamento do arquivo original;
- relatório de linhas aceitas, rejeitadas e pendentes.

No MVP-0, a RPI não nasce durante a jornada. Ela nasce quando uma glosa é importada e vinculada a uma evidência de origem.

Eventos do Claim Intake no MVP-0:

- `claim_file_imported`;
- `commercial_claim_received`;
- `claim_linked_to_origin_evidence`;
- `claim_line_rejected`;
- `claim_line_pending_exported`.

Eventos futuros:

- `claim_file_hash_recorded`;
- `claim_line_pending_association`;
- `claim_linked_to_operation`;
- `claim_linked_to_rpi`;
- `claim_unmatched`.

## 49. Dados mínimos de uma glosa ou contestação · [MVP-0]

O Claim Intake deve capturar os campos mínimos necessários para vincular cobrança comercial a evidência logística.

Campos obrigatórios:

- cliente ou destinatário;
- CNPJ ou identificador do cliente;
- NF ou chave de acesso;
- pedido, ordem de compra ou referência comercial;
- data da entrega;
- data da contestação informada pelo cliente;
- data em que o embarcador recebeu a contestação;
- tipo de glosa;
- valor contestado;
- quantidade contestada quando aplicável;
- documento de origem;
- protocolo do cliente quando houver.

Campos desejáveis:

- pallet ID;
- SSCC;
- SKU;
- lote;
- romaneio;
- manifesto;
- transportadora;
- placa;
- rota;
- centro de distribuição;
- observação do cliente;
- comprovante anexo;
- data de processamento financeiro.

Tipos de glosa:

- falta;
- avaria;
- divergência de SKU;
- divergência de quantidade;
- devolução;
- atraso;
- abatimento comercial;
- cobrança por inventário;
- divergência de lote;
- contestação genérica.

O evento normalizado é:

```text
commercial_claim_received
```

No MVP-0, esse evento aciona apenas o vínculo com evidência de origem e a RPI Lite quando houver claim match. O motor completo da RPI pertence a ciclos posteriores.

## 50. Vínculo entre glosa, operação e RPI por fase · [MVP-0 + ALVO]

O vínculo entre glosa, operação e RPI deve ser simples no MVP-0 e mais rico nos ciclos posteriores.

### MVP-0

No MVP-0, o sistema vincula a glosa importada no template SILD à evidência de saída por NF, pedido, manifesto ou referência comercial.

Fluxo:

```text
Arquivo de glosa importado
        ↓
Claim Intake valida o template SILD
        ↓
Gera commercial_claim_received
        ↓
Motor busca operação por NF, pedido ou referência
        ↓
Se encontrar evidência de saída:
        claim_linked_to_origin_evidence
        rpi_lite_opened_by_claim_match
        defense_dossier_generated
Se não encontrar:
        claim_without_matching_origin_evidence
```

No MVP-0, não há RPI completa, Observação Comercial, Mesa Humana formal ou ciclo de vida avançado. Há apenas RPI Lite como marca documental da colisão entre glosa recebida e evidência de saída existente.

#### Por que o matching não é trivial no MVP-0

Toda a promessa de "dossiê em minutos" depende do evento `claim_linked_to_origin_evidence`. Mas glosas reais chegam com referências bagunçadas: às vezes só com número de pedido, às vezes com um ID interno do cliente que não corresponde à NF, às vezes com a chave de acesso truncada, frequentemente sem pallet ou SSCC. Se uma fração relevante das glosas cair em `claim_without_matching_origin_evidence`, a promessa quebra logo na primeira semana de piloto.

Portanto, o matching precisa de estratégia já no ciclo zero — não na arquitetura-alvo. A estratégia do MVP-0 é deliberadamente simples, mas não ingênua.

#### Normalização de chave obrigatória no MVP-0

Antes de tentar qualquer vínculo, o Claim Intake deve normalizar as chaves de ambos os lados (glosa e operação):

- **chave de NF:** remover máscara, espaços, pontuação; quando houver chave de acesso de 44 dígitos, extrair e indexar também o número da NF e a série; aceitar correspondência por chave completa **ou** por número+série+CNPJ emitente.
- **pedido / ordem de compra:** normalizar caixa, zeros à esquerda e prefixos do cliente; manter o valor bruto original preservado ao lado do normalizado.
- **CNPJ / identificador do cliente:** normalizar para dígitos; tolerar matriz/filial comparando a raiz de 8 dígitos quando a comparação por 14 falhar.
- **datas:** converter para ISO; tolerar fuso e formato brasileiro.
- **valor:** normalizar separador decimal e moeda.

O sistema deve guardar tanto o valor original quanto o normalizado, para auditoria e para o dossiê.

#### Cascata de matching do MVP-0

O motor do ciclo zero deve tentar o vínculo em cascata determinística, parando no primeiro nível que resolver, e **declarar a chave usada**:

1. **Match por chave de NF normalizada** (preferencial).
2. **Match por número+série de NF + CNPJ emitente**, quando a chave completa não bate.
3. **Match por pedido normalizado + CNPJ do cliente**, quando não há NF utilizável.
4. **Match por referência comercial declarada no template** (campo livre controlado), apenas como apoio.

Se nenhum nível resolver, a linha **não** é descartada silenciosamente e **não** gera tela de investigação no MVP-0. Ela é exportada como pendência (`claim_line_pending_exported`) em um **CSV de rejeições e pendências**, para correção externa pelo cliente e novo upload. Linha malformada que falha na validação do template gera `claim_line_rejected` no mesmo arquivo.

O fluxo do MVP-0 fica:

```text
Arquivo de glosa importado
        ↓
Claim Intake valida o template SILD
        ↓
Linha inválida → claim_line_rejected (vai para o CSV de pendências)
        ↓
Normaliza chaves (NF, pedido, CNPJ, datas, valor)
        ↓
Gera commercial_claim_received
        ↓
Cascata de matching (NF → NF+série+CNPJ → pedido+CNPJ → referência)
        ↓
Se resolver:
        claim_linked_to_origin_evidence  (registra a chave usada)
        rpi_lite_opened_by_claim_match
        defense_dossier_generated
Se não resolver automaticamente:
        claim_line_pending_exported      (CSV de pendências → corrigir e reenviar)
Se não houver operação correspondente alguma:
        claim_without_matching_origin_evidence
```

A regra de matching do MVP-0 é:

> **O SILD não deve perder uma glosa porque o cliente informou a referência de forma imperfeita. Ele deve normalizar, tentar a melhor chave disponível em cascata, declarar qual chave usou e, quando falhar, exportar a pendência para correção externa — nunca um descarte silencioso e nunca uma tela de investigação no ciclo zero.**

A regra de pendência é:

> **No MVP-0, linha não conciliada não gera tela de investigação. Ela gera arquivo de pendência para correção externa e novo upload.**

Essa decisão é deliberadamente de baixo volume: para o piloto de 30 dias, o round-trip de CSV é preferível a construir uma interface de reconciliação. A fila de associação manual em tela, com candidatos sugeridos, pertence a ciclos posteriores.

A **taxa de match automático**, a **taxa de linhas rejeitadas no template** e a **taxa de novo upload após correção** passam a ser métricas de primeira linha do piloto (ver seção 71), porque medem diretamente se a promessa do ciclo zero se sustenta na realidade dos dados do cliente.

### Arquitetura-alvo

Nos ciclos posteriores, o motor pode associar glosa a operação por camadas de confiança.

#### Match forte

Ocorre quando há:

- mesma NF ou chave;
- mesmo pedido;
- mesmo pallet ID ou SSCC;
- mesmo cliente;
- data de entrega compatível;
- valor ou quantidade compatível.

Ação:

> Vincular automaticamente à RPI ou operação.

#### Match médio

Ocorre quando há:

- mesma NF;
- mesmo cliente;
- mesmo SKU ou lote;
- data de entrega compatível;
- ausência de pallet ou SSCC.

Ação:

> Vincular com observação ou enviar para fila rápida de validação.

#### Match fraco

Ocorre quando há:

- mesmo cliente;
- período compatível;
- valor ou SKU semelhante;
- identificadores incompletos.

Ação:

> Criar caso pendente de associação.

#### Sem match

Ocorre quando não há vínculo confiável.

Ação:

> Criar contestação isolada sem RPI vinculada.

O SILD não deve perder uma glosa porque o marketplace não informou pallet. Ele deve vincular pela melhor chave disponível e declarar a qualidade do vínculo.

O motor deve ser orientado por eventos, não por varredura cega.

## 51. Armazenamento, cold storage e legal hold · [ALVO]

Cold storage automatizado e legal hold sistêmico não pertencem ao MVP-0. O ciclo zero deve manter retenção simples e proporcional.

O SILD deve separar retenção lógica de retenção de mídia pesada.

Eventos, hashes, reason codes e metadados devem permanecer pesquisáveis conforme a política contratual e jurídica.

Mídias pesadas, como frames de alta resolução e clipes auxiliares, podem migrar para armazenamento frio após a janela comercial e o período de respiro, desde que não haja contestação aberta, sinistro, auditoria, litígio ou legal hold.

A política recomendada é:

- operações normais: retenção padrão contratual;
- RPI baixa: retenção padrão com marcação de observação;
- RPI média: retenção até fim da janela comercial + respiro + prazo adicional configurado;
- RPI crítica: retenção ampliada;
- RPI com glosa, sinistro, auditoria ou litígio: legal hold sem descarte automático;
- mídia sem valor probatório residual: descarte, redução ou anonimização após finalidade.

Eventos de armazenamento:

- `rpi_media_moved_to_cold_storage`;
- `rpi_media_restored_for_claim_review`;
- `legal_hold_applied`;
- `legal_hold_released`;
- `evidence_retention_extended`;
- `evidence_disposal_executed`.

A regra é:

> **O ledger permanece quente. A mídia pesada pode esfriar. A prova não desaparece.**

O painel deve permitir localizar o dossiê por operação, cliente, NF, pallet, SSCC, placa, rota, transportadora, RPI ou claim mesmo quando a mídia estiver em cold storage.

## 52. Relatório SILD · [MVP-0 → ALVO]

O relatório SILD deve organizar evidência em camadas.

### Camada operacional

Mostra:

- status atual;
- ação necessária;
- severidade;
- prazo;
- pendências;
- divergências;
- responsável interno;
- próximos eventos esperados.

### Camada probatória

Mostra:

- mídia;
- hashes;
- PACC Lite;
- PIP Duplex Lite;
- reason codes;
- trilha de eventos;
- dispositivo;
- operador;
- âncora local;
- timestamps;
- qualidade da mídia;
- teto probatório.

### Camada comercial

Mostra:

- recebimento sistêmico;
- WMS, EDI, portal ou arquivo financeiro;
- status de glosa;
- RPI;
- Claim Intake;
- valor contestado;
- vínculo com NF, pedido, pallet ou SSCC;
- dossiê de defesa.

### Camada jurídica e seguro

Mostra:

- Ressalva Preventiva de Integridade;
- preservação de prova;
- recomendação de aviso preventivo;
- legal hold;
- histórico de exportações;
- retenção aplicável.

A redação externa deve ser factual e defensável.

Frase padrão:

> **O recebimento sistêmico sem ressalva confirma o encerramento comercial informado pelo destinatário, mas não elimina a divergência física observada na unidade logística.**

A expressão “limitação probatória” pode existir na camada técnica interna, mas deve ser usada com cautela em relatórios externos.

## 53. Sistemas legados · [BASE]

TMS, GR, POD, ERP, WMS, EDI, portais de marketplace e arquivos financeiros podem compor a narrativa logística, mas não possuem a mesma força probatória.

A regra é:

> **Sistema legado não eleva sozinho a força de evidência física SILD.**

Ele pode:

- corroborar;
- contradizer;
- explicar;
- acionar reconciliação;
- compor conjunto independente;
- ajudar a reconstruir cronologia;
- gerar evento de Claim Intake.

Ele não pode lavar uma falha física relevante sozinho.

Se há WMS sem ressalva, mas o SILD registra trava rompida, o caso não deve ir para Fast Track pleno. Deve gerar colisão probatória, RPI ou Mesa Humana conforme severidade.

Se há EDI ou portal sem ressalva em destino terceiro, o evento pode reconciliar falha de observabilidade, mas com teto probatório proporcional à qualidade da fonte.

---

# PARTE V — ELEGIBILIDADE E OPERAÇÃO

## 54. Interoperabilidade e APIs do protocolo · [ALVO]

O SILD deve evitar dependência prematura de integrações específicas, mas seu protocolo deve nascer preparado para interoperabilidade.

A regra é:

> **Primeiro definir contratos de evidência; depois construir conectores.**

APIs e contratos futuros:

### Operation API

Cria, consulta e atualiza operações logísticas por documento, pedido, manifesto, cliente, origem, destino, transportadora, placa, lacre ou unidade de custódia.

### Evidence Event API

Registra eventos de custódia, evidências, reason codes, mídia, hash, dispositivo, ator, canal e status.

### Claim Intake API

Recebe commercial claims, chargebacks, abatimentos, divergências financeiras, glosas e contestações em formato estruturado.

### RPI API

Consulta e atualiza RPIs, severidade, janelas comerciais, eventos de reforço por claim, legal hold, arquivamento e dossiês associados.

### Dossier Export API

Gera e exporta dossiês em PDF, JSON probatório, pacote de mídia, hash manifest, trilha de eventos e anexos.

### Conformance API

Permite verificar se uma evidência, componente, operação, integração ou dossiê atende a determinado nível de conformidade SILD.

### Webhooks

Eventos recomendados:

- evidência de saída registrada;
- captura incompleta;
- claim importado;
- claim vinculado;
- RPI aberta;
- divergência física;
- colisão probatória;
- reconciliação concluída;
- dossiê gerado;
- legal hold aplicado;
- retenção estendida.

A interoperabilidade deve preservar minimização de dados, segregação por cliente, controle de acesso, trilha de exportação e finalidade legítima.

O SILD deve integrar com WMS, TMS, ERP, GR, seguradoras, portais e marketplaces por contratos probatórios, não por adaptação caótica a cada fonte.

## 55. Contingência · [BASE]

Contingência é parte da logística real.

Pode haver falha de rede, chuva, baixa iluminação, QR ilegível, câmera danificada, pressa de doca, erro operacional, pátio metálico, queda de energia, etiqueta raspada, WMS atrasado ou indisponibilidade temporária do aplicativo.

A contingência não deve bloquear automaticamente a operação.

A contingência também não deve virar caminho padrão para escapar do sistema.

Ela deve gerar:

- evento auditável;
- causa declarada;
- status proporcional;
- evidência compensatória quando houver;
- monitoramento de recorrência;
- melhoria de processo;
- suspensão de Fast Track quando houver recorrência restrita.

Contingência recorrente não prova fraude. Ela prova perda de qualidade operacional ou tentativa de evasão a investigar.

A regra é:

> **Contingência isolada reconcilia. Contingência recorrente perde benefício automático.**

## 56. MEP — Motor de Elegibilidade Probatória por fase · [MVP-0 + ALVO]

O **MEP — Motor de Elegibilidade Probatória** define qual produto SILD é aplicável à operação.

No MVP-0, o MEP deve ser mínimo e não deve exigir PACC Lite, SILD Hub, destino cooperativo, G2 Lite ou integração.

Perguntas mínimas do MVP-0:

- a origem é controlada?
- a carga sai lacrada?
- há NF, pedido, manifesto ou documento associável?
- há operador de pátio disponível para captura C0?
- há foto mínima de lacre e contexto?
- há fluxo de glosa que possa ser importado no template SILD?
- a tese comercial é defesa de regresso, seguro, auditoria ou redução de caça manual a evidências?

Se essas respostas forem positivas, o MVP-0 é elegível.

Na arquitetura-alvo, o MEP pode avaliar:

- topologia logística;
- cooperação do destino;
- granularidade da custódia;
- densidade de paradas;
- criticidade da carga;
- tipo de lacre;
- disponibilidade de captura na origem;
- disponibilidade de observação no destino;
- existência de GR;
- possibilidade de auditoria;
- histórico operacional;
- janela comercial de contestação;
- capacidade de Claim Intake;
- necessidade de RPI;
- viabilidade de PACC Lite;
- viabilidade de SILD Hub ou âncora local;
- necessidade de G1, G2 Lite ou G3.

A regra é:

> **O SILD só promete a força probatória que a topologia permite.**

## 57. Topologias operacionais por fase · [MVP-0 + ALVO]

O SILD classifica operações conforme capacidade de gerar evidência. Nem toda topologia pertence ao MVP-0.

### T1 — Origem controlada e destino próprio

Cenário ideal para ciclos posteriores com Origin Snap + Symmetry, app autenticado nas duas pontas, WMS granular e Fast Track mais forte.

No MVP-0, pode operar apenas como auditoria de saída se o destino ainda não for integrado.

### T2 — Origem controlada e destino cooperativo

Elegível, em ciclos posteriores, para Origin Snap + WebSnap, app do destino, portal, WMS, EDI, API, canal oficial ou confirmação estruturada.

No MVP-0, o destino cooperativo não é necessário.

### T3 — Multi-drop cooperativo

Elegível para Proof Segmentado por unidade logística, destino, pallet, gaiola ou volume crítico em fases posteriores.

Não pertence ao MVP-0.

### T4 — LTL aberto e varejo fracionado

Não deve receber Proof Completo em G1. Pode operar com G2 Lite por pallet, gaiola, roll container ou volume crítico em MVP-2.

No MVP-0, só deve entrar se a tese for defesa documental de origem e regresso, sem promessa de granularidade interna.

### T5 — Last-mile capilar não cooperativo

Não deve receber certificado forte. Pode gerar rastreabilidade parcial e evidência documental, mas não é prioridade do MVP-0.

### T6 — Marketplace ou varejo dominante com portal fechado

No MVP-0, o caminho correto é **Origin Snap Basic + Claim Intake + dossiê de regresso**, sem prometer vitória contra o marketplace.

Em ciclos posteriores, pode evoluir para G2 Lite + Claim Intake, dependendo de palletização, dados de portal, EDI, documento comercial, geofence, comprovante, aceite sistêmico ou glosa financeira recebida posteriormente.

A matriz impede que o sistema force alta confiança em operações estruturalmente incapazes de produzi-la.

## 58. Índice de Cooperação do Destino · [ALVO]

O **ICD — Índice de Cooperação do Destino** mede se o destino pode funcionar como pilar probatório.

Na arquitetura-alvo inicial, o ICD deve ser operacional, não estatístico.

Categorias:

### Destino próprio

Usa app autenticado, WMS controlado ou sistema interno.

### Destino cooperativo

Aceita WebSnap, app, e-mail oficial, WMS, API, PIN, EDI ou confirmação estruturada.

### Destino parcialmente cooperativo

Aceita alguma evidência, mas sem autenticação forte ou granularidade plena.

### Destino terceiro fechado

Fornece apenas portal, EDI, confirmação financeira, arquivo de glosa ou comprovante sem acesso granular ao WMS.

### Destino não cooperativo

Não permite confirmação confiável.

A regra é:

> **Destino não cooperativo não destrói a prova de origem; apenas impede simetria forte.**

## 59. Índice de Granularidade da Custódia · [BASE]

O **IGC — Índice de Granularidade da Custódia** define o objeto certificado pelo SILD.

### G1 — Caminhão, carreta, baú ou contêiner inteiro

Adequado para FTL, hub-to-hub e cargas lacradas como unidade única.

### G2 — Pallet, gaiola, roll container ou unidade logística intermediária

Adequado para operações fracionadas controladas, defesa de receita, glosas por pallet, cargas sensíveis e volumes críticos.

### G2 Lite — Pallet Snap

Versão operacional de baixo atrito para MVP. Registra identidade do pallet ou unidade intermediária, face observável, stretch film, emenda/trava e captura por etiqueta duplex.

O G2 Lite não prova caixa a caixa. Ele reduz a zona cega entre “baú lacrado” e “item contestado”.

### G3 — Caixa, volume ou remessa individual

Adequado para cargas sensíveis em LTL, desde que haja identificação e lacre por unidade.

### G4 — Remessa documental

Adequado para varejo capilar sem controle físico granular.

A regra é:

> **Se a operação é multi-drop e não há lacre, etiqueta ou identificação por unidade logística, o SILD não deve emitir certificação forte por entrega individual.**

## 60. Disputas internas à unidade lacrada · [BASE]

O SILD deve distinguir disputa sobre a unidade lacrada de disputa dentro da unidade lacrada.

Se a operação opera em granularidade **G1**, o sistema pode demonstrar que a unidade saiu lacrada e chegou com lacre compatível. Isso não resolve, sozinho, disputas sobre falta de caixa, avaria interna, pallet incompleto ou divergência de conteúdo dentro da unidade lacrada.

Quando a dor comercial recorrente envolve faltas internas, o piloto deve migrar para granularidade superior:

- G2 Lite, com pallet, gaiola, roll container ou volume crítico identificado;
- G2, com unidade logística intermediária mais controlada;
- G3, com caixa, volume ou remessa individual identificada;
- inspeção, pesagem, conferência material ou integração adicional fora do escopo do Origin Snap.

A regra é:

> **Lacre íntegro protege a narrativa da unidade lacrada. Não prova composição interna se a granularidade não foi capturada.**

## 61. Relação com Gerenciamento de Risco · [BASE]

O SILD não substitui gerenciadoras de risco.

Gerenciamento de risco tradicional responde principalmente:

- onde está o veículo;
- se ele saiu da rota;
- se parou em local proibido;
- se houve abertura de porta;
- se deve haver bloqueio ou acionamento operacional.

O SILD responde:

- se a operação é elegível para prova forte;
- se a origem foi documentada;
- se o lacre observado é o lacre esperado;
- se a chegada preservou coerência;
- se o ator era independente;
- se houve reconciliação;
- se há RPI;
- se há dossiê defensável para glosa ou disputa.

A formulação comercial é:

> **Gerenciamento de risco controla o veículo. O SILD qualifica a confiança da história da carga.**

No piloto, o SILD deve rodar independente. Integrações com GR, TMS, ERP e WMS entram depois da prova de valor.

## 62. Governança financeira e bloqueio de faturamento · [BASE]

O status SILD não deve ser usado como gatilho automático de bloqueio financeiro.

O SILD qualifica a evidência da entrega, organiza a defesa operacional e sinaliza pendências, reconciliações, divergências físicas, RPIs e claims.

A decisão de faturamento, retenção, glosa, cobrança, aceite comercial ou contestação deve permanecer sujeita à política financeira, comercial e contratual da empresa.

A regra é:

> **O SILD informa a qualidade da evidência; ele não substitui a política de faturamento.**

Aplicações corretas:

- priorizar reconciliação antes de disputa;
- acelerar resposta ao cliente;
- anexar dossiê a cobrança contestada;
- separar pendência documental de divergência física;
- abrir RPI quando houver anomalia material;
- preservar direito contra glosa tardia;
- proteger receita com documentação estruturada.

Aplicações incorretas:

- bloquear automaticamente faturamento por qualquer observação técnica;
- tratar Custódia Concluída e Reconciliada como inadimplência operacional;
- transformar status técnico interno em punição financeira automática;
- permitir que exceção de conectividade vire glosa interna sem análise;
- permitir que WMS sem ressalva apague violação física relevante.

O SILD deve reduzir disputa cega, não criar uma nova fila burocrática de bloqueio financeiro.

---

# PARTE VI — COMERCIAL E PILOTO

## 63. Defesa de receita e regresso · [MVP-0]

O SILD deve ser posicionado comercialmente como defesa de receita operacional, mas o discurso precisa respeitar a assimetria de poder dos grandes clientes.

No MVP-0, o SILD não deve prometer vencer glosas contra marketplaces ou varejistas dominantes. Amazon, Mercado Livre, grandes redes e compradores com portal fechado podem ignorar o dossiê do embarcador se seus processos internos registrarem falta ou abatimento.

#### O comprador certo do MVP-0: quem recupera dinheiro com o dossiê

Há uma armadilha comercial a evitar. Se o embarcador grande sangra principalmente em glosas de marketplace, e o MVP-0 admite que não vence essas glosas, é legítimo perguntar: quem paga e por quê? A resposta deve ser explícita, não subentendida.

O MVP-0 deve ser vendido, em primeiro lugar, como **defesa de regresso contra transportadora e instrução de sinistro junto à seguradora** — os dois fluxos em que o dossiê de saída tem efeito financeiro direto e imediato:

1. **Apoio ao regresso contra transportadora.** Quando há falta, avaria ou desvio atribuível ao trecho de transporte, o embarcador que possui evidência de saída lacrada e vinculada à NF chega à negociação com prova organizada, em vez de começar do zero. O dossiê **apoia** o pleito de regresso e a discussão de desconto de frete; ele não garante o resultado, que depende de contrato, circunstâncias e análise jurídica. Mas, diferentemente da glosa de marketplace, esse é um terreno bilateral onde a evidência tem peso real.

2. **Apoio à instrução de sinistro.** Seguradoras de carga avaliam o estado de saída ao analisar sinistro. Um dossiê de origem estruturado organiza a evidência disponível para essa instrução e pode compor a eventual cadeia de sub-rogação, conforme análise jurídica aplicável. O SILD não promete liberação mais rápida nem precificação melhor; ele entrega prova organizada a um interlocutor que já valoriza prova.

A regra de prudência é:

> **O SILD não promete resultado jurídico, desconto de prêmio, aceite automático de seguradora ou aceleração garantida de sinistro. Ele organiza a cadeia probatória de suporte para regresso, instrução de sinistro, auditoria e eventual sub-rogação, conforme análise jurídica aplicável.**

A anti-glosa de marketplace e a defesa comercial interna são **benefícios secundários** do mesmo dossiê — reais, mas não a tese de venda. Vender o MVP-0 prioritariamente como "ganhe da Amazon" prepara a frustração; vender como "chegue à mesa de regresso e de sinistro com prova organizada" entrega valor verificável no primeiro ciclo.

A tese inicial, então, é:

> **Quando a glosa chega, o embarcador não começa do zero. Ele já tem a evidência de saída organizada e vinculada à NF, pronta para apoiar regresso contra a transportadora e instrução de sinistro — e, secundariamente, para sustentar defesa comercial e contestação.**

O MVP-0 serve principalmente para:

- **apoiar o pleito de regresso contra transportadora** (tese primária);
- **organizar evidência para instrução de sinistro** (tese primária);
- reduzir caça manual a canhotos, fotos, WhatsApp, e-mails e comprovantes;
- montar dossiê de saída em minutos;
- organizar defesa interna diante do financeiro;
- qualificar negociação comercial com cliente difícil;
- preservar evidência de origem para glosa tardia.

A formulação comercial correta do MVP-0 é:

> **Da glosa recebida ao dossiê de regresso e sinistro em minutos.**

> **Foto de saída, serial do lacre, NF e glosa financeira no mesmo dossiê.**

> **O SILD não obriga o marketplace a aceitar sua versão; ele impede que sua equipe comece a defesa sem prova organizada e apoia o pleito de regresso e a instrução de sinistro com evidência estruturada.**

Para ciclos posteriores, com Symmetry, G2 Lite, RPI completa e integrações, a promessa pode evoluir para defesa de receita mais ampla, inclusive contra portais e marketplaces.

## 64. Promessa comercial do MVP-0 · [MVP-0]

A promessa do MVP-0 deve ser estreita, mensurável e honesta.

O MVP-0 não promete:

- Confiança Zero plena;
- prova forte de destino;
- vitória automática contra marketplace;
- detecção de fraude;
- validação de conteúdo interno;
- redução imediata do volume total de trabalho administrativo;
- reconciliação automática de imagens;
- Fast Track;
- simetria origem-destino.

O MVP-0 promete:

- registrar evidência mínima de saída;
- vincular evidência a NF, pedido ou manifesto;
- importar glosa em template SILD;
- cruzar glosa com operação capturada;
- gerar dossiê de defesa/regresso;
- reduzir o tempo de reconstrução manual;
- criar linha de base para evolução probatória.

A frase comercial é:

> **Antes de provar a cadeia inteira, o SILD prova que consegue transformar uma saída fotografada e uma glosa recebida semanas depois em um dossiê de defesa em minutos.**

A redução de retrabalho administrativo vem depois da estabilização do processo. No primeiro ciclo, o indicador principal é o tempo para montar um dossiê defensável.

## 65. Playbook de reunião comercial · [MVP-0]

A primeira reunião deve começar pela dor operacional do Diretor de Logística, não por tecnologia, criptografia, score ou integração.

Abertura recomendada:

> **Toda entrega contestada vira uma investigação improvisada. O SILD transforma essa investigação em dossiê automático.**

Sequência de abordagem:

1. Perguntar qual rota, cliente ou CD mais exige reconstrução de entrega.
2. Identificar se a dor é G1, G2 Lite ou glosa financeira tardia.
3. Explicar que o piloto não exige integração de TI no dia zero.
4. Explicar que o motorista terceirizado não usa app, não faz login e não produz prova.
5. Explicar que, no MVP-0, o pátio controlado captura a saída. Em ciclos com Symmetry, o CD próprio ou destino cooperativo pode capturar a chegada.
6. Explicar que marketplaces podem começar por Claim Intake, sem API.
7. Explicar que o SILD não garante aceite automático de grandes clientes, mas melhora a posição de negociação.
8. Propor piloto de 30 dias em uma rota, cliente ou CD com linha de base na primeira semana.

Perguntas úteis:

- qual cliente mais contesta entrega;
- qual rota mais exige busca manual de comprovantes;
- onde o canhoto mais falha;
- onde o lacre mais gera discussão;
- onde há glosa por falta de pallet, caixa ou SKU;
- qual CD ou portaria consegue capturar chegada com menor atrito;
- como o financeiro recebe chargebacks e abatimentos;
- em quanto tempo o cliente costuma cobrar faltas internas.

Frases de apoio:

> **O SILD não cria divergência. Ele organiza sua defesa antes que a divergência vire cobrança.**

> **O motorista rotativo não é validador. O pátio e o CD são as testemunhas controladas da custódia.**

> **O marketplace não precisa abrir API para o piloto começar. A glosa que chega ao financeiro já pode virar evento SILD.**

## 66. Valor contra canhoto tradicional · [MVP-0]

O canhoto tradicional é binário. O SILD é diagnóstico.

O canhoto diz que alguém recebeu.

O SILD mostra:

- o que saiu;
- de onde saiu;
- com qual lacre;
- em qual veículo;
- por qual operador;
- em qual horário;
- se chegou com lacre compatível;
- quem confirmou;
- se houve reconciliação;
- se houve RPI;
- se houve colisão probatória;
- se houve glosa vinculada;
- quais evidências sustentam o fechamento.

O SILD não substitui necessariamente o canhoto. Ele mostra se o encerramento da entrega merece confiança.

A frase comercial é:

> **O canhoto encerra a entrega. O SILD qualifica a confiança do encerramento.**

## 67. Separação entre arquitetura-alvo, MVP técnico e piloto comercial · [BASE]

O SILD deve separar claramente três coisas.

### Arquitetura-alvo

A arquitetura-alvo deste documento descreve o mapa completo de campo e a transição para padrão global: PACC Lite, SILD Hub, Symmetry, G2 Lite, PIP Duplex Lite, RPI completa, Claim Intake avançado, Fast Track, Mesa Humana, cold storage, legal hold e inteligência futura.

### MVP técnico

O MVP técnico é o conjunto mínimo de módulos, regras, estados e controles que permite ao sistema provar uma hipótese específica.

No ciclo zero, essa hipótese é:

> **uma evidência de saída pode ser vinculada a uma glosa posterior e gerar um dossiê de defesa melhor que a investigação improvisada atual?**

### Piloto comercial

O piloto comercial é o recorte controlado de aplicação desse MVP em uma rota, cliente, CD ou fluxo de glosa específico.

A regra é:

> **Arquitetura-alvo orienta o futuro. MVP técnico valida capacidade do produto. Piloto comercial valida valor em uma operação real.**

Essa separação evita dois erros:

- tratar o piloto como se fosse o produto final;
- vender uma transformação sistêmica antes de provar o gesto operacional mínimo.

## 68. Roadmap de MVPs · [MVP-0 → PADRÃO]

O SILD deve evoluir por camadas de produto, não por implementação simultânea de toda a arquitetura.

### MVP-0 — Auditoria de Saída e Defesa de Regresso

Objetivo:

> **Reduzir o custo e o tempo de reconstrução de evidências quando uma entrega sofre glosa, abatimento, cobrança por falta ou disputa comercial.**

Escopo funcional:

1. Criar operação por NF, pedido ou manifesto.
2. Vincular lacre.
3. Capturar foto aproximada do lacre.
4. Capturar foto de contexto traseiro.
5. Armazenar evidência em registro simples.
6. Importar glosa por template SILD.
7. Cruzar glosa com NF, pedido ou operação.
8. Abrir RPI Lite por claim match.
9. Gerar dossiê de defesa/regresso.

Módulos:

- Console Web;
- Captura simples C0;
- Evidence Register;
- Claim Intake por template único;
- Dossiê PDF.

Fora do MVP-0:

- PACC Lite obrigatório;
- SILD Hub;
- G2 Lite;
- PIP Duplex Lite;
- WebSnap;
- Symmetry obrigatória;
- Fast Track;
- Mesa Humana formal;
- cold storage;
- ciclo completo de RPI;
- EDI;
- API;
- inteligência visual;
- ledger imutável avançado.

### MVP-1 — Captura Atestada

Adiciona:

- PACC Lite;
- captura C1/C2;
- câmera direta;
- bloqueio de galeria quando viável;
- reason codes de qualidade;
- RPI Lite melhorada;
- relatório de evidência mais forte.

### MVP-2 — Symmetry e G2 Lite

Adiciona:

- destino próprio ou cooperativo;
- Symmetry;
- G2 Lite;
- PIP Duplex Lite;
- Pallet Registry;
- captura por face A/B;
- eventos de captura após descarga;
- regras de claim por pallet ou SSCC.

### MVP-3 — Plataforma Probatória

Adiciona:

- SILD Hub;
- RPI completa;
- Mesa Humana formal;
- Fast Track documental e, posteriormente, visual validado;
- Storage Lifecycle Manager;
- cold storage;
- legal hold;
- conectores EDI/SFTP/API;
- inteligência operacional inicial de recorrência, limitada ao próprio ambiente do cliente.

### MVP-4 — SILD Standard & Certification

Adiciona:

- schemas oficiais do SILD Protocol;
- SILD Evidence Object versionado;
- níveis de conformidade SILD L0–L5;
- testes de conformidade;
- certificação de lacres, PIP Kits, dispositivos, docas, hubs e integrações;
- certificação de dossiês probatórios;
- API pública ou controlada do protocolo;
- homologação de integradores;
- auditoria de aderência ao padrão.

### MVP-5 — Federated Network Intelligence

Adiciona:

- inteligência agregada e privacidade-preservada;
- recorrência restrita multicliente quando juridicamente permitida;
- degradação de nós logísticos;
- sinais de risco por padrão de evidência;
- exigência probatória progressiva;
- governança de uso externo;
- relatórios institucionais não acusatórios;
- direito de contestação;
- controles contra blacklist opaca.

### MVP-6 — Global Custody Standard

Adiciona:

- adaptação multimodal;
- equivalência documental por país;
- linguagem contratual de conformidade SILD;
- adoção por seguradoras, grandes embarcadores e operadores globais;
- integração com auditorias independentes;
- relatórios aceitos por políticas internas de risco, seguro e compliance;
- interoperabilidade internacional de evidência de custódia;
- governança institucional do padrão.

A regra é:

> **O SILD só sobe de camada quando a camada anterior provar valor operacional e comercial.**

## 69. Piloto comercial recomendado para MVP-0 · [MVP-0]

O piloto inicial deve durar 30 dias e operar em uma rota, cliente, CD ou fluxo de glosa controlado.

### Semana 1 — Linha de base

A equipe observa o processo atual sem alterar a operação.

Mede:

- tempo de liberação;
- qualidade dos canhotos;
- frequência de lacres não fotografados;
- **qualidade real dos lacres existentes do cliente;**
- **taxa de QR/serial ilegível dos lacres atuais, antes de exigir qualquer troca de insumo;**
- tempo para localizar evidência;
- tipos de divergência;
- retrabalho de reconstrução;
- fluxo real de pátio;
- glosas recebidas no financeiro;
- **tempo de preparação da glosa pelo financeiro (fricção humana);**
- prazo médio entre entrega e contestação;
- custo de reconstrução de dossiê.

### Semanas 2 a 4 — MVP-0 em operação

Na origem:

- operação criada por NF, pedido ou manifesto;
- lacre vinculado no ponto físico de fechamento;
- foto aproximada do lacre capturada;
- foto de contexto traseiro capturada;
- evidência registrada no Evidence Register.

No financeiro ou backoffice:

- glosa importada no template SILD;
- claim vinculado a NF, pedido ou operação;
- RPI Lite aberta por claim match;
- dossiê de defesa/regresso gerado.

Resultado do piloto:

- tempo médio de captura C0;
- **tempo do upload do template válido ao PDF (tempo core do software);**
- taxa de operações capturadas sem atrasar pátio;
- taxa de evidências mínimas completas;
- **taxa de `manual_seal_entry`;**
- **taxa de dossiês com ressalva;**
- taxa de glosas importadas com sucesso;
- taxa de glosas vinculadas a operações capturadas;
- número de casos em que o SILD substituiu busca manual por canhoto, print, ligação ou WhatsApp;
- utilidade do dossiê para transportadora, seguro, financeiro ou auditoria.

O resultado deve **separar três falhas distintas**: falha do software, falha do lacre (insumo/legibilidade) e falha do processo financeiro (preparação da glosa). Misturá-las leva a conclusões erradas sobre o produto.

O piloto MVP-0 não deve medir sucesso por Symmetry, Fast Track, G2 Lite, PACC válido ou cold storage. Essas métricas pertencem a ciclos posteriores.

## 70. Critérios de inviabilidade do piloto · [MVP-0]

Nem toda operação deve receber piloto SILD no estágio inicial.

O piloto deve ser recusado, adiado ou redesenhado quando:

- a carga não sai lacrada;
- não há origem controlada;
- não há operador de pátio disponível para captura;
- não há documento mínimo associável à operação;
- o fluxo físico não permite captura traseira mínima;
- o destino é o foco principal da disputa, mas não aceita nenhuma confirmação;
- o cliente quer resolver falta interna de pallet ou caixa sem granularidade G2 ou G3;
- o embarcador espera prova de conteúdo interno sem inspeção material;
- a operação é last-mile capilar não cooperativa;
- a carga muda de unidade logística sem registro mínimo;
- o piloto depende de integração de TI que não estará disponível no prazo;
- a empresa pretende usar o status SILD como bloqueio financeiro automático;
- não há responsável interno para tratar reconciliações;
- não há responsável por importar glosas no Claim Intake;
- em ciclos posteriores, a taxa de mídia cega projetada inviabiliza Fast Track;
- em ciclos posteriores, a taxa de RPI projetada inviabiliza a Mesa Humana;
- em ciclos posteriores, o custo do PIP exigido é incompatível com a margem;
- o WMS ou portal do cliente só fornece baixa genérica sem NF, pedido ou referência comercial mínima.

A regra é:

> **O SILD deve começar onde há chance real de produzir evidência útil.**

Se a dor principal está no destino, o piloto deve incluir Symmetry. Se a dor principal está dentro do pallet, o piloto deve elevar a granularidade. Se a dor principal é conteúdo interno, o SILD precisa de inspeção ou integração material adicional.

## 71. Métricas de sucesso · [MVP-0 + ALVO]

As métricas devem respeitar o estágio do produto.

### Métricas do MVP-0

As métricas do MVP-0 separam **fricção humana** de **eficiência do software**, porque misturá-las distorce a leitura comercial do piloto.

Tempo, em duas medidas distintas:

- `human_claim_preparation_time` — **tempo humano de preparação** da glosa bruta para o template SILD, que é processo do cliente;
- `sild_template_upload_to_pdf_time` — **tempo core do software**, do upload do template válido ao PDF do dossiê.

O "tempo total da glosa bruta ao dossiê" **não** deve ser usado como métrica comercial isolada; ele serve apenas como métrica diagnóstica do processo do cliente, porque embute a fricção humana acima.

Demais métricas do MVP-0:

- tempo médio de captura C0;
- `origin_capture_completion_rate` — taxa de operações com evidência mínima completa (lacre + foto de lacre + foto de contexto);
- taxa de operações com lacre vinculado;
- **distribuição do método de vínculo do lacre: QR, código de barras, NFC, manual, não verificado;**
- `manual_seal_entry_rate` — taxa de entrada manual de serial;
- `seal_not_verified_rate` — taxa de lacre não verificável;
- `qr_read_success_rate` — taxa de leitura automática bem-sucedida;
- taxa de capturas que não travaram a fila;
- taxa de glosas importadas no template SILD;
- `claim_template_rejection_rate` — taxa de linhas rejeitadas no template;
- `claim_auto_match_rate` — taxa de match automático glosa↔operação (alvo de saúde do piloto a definir na linha de base);
- `claim_pending_export_rate` — taxa de linhas exportadas como pendência;
- taxa de novo upload após correção externa;
- **taxa de glosas em `claim_without_matching_origin_evidence` (quanto menor, melhor);**
- **distribuição da chave usada no match (NF / NF+série+CNPJ / pedido+CNPJ / referência);**
- taxa de glosas vinculadas a operação capturada;
- taxa de dossiês com ressalva (`origin_evidence_registered_with_observation`);
- redução do tempo de caça manual a evidências;
- número de dossiês usados para transportadora, seguro, auditoria ou financeiro;
- **número de dossiês que apoiaram regresso contra transportadora ou instrução de sinistro (indicador de utilidade probatória real, sem prometer resultado jurídico);**
- aceitação operacional pelo pátio.

A métrica principal do MVP-0 é:

> **reduzir o tempo de reconstrução de evidência quando chega uma glosa — medido pelo tempo core do software, não pelo tempo total que embute a preparação humana.**

A métrica de saúde estrutural do MVP-0 é:

> **a taxa de match automático glosa↔operação. Se ela for baixa na linha de base, o problema não é o produto, é a qualidade da referência fornecida pelo cliente — e isso precisa ser endereçado no desenho do template e na cascata de normalização antes de escalar o piloto.**

### Métricas dos ciclos posteriores

- tempo p50 de captura;
- tempo p95 de captura;
- taxa de PACC válido;
- taxa de Saída Validada;
- taxa de Saída Validada Localmente;
- taxa de mídia cega;
- taxa de captura por face A/B;
- taxa de PIP legível;
- taxa de etiquetas danificadas por atrito;
- taxa de reconciliação automática;
- taxa de reconciliação humana;
- taxa de Fast Track negado por recorrência restrita;
- taxa de chegada validada;
- taxa de RPIs por 1.000 pallets;
- percentual de RPI baixa, média e crítica;
- percentual de mídia movida para cold storage;
- impacto no tempo de liberação.

No primeiro ciclo, não se deve medir sucesso pela redução imediata de horas administrativas totais. O indicador mais relevante é a redução do tempo de resposta e a melhora da qualidade da defesa quando a entrega é contestada.

## 72. Arquitetura mínima do MVP-0 · [MVP-0]

A arquitetura mínima do MVP-0 deve ser pequena.

### Console Web

Criação simples de operação por NF, pedido, manifesto ou entrada mínima.

### Captura C0

Captura simples de foto do lacre e foto de contexto traseiro, com vínculo à operação.

### Evidence Register

Registro simples de evidência operacional em banco de dados comum, preparado para evoluir para Custody Ledger append-only.

No MVP-0, não é necessário implementar ledger avançado. O sistema deve registrar:

- operação;
- documento;
- lacre;
- mídia;
- hash simples;
- usuário;
- data e hora;
- vínculo com glosa;
- dossiê gerado.

### Claim Intake por template único

Upload CSV/XLSX no modelo SILD.

### Dossiê PDF

Geração de relatório de defesa/regresso com operação, lacre, mídia, glosa vinculada e conclusão factual.

### RPI Lite

Flag documental aberta por claim match. No MVP-0, a RPI Lite não possui ciclo de vida completo.

Módulos que pertencem à arquitetura-alvo, mas não ao MVP-0:

- SILD Snap App completo;
- SILD PACC Lite;
- SILD Hub / Local Anchor;
- SILD Seal Registry avançado;
- SILD Pallet Registry;
- SILD PIP Duplex Lite;
- SILD Custody Ledger append-only avançado;
- SILD Reconciliation Engine;
- SILD RPI Manager completo;
- SILD Storage Lifecycle Manager;
- SILD Network Intelligence.

## 73. Eventos mínimos do backend · [MVP-0 + ALVO]

O backend do MVP-0 deve registrar poucos eventos discretos, auditáveis e suficientes para gerar dossiê.

Eventos mínimos do MVP-0:

```text
operation_created
manifest_or_nf_linked
closure_point_reached
seal_bound                 (só nasce no ponto físico de fechamento)
seal_read_failed           (quando a leitura automática falha)
invalid_pre_scan_blocked   (tentativa de leitura fora do fechamento)
origin_media_captured
origin_capture_confirmed
claim_file_imported
commercial_claim_received
claim_line_rejected
claim_linked_to_origin_evidence
claim_line_pending_exported
defense_dossier_generated
```

A regra de `seal_bound` é dura: ele **só** é emitido quando o lacre já está instalado no ponto físico de fechamento. Leitura prévia nunca gera `seal_bound`; gera `invalid_pre_scan_blocked`.

No MVP-0, não há evento automático de RPI durante a jornada. A RPI Lite nasce apenas quando há claim match.

Evento derivado opcional:

```text
rpi_lite_opened_by_claim_match
```

Eventos da arquitetura-alvo, para ciclos posteriores:

- `manifest_scanned`;
- `manifest_uploaded`;
- `origin_snap_started`;
- `pacc_session_started`;
- `pacc_nonce_issued`;
- `pacc_anchor_detected`;
- `frame_freeze_captured`;
- `clip_context_captured`;
- `sild_hub_nonce_issued`;
- `local_validation_completed`;
- `rear_plate_captured`;
- `seal_image_captured`;
- `seal_mechanical_integrity_captured`;
- `origin_context_captured`;
- `arrival_snap_started`;
- `arrival_plate_captured`;
- `arrival_seal_captured`;
- `arrival_condition_recorded`;
- `arrival_snap_confirmed`;
- `pallet_label_a_captured`;
- `pallet_label_b_captured`;
- `stretch_closure_captured`;
- `pip_duplex_lite_applied`;
- `pallet_face_unavailable_in_trailer`;
- `capture_after_unload_recorded`;
- `physical_tamper_detected`;
- `media_blindness_detected`;
- `reconciliation_opened`;
- `reconciliation_auto_closed`;
- `rpi_opened`;
- `rpi_critical_action_triggered`;
- `rpi_observation_started`;
- `cooling_off_period_started`;
- `claim_linked_to_rpi`;
- `rpi_strengthened_by_claim`;
- `rpi_closed_no_claim_received`;
- `rpi_media_moved_to_cold_storage`;
- `legal_hold_applied`.

Cada evento deve conter, quando aplicável:

- ID da operação;
- ator;
- dispositivo;
- canal;
- horário de servidor;
- hash da mídia;
- vínculo com evento anterior;
- reason code;
- status interno;
- status externo.

A regra é:

> **O MVP-0 registra o mínimo necessário para defender uma glosa. A arquitetura-alvo registra a cadeia de custódia completa.**

## 74. Reason codes internos · [MVP-0 + ALVO]

O MVP-0 deve começar com poucos reason codes.

Reason codes do MVP-0:

Captura e lacre:

- `origin_evidence_registered`;
- `seal_photo_captured`;
- `context_photo_captured`;
- `seal_read_success` — leitura automática (QR/código/NFC) bem-sucedida no ponto de fechamento;
- `seal_read_failed` — tentativa de leitura automática falhou (substitui o antigo `seal_unreadable`);
- `manual_seal_entry` — serial digitado manualmente no ponto de fechamento;
- `seal_not_verified` — lacre não verificável (sem leitura e sem serial útil);
- `invalid_pre_scan_blocked` — tentativa de leitura fora do ponto de fechamento, não vincula;
- `manual_entry_pending_visual_audit` — entrada manual com foto ainda não auditada;
- `manual_entry_visual_confirmed` — auditoria posterior confirmou suporte visual do serial;
- `manual_entry_visual_blind` — auditoria posterior indicou foto cega;
- `origin_evidence_registered_with_observation` — status externo com ressalva;
- `origin_evidence_incomplete` — evidência de origem incompleta.

Glosa e dossiê:

- `claim_template_imported`;
- `claim_line_rejected` — linha malformada no template;
- `claim_linked_to_origin_evidence`;
- `claim_line_pending_exported` — pendência exportada em CSV para correção externa;
- `rpi_lite_opened_by_claim_match`;
- `defense_dossier_generated`;
- `claim_without_matching_origin_evidence`.

Nota de taxonomia: o `seal_read_failed` substitui o antigo `seal_unreadable`; não devem coexistir. Os códigos de lacre acima formam a taxonomia única do MVP-0, alinhada com o campo `seal_bind_method` e a matriz de estados de lacre da seção 22.

Reason codes da arquitetura-alvo:

- `origin_snap_validated`;
- `rear_plate_captured`;
- `seal_captured`;
- `seal_reused`;
- `seal_cancelled`;
- `seal_mechanical_integrity_observed`;
- `seal_mechanical_integrity_missing`;
- `gallery_upload_blocked`;
- `offline_expected`;
- `offline_reconciled`;
- `offline_suspicious`;
- `device_reboot_detected`;
- `arrival_snap_validated`;
- `arrival_context_missing`;
- `arrival_actor_not_independent`;
- `legacy_only_insufficient`;
- `auto_reconciled_via_wms`;
- `manual_reconciliation_required`;
- `driver_controlled_evidence_rejected`;
- `destination_app_authenticated`;
- `websnap_geolocation_missing`;
- `websnap_outside_geofence`;
- `custody_reconciled`;
- `custody_divergent`;
- `media_blur_or_low_light`;
- `media_blindness`;
- `label_damaged_by_friction`;
- `pallet_qr_unreadable`;
- `pallet_label_a_read`;
- `pallet_label_b_read`;
- `stretch_closure_intact`;
- `pip_duplex_lite_applied`;
- `pallet_face_unavailable_in_trailer`;
- `capture_after_unload_with_observation`;
- `stretch_cut_detected`;
- `stretch_rewrapped`;
- `closure_lock_detached`;
- `pallet_id_mismatch`;
- `physical_tamper_conflicts_with_wms`;
- `claim_received_within_window`;
- `claim_received_after_window`;
- `cooling_off_period_started`;
- `rpi_closed_without_claim`;
- `claim_intake_file_hash_recorded`.

Reason codes devem ser legíveis por operação, auditoria, suporte e produto.

## 75. Segurança, LGPD e direito de imagem · [BASE]

Todas as fases do SILD devem seguir minimização de dados.

Regras:

- não coletar rosto do motorista;
- não exigir selfie;
- não usar biometria;
- não instalar app no celular pessoal do motorista;
- não fotografar CNH como rotina;
- não transformar trabalhador terceirizado em objeto biométrico;
- coletar apenas dados operacionais necessários;
- registrar ativos logísticos, não pessoas sem necessidade;
- autenticar operadores próprios do pátio e do CD;
- controlar acesso às evidências;
- manter retenção proporcional;
- registrar acesso aos dossiês;
- aplicar cold storage quando a finalidade operacional encerrar;
- aplicar legal hold apenas quando houver justificativa.

O motorista terceirizado pode ser identificado pelos meios contratuais e operacionais já existentes, quando necessários, mas o SILD não deve criar uma camada adicional de vigilância pessoal no MVP.

A regra é:

> **O SILD observa ativos de custódia, não rostos de terceiros.**

## 76. Política de retenção e acesso às evidências · [BASE]

A retenção das evidências deve ser proporcional à finalidade operacional, contratual e jurídica.

Diretrizes:

- evidências de operações comuns devem ter prazo de retenção definido em contrato;
- evidências de operações contestadas podem ter retenção ampliada enquanto durar a disputa;
- evidências vinculadas a sinistro, auditoria, seguradora ou litígio devem seguir prazo jurídico aplicável;
- mídias sem valor probatório residual devem ser descartadas, reduzidas ou anonimizadas ao final da finalidade;
- acesso aos dossiês deve ser registrado;
- exportações devem gerar trilha de auditoria;
- usuários devem ter perfis de acesso proporcionais;
- evidências com terceiros, quando inevitáveis, devem ter controle de compartilhamento;
- dados pessoais incidentais devem ser minimizados.

A regra é:

> **O SILD preserva evidência enquanto houver finalidade legítima; depois reduz, anonimiza, esfria ou descarta.**

A retenção não deve transformar o SILD em arquivo indefinido de vigilância operacional.

---

# PARTE VII — PADRÃO, IMPACTO E VISÃO

## 77. Governança do Padrão SILD · [PADRÃO]

Para funcionar como padrão de mercado, o SILD deve possuir governança explícita.

A governança não é ornamento institucional. Ela impede que o protocolo vire mecanismo privado de acusação, vigilância, bloqueio comercial opaco ou blacklist logística.

Componentes recomendados:

### Especificação versionada

O SILD Protocol deve possuir versões públicas ou controladas de schema, eventos, reason codes, níveis de conformidade, critérios de elegibilidade e formato de dossiê.

### Testes de conformidade

Componentes, integrações e operadores devem poder ser testados contra requisitos objetivos: captura mínima, hash, mídia, campos obrigatórios, reason codes, exportação, retenção e controle de acesso.

### Certificação de componentes

Lacres, PIP Kits, dispositivos, docas, hubs, apps, integrações e relatórios podem receber certificação quando atenderem ao nível declarado.

### Auditoria independente

Operações críticas, seguradoras, clientes estratégicos e setores regulados podem exigir revisão independente da conformidade SILD.

### Direito de contestação

Nenhum ator deve ser condenado, bloqueado ou punido automaticamente por indicador SILD. Divergências devem admitir revisão, evidência compensatória e registro de decisão.

### Separação entre evidência, inferência e acusação

O SILD registra evidência e classifica força probatória. Inferências de risco devem ser tratadas como sinais. Acusações de crime, fraude ou responsabilidade pertencem a processos jurídicos, contratuais, periciais ou públicos competentes.

### Proibição de blacklist automática

O protocolo não deve gerar listas negras opacas de motoristas, operadores, transportadoras, destinos ou clientes.

O princípio que rege essa proibição é:

> **Risco aumenta exigência probatória; não substitui prova.**

Sinais recorrentes podem reduzir elegibilidade para Fast Track, exigir captura mais forte, acionar auditoria, ampliar retenção ou solicitar revisão humana. Eles não devem produzir condenação automática.

### Quem governa o padrão: estrutura e fases

Princípios sem entidade que os mantenha não produzem um padrão; produzem uma aspiração. O documento até aqui descreveu *o que* a governança deve impedir, mas não *quem* a exerce. Esta subseção fecha essa lacuna, em fases proporcionais à maturidade.

**Fase 1 — Custódia única do mantenedor (MVP-0 a MVP-3).** No início, é honesto admitir que o schema, os reason codes e o formato de dossiê são mantidos pela empresa fundadora. Isso é normal para um padrão nascente. O que se exige nesta fase é apenas **versionamento público do schema e changelog**, para que integradores e clientes possam acompanhar mudanças sem surpresa. Não há, ainda, pretensão de neutralidade institucional.

**Fase 2 — Comitê técnico com participação externa (MVP-4, junto com a certificação).** Quando o SILD passa a certificar componentes de terceiros, surge a necessidade de um **comitê técnico do protocolo** com assentos para atores que não sejam a empresa: ao menos um embarcador, uma seguradora e um integrador independentes. Esse comitê aprova mudanças de schema, níveis de conformidade e critérios de teste. As decisões e atas devem ser registradas e acessíveis aos certificados.

**Fase 3 — Governança separada da operação comercial (MVP-5/MVP-6, padrão global).** Para que o mercado adote o SILD como padrão neutro, a manutenção do *Protocol* deve ser institucionalmente separada da venda da *Platform*. As formas possíveis incluem um consórcio setorial, uma associação sem fins lucrativos, uma fundação de padrão, ou a doação da especificação a um organismo de padronização existente. A escolha entre essas formas é uma decisão estratégica futura; o que não pode faltar é a **separação**.

### O conflito de interesse que precisa ser nomeado

Há um conflito estrutural que o mercado perceberá de imediato e que, se não for endereçado, impede a adoção como padrão neutro:

> **A mesma empresa que vende a SILD Platform, certifica os componentes e governa o SILD Protocol tem incentivo para escrever o padrão a favor do próprio produto e para certificar de forma a favorecer parceiros comerciais.**

Negar esse conflito não o resolve. A resposta correta é desenhar salvaguardas explícitas:

- **Separação de papéis:** quem mantém a especificação não deve ser a mesma unidade que fecha contratos de Platform. À medida que a Fase 2 e a Fase 3 avançam, essa separação deixa de ser organizacional interna e passa a ser institucional.
- **Especificação aberta o suficiente para implementação independente:** o Protocol deve poder ser implementado por um concorrente sem licença comercial da empresa fundadora. Um padrão que só uma empresa consegue implementar não é padrão; é produto com nome de padrão.
- **Certificação auditável e contestável:** decisões de certificar ou negar certificação devem ter critérios objetivos publicados, registro de decisão e via de contestação. Certificação discricionária e opaca reproduz, no nível do componente, exatamente a blacklist opaca que o protocolo proíbe no nível do ator.
- **Transparência de financiamento do organismo de governança:** quando houver consórcio ou fundação, suas fontes de receita (taxas de certificação, anuidades) devem ser conhecidas pelos membros, para que ninguém possa capturar o padrão por financiamento.

A regra constitucional de governança é:

> **Risco aumenta exigência probatória; não substitui prova. E quem governa o padrão não deve poder usá-lo para vencer no mercado contra quem o implementa de forma conforme.**

Essa disciplina não pertence ao MVP-0 — no ciclo zero, a empresa simplesmente mantém o schema e versiona. Mas a ambição de padrão global declarada nas seções 2, 3 e 36 só é honesta se a estrutura de governança e a separação institucional estiverem desenhadas desde já como destino, não improvisadas quando o conflito explodir.

## 78. Limites técnicos · [BASE]

O SILD possui limites explícitos.

O Origin Snap não prova entrega.

O Arrival Snap não prova conteúdo interno.

O G2 Lite não garante cobertura 360 graus.

Etiqueta A/B não impede violação sofisticada.

Trava de emenda não certifica conteúdo interno.

O lacre comum não prova inviolabilidade sofisticada.

Captura offline não mantém força máxima sem âncora e sincronização.

Foto sem contexto não valida evento.

Sistema legado não cura falha sozinho.

WMS sem ressalva não apaga anomalia física.

Mídia cega não prova ausência de violação.

Reconciliação não apaga lacuna original.

RPI não acusa furto.

Claim Intake não valida automaticamente legitimidade da glosa.

O vínculo de lacre do MVP-0 não resiste a conluio de origem: um operador autenticado que forja a evidência de propósito tem teto probatório limitado, e o dossiê não deve afirmar mais do que "lacre associado ao documento por aquele operador naquele horário".

Entrada manual de serial com foto cega é falha visual de contingência: não comprova o serial e leva a evidência ao teto `origin_evidence_incomplete`.

Motorista terceirizado não é raiz de confiança.

WebSnap anônimo não deve ser usado em destino próprio.

QR de recebimento não pode viajar com a carga.

Cold storage preserva prova, mas pode exigir tempo de restauração.

O SILD não consegue provar ausência de ilícito dentro da carga sem inspeção de conteúdo.

O SILD não impede fraude perfeita em ambiente totalmente comprometido.

O SILD não transforma smartphone em equipamento forense absoluto.

O SILD certifica a qualidade da evidência logística disponível.

## 79. Decisões operacionais por fase · [MVP-0 + ALVO]

As decisões abaixo pertencem à arquitetura-alvo. No MVP-0, as decisões se limitam a registrar evidência, importar glosa, vincular claim e gerar dossiê.

O SILD deve operar com ações proporcionais.

No MVP-0, a resposta operacional pode incluir:

- registrar evidência de saída;
- solicitar nova foto quando a evidência mínima estiver ausente;
- importar glosa no template SILD;
- vincular claim à evidência de origem;
- gerar dossiê de defesa/regresso;
- marcar glosa sem evidência de origem quando não houver match.

Nos ciclos posteriores, a resposta a um evento anômalo pode incluir:

- registrar sem interromper;
- solicitar nova captura;
- exigir segundo sinal físico quando houver mídia cega;
- exigir leitura no destino;
- emitir relatório com status correto;
- abrir pendência de reconciliação;
- aplicar Fast Track automático;
- negar Fast Track por cegueira, recorrência ou falha de integridade;
- acionar Mesa Humana;
- abrir RPI;
- disparar ação imediata quando RPI crítica;
- exigir evidência compensatória;
- reconciliar sem apagar evento original;
- acionar Claim Intake quando houver glosa;
- gerar dossiê de defesa;
- recomendar ajuste de processo;
- escalar para auditoria, jurídico ou seguradora quando necessário.

A regra é:

> **primeiro aumentar evidência; depois aumentar controle; só por último impedir fluxo.**

Isso reduz impacto operacional e responsabilidade civil.

## 80. CTM e mutações topológicas como fase futura · [ALVO]

O **CTM — Controlador de Transição de Modo** permanece como camada futura para operações maduras.

Ele deve gerenciar:

- mudança de topologia;
- Proof Suspenso;
- transbordo;
- fracionamento;
- troca de veículo;
- redirecionamento;
- evidência compensatória;
- split de custódia;
- reclassificação de cadeia.

No MVP Origin Snap e G2 Lite, o CTM completo não deve ser implementado.

A lógica de mutação deve aparecer apenas como exceção simples quando houver divergência entre saída, chegada, reconciliação, RPI ou claim.

## 81. Inteligência de rede como fase futura · [ALVO/PADRÃO]

A inteligência de rede federada não deve fazer parte do MVP. No MVP-3, podem existir sinais internos de recorrência e qualidade operacional restritos ao próprio cliente. A inteligência federada, multicliente, agregada e privacidade-preservada pertence ao MVP-5 ou a fases institucionais posteriores.

NRI, ICE, desvio homólogo, degradação de nós, deslocamento adversarial, recorrência restrita e dossiês institucionais dependem de:

- volume de dados suficiente;
- padronização;
- base contratual;
- governança jurídica;
- segregação de clientes;
- minimização de dados;
- revisão humana;
- direito de contestação;
- controle de uso externo;
- privacidade preservada;
- maturidade dos níveis de conformidade SILD.

A inteligência de rede deve ser orientada por padrões probatórios, não por acusação.

Ela pode medir:

- aumento de mídia cega por rota, doca, destino, dispositivo ou operador;
- recorrência de lacre ilegível;
- captura manual acima do normal;
- concentração de claims após determinado padrão de evidência;
- divergências repetidas por combinação restrita de transportadora, veículo, destino, operador ou doca;
- degradação de qualidade de captura em janelas específicas;
- uso recorrente de contingência;
- incompatibilidade entre baixa sistêmica e evidência física;
- aumento de eventos não elegíveis para Fast Track;
- mudança anômala de topologia operacional.

Esses índices não devem gerar condenação automática, bloqueio automático ou blacklist opaca.

Quando implementados, devem aumentar exigência probatória, orientar auditoria, priorizar revisão, sugerir melhoria operacional, reduzir elegibilidade para automação e gerar dossiês apenas quando houver base adequada.

A inteligência de rede deve ser preferencialmente federada ou agregada quando envolver múltiplos clientes, preservando segredos comerciais, rotas sensíveis, dados pessoais incidentais e informações competitivas.

A regra é:

> **Risco de rede aumenta exigência probatória; não substitui prova.**

## 82. Mecanismo de impacto sobre mercados ilícitos logísticos · [PADRÃO]

O SILD não deve prometer impactar todos os crimes diretamente.

Seu domínio são crimes, fraudes, desvios, disputas e simulações que dependem de cadeias de entrega, eventos de custódia, ativos logísticos, documentos comerciais e narrativas operacionais verificáveis.

Mercados ilícitos que exploram logística lícita dependem de opacidade. Essa opacidade costuma aparecer como:

- evidência fraca;
- lacunas de custódia;
- baixa independência do ator;
- divergência entre documento e objeto;
- falha recorrente de captura;
- lacre não observado;
- mídia cega;
- destino sem contexto;
- baixa sistêmica sem suporte físico;
- claim sem evidência reconciliável;
- mutação logística não documentada.

O SILD não elimina esses mercados. Ele pode degradar sua capacidade de operar dentro da logística lícita sem produzir contradições auditáveis.

O mecanismo causal é:

1. padronizar evidência de custódia;
2. reduzir zonas cegas;
3. tornar lacunas mensuráveis;
4. aumentar exigência probatória em padrões recorrentes de baixa confiabilidade;
5. elevar custo de simulação logística;
6. dificultar manutenção de narrativas falsas entre origem, destino, lacre, documento, ator e claim;
7. produzir dossiês auditáveis para seguro, regresso, compliance, auditoria e autoridades competentes quando aplicável.

A regra é:

> **O SILD não combate crime como polícia. Ele torna a logística lícita mais difícil de ser parasitada por narrativas falsas.**

## 83. Núcleo de Negação Logística Ilícita como visão estratégica · [PADRÃO]

A camada de Negação Logística Ilícita permanece como visão de longo prazo.

Sua função não é punir, fiscalizar, investigar no lugar do Estado ou acusar atores privados. Sua função é reduzir a previsibilidade logística que permite a mercados ilícitos operarem em escala dentro de cadeias formalmente lícitas.

Essa camada atua por degradação estrutural da opacidade logística. Ao aumentar a exigência de evidência em rotas, nós, cargas, operadores, transportadoras, dispositivos, docas e eventos recorrentes de baixa confiabilidade, o SILD reduz a capacidade de redes ilícitas explorarem cadeias lícitas sem produzir contradições auditáveis.

Essa camada só deve surgir depois de o SILD provar sua base operacional:

1. captura de origem;
2. simetria destino;
3. G2 Lite quando a dor exigir granularidade;
4. relatórios confiáveis;
5. reconciliação madura;
6. RPI e Claim Intake operacionais;
7. volume de dados;
8. governança jurídica;
9. inteligência de rede;
10. conformidade e certificação.

A linguagem institucional deve permanecer:

> **Há recorrência logística anômala com base probatória documentada.**

E não:

> **Este nó é criminoso.**

A regra é:

> **A Negação Logística Ilícita aumenta fricção, custo e risco de contradição para narrativas logísticas falsas. Ela não substitui investigação criminal, perícia, fiscalização ou decisão judicial.**

## 84. Multimodal como fase futura · [ALVO]

O SILD deve ser concebido como plataforma potencialmente multimodal, mas a expansão não pertence ao MVP.

O princípio aplicável a todos os modais é:

> **A unidade lógica do SILD é o evento de custódia, não o caminhão.**

Fases futuras podem adaptar o protocolo para:

- rodoviário;
- aéreo;
- marítimo;
- ferroviário;
- intermodal;
- contêineres;
- ULDs;
- vagões;
- terminais;
- cargas especiais e sensíveis.

O MVP-0 deve permanecer rodoviário, lacrado, controlado e orientado por evidência física de baixa fricção.

## 85. Modelo comercial · [MVP-0 → PADRÃO]

O SILD pode operar como SaaS de evidência logística e defesa de receita.

Modelos possíveis:

- cobrança por operação capturada;
- cobrança por pallet ou unidade G2 Lite;
- cobrança por dossiê gerado;
- assinatura mensal por pátio;
- assinatura por embarcador;
- pacote por rota crítica;
- licença por CD;
- cobrança premium para Symmetry;
- módulo RPI & Claim Defense;
- módulo Claim Intake;
- SILD Hub por doca ou pátio;
- PIP Kit por pallet ou volume crítico;
- módulos adicionais para API, WMS, auditoria e relatórios jurídicos.

Pacotes comerciais:

### SILD G1 Custody

Cobrança por viagem ou unidade lacrada.

### SILD G2 Lite Pallet Snap

Cobrança por pallet, gaiola, roll container ou volume crítico.

### SILD RPI & Claim Defense

Cobrança por módulo mensal, por dossiê de glosa ou por volume de claims processados.

### SILD Hub

Cobrança por doca, pátio ou ponto de captura.

### PIP Kit

Insumo físico por pallet, com tiers de risco.

Modelos de monetização de padrão e certificação:

- licença de certificação SILD;
- selo de conformidade por componente;
- auditoria anual de aderência;
- homologação de lacres;
- homologação de PIP Kits;
- homologação de dispositivos;
- homologação de docas e hubs;
- homologação de integradores;
- certificação de relatórios e dossiês;
- API premium de conformidade;
- módulo para seguradoras;
- módulo para auditoria e compliance;
- marketplace de componentes certificados.

### SILD Certified Seal

Certificação de lacres compatíveis com leitura, serialização, zona mecânica observável, lote, controle de reutilização e captura SILD.

### SILD Certified Dock

Certificação de docas, portarias, pontos de captura, hubs ou estações capazes de produzir evidência contextual consistente.

### SILD Certified Carrier

Certificação de transportadoras que aderem a fluxos mínimos de evidência, exceção, reconciliação, preservação e resposta a dossiês.

### SILD Certified Evidence Report

Certificação de relatórios que respeitam linguagem factual, limites probatórios, hashes, trilha de eventos, anexos, status e ausência de acusação automática.

A proposta de valor inicial é:

- reduzir reconstrução manual de entregas;
- fortalecer defesa contra glosas;
- melhorar posição de negociação com clientes difíceis;
- reduzir tempo de resposta a contestação;
- qualificar a confiança do canhoto;
- organizar evidência antes da cobrança;
- reduzir disputa cega;
- proteger receita operacional.

O SILD deve ser vendido como defesa de receita, não como vigilância logística.

## 86. Adoção institucional do SILD · [PADRÃO]

Para se tornar padrão ouro, o SILD deve criar valor diferente para cada ator da cadeia.

### Embarcadores

Usam o SILD para defesa de receita, redução de caça manual a evidências, organização de dossiês, contestação de glosas, acionamento de seguro e direito de regresso.

### Transportadoras qualificadas

Usam o SILD para demonstrar qualidade operacional, reduzir disputas subjetivas, diferenciar serviço premium e responder a claims com evidência estruturada.

### Operadores logísticos

Usam o SILD para padronizar captura em pátio, doca, hub, staging, expedição, recebimento e reconciliação.

### Seguradoras

Usam o SILD para melhorar análise de sinistro, precificação de risco, exigência de evidência, auditoria de recorrência e defesa contra alegações sem lastro.

### Varejistas e marketplaces

Podem usar o SILD para consumir evidência externa padronizada, reduzir conflitos com fornecedores e diferenciar contestação legítima de disputa com evidência fraca.

### Auditores e jurídico

Usam o SILD para acessar trilha de eventos, dossiês, hashes, reason codes, limites probatórios, retenção, legal hold e histórico de exportação.

### Autoridades competentes

Podem receber dossiês mais organizados quando houver base legal ou solicitação apropriada. O SILD não delega fiscalização pública a atores privados.

A regra é:

> **O SILD se torna padrão quando cada ator racional prefere operar com evidência estruturada em vez de disputa narrativa.**

## 87. Segmentação de mercado · [MVP-0]

O SILD deve começar em setores que pagam por prova, disputa e defesa de entrega.

Clientes iniciais adequados:

- embarcadores com alto volume de glosas;
- indústrias que abastecem grandes varejistas;
- farmacêuticas;
- eletrônicos;
- químicos sensíveis;
- cargas de alto valor;
- operadores com CD próprio;
- seguradoras de carga;
- transportadoras premium;
- operadores com rotas críticas;
- empresas com alto custo de contestação;
- operações hub-to-hub controladas;
- operações fracionadas com palletização controlada;
- embarcadores expostos a chargebacks de marketplace.

O SILD não deve começar pela logística genérica de baixa margem nem pelo last-mile capilar não cooperativo.

## 88. Formulação institucional revisada · [BASE]

O SILD pode ser apresentado em quatro camadas.

### Formulação do padrão global

> **O SILD é um padrão progressivo de evidência de custódia para cadeias de entrega. Ele define como eventos logísticos devem ser registrados, classificados, reconciliados, certificados e preservados, permitindo que embarcadores, transportadores, destinatários, seguradoras, auditores, sistemas legados e operadores logísticos usem uma linguagem comum de confiança operacional.**

### Formulação da arquitetura-alvo

> **O SILD é um protocolo progressivo de evidência logística baseado em Confiança Zero. Ele mede a força da narrativa logística de uma carga, combinando evidência física, contexto, ator, dispositivo, documento, reconciliação comercial e dossiê auditável. Quando a operação permite, evolui para PACC Lite, simetria origem-destino, G2 Lite, RPI, Claim Intake, Fast Track, certificação e inteligência de rede. O sistema não promete detectar todo ilícito; ele mede a força da evidência que sustenta a história logística, reduz disputas cegas, organiza a defesa da entrega e torna a mentira logística mais difícil de sustentar sem contradições.**

### Formulação do MVP-0

> **O SILD MVP-0 registra a evidência mínima de saída da carga, vincula essa evidência à NF, pedido ou manifesto e, quando uma glosa chega ao financeiro, gera um dossiê de defesa ou regresso. Ele não implementa Confiança Zero plena, não prova destino e não obriga marketplace a aceitar a versão do embarcador. Seu primeiro valor é reduzir a caça manual a evidências e acelerar a defesa contra glosas, seguros e cobranças de transportadora.**

### Formulação da camada de impacto ilícito

> **O SILD não combate crime como polícia. Ele reduz a capacidade de mercados ilícitos parasitarem cadeias logísticas lícitas por meio de narrativas falsas, lacunas de custódia e evidências fracas. Em escala institucional, o SILD aumenta o custo de simulação logística, reduz zonas cegas e torna contradições mais mensuráveis, contestáveis e auditáveis.**

## 89. Valor unilateral antes da rede · [BASE/MVP-0]

Muitos projetos que se anunciam como "padrão" morrem no problema do ovo e da galinha: ninguém adota porque ninguém adotou. Um padrão que só gera valor quando muitos atores já o usam fica preso à ausência de massa crítica. Isso mata efeitos de rede antes que eles comecem.

O SILD escapa dessa armadilha por um motivo que precisa ser dito explicitamente, porque é a maior força estratégica do projeto:

> **O SILD entrega valor a um único ator, sozinho, antes de existir qualquer rede. Um embarcador que captura a saída e gera dossiê de regresso ganha imediatamente, mesmo que nenhuma transportadora, marketplace, seguradora ou outro embarcador use SILD.**

O MVP-0 não precisa de adoção de terceiros para funcionar. Ele não depende de o destino cooperar, de o marketplace abrir API, de a transportadora se certificar ou de outro embarcador estar na rede. O ganho — reduzir caça manual a evidências e organizar regresso e sinistro — é **unilateral**.

Isso inverte a lógica de adoção. Em vez de "o SILD vale quando todos usarem", a tese é:

> **O SILD vale para você mesmo que você seja o único a usar. A rede é um bônus posterior, não um pré-requisito.**

As consequências estratégicas:

- **Venda não depende de convencer o ecossistema.** Cada embarcador é um caso de uso fechado em si mesmo. Não há necessidade de coordenar múltiplas partes para a primeira venda.
- **O efeito de rede vem depois e por cima.** Quando muitos embarcadores já usam SILD por valor próprio, surge naturalmente a camada de linguagem comum, certificação e inteligência — mas como segunda onda, não como aposta inicial.
- **O padrão emerge, não é decretado.** O SILD não vira padrão porque alguém declarou que é. Vira padrão porque acumulou massa de atores que adotaram por interesse unilateral e passaram a preferir sua gramática de evidência.

A regra é:

> **Padrão é efeito de rede; efeito de rede é consequência de valor unilateral repetido. Primeiro o valor isolado, muitas vezes; depois a rede; só então o padrão.**

Toda decisão de roadmap deve passar por este filtro: a próxima funcionalidade gera valor para um ator sozinho, ou só gera valor se a rede já existir? Funcionalidades do primeiro tipo são seguras; funcionalidades do segundo tipo só entram depois que a base instalada justificar.

## 90. Seguradora como âncora de adoção · [MVP-0 → PADRÃO]

Padrões raramente se espalham por superioridade técnica. Espalham-se quando um ator com poder de barganha passa a exigi-los. Esse ator é a **âncora de adoção**: quem, ao adotar, arrasta os demais.

No SILD, a âncora natural é a **seguradora de carga**, e isso tem fundamento jurídico concreto no Brasil, não apenas conveniência comercial.

### Por que a seguradora, e não o embarcador isolado

O embarcador adota o SILD por valor unilateral (seção 89), mas ele não tem poder para impor o padrão à cadeia. A seguradora tem. Quando uma seguradora condiciona prêmio, cobertura ou aceitação de sinistro à existência de evidência estruturada de custódia, ela move embarcadores e transportadores de uma só vez, porque ambos dependem da apólice.

### O fundamento jurídico que torna a evidência valiosa para o seguro

No direito brasileiro, paga a indenização, a seguradora se sub-roga nos direitos do segurado contra o causador do dano. O art. 786 do Código Civil estabelece que, paga a indenização, o segurador se sub-roga, nos limites do valor respectivo, nos direitos e ações que competirem ao segurado contra o autor do dano. Isso significa que a seguradora, depois de pagar o embarcador, vai cobrar a transportadora em ação regressiva — e o sucesso dessa ação depende de prova.

A jurisprudência reforça o valor da prova. Conforme entendimento consolidado, o roubo de carga em transporte terrestre não é automaticamente fortuito externo capaz de romper o nexo causal; é cabível o direito de regresso quando as circunstâncias fáticas o autorizam, ainda que exista cláusula de renúncia, nas hipóteses de agravamento do risco ou culpa do transportador. A eficácia da defesa do transportador depende estritamente da observância das cláusulas de gerenciamento de risco, e cai por terra diante de prova de culpa grave ou dolo.

A leitura estratégica é direta: tudo gira em torno de **prova de cumprimento de protocolo e de estado da carga**. É exatamente o que o SILD produz. Um dossiê SILD de saída, com lacre serializado vinculado à NF, horário, operador e contexto, é matéria-prima para:

- a seguradora avaliar e precificar risco com mais informação;
- a seguradora sustentar regresso contra o transportador com prova organizada;
- o embarcador demonstrar que cumpriu protocolo de saída;
- distinguir sinistro legítimo de alegação sem lastro.

### O mecanismo de âncora

Esta seção descreve o fundamento jurídico do *porquê* a seguradora valoriza a prova — não um argumento de venda. O art. 786 e a jurisprudência citados explicam por que evidência organizada importa no regresso e na sub-rogação; eles não devem ser usados como promessa comercial direta ao cliente. A regra de prudência da seção 63 vale aqui integralmente: o SILD não promete resultado jurídico, desconto de prêmio, aceite automático nem aceleração garantida de sinistro.

A sequência de adoção via seguradora, descrita como hipótese de mercado de médio prazo, é:

1. O SILD demonstra, em pilotos, que dossiês estruturados organizam melhor a evidência para análise de sinistro e para o pleito de regresso.
2. Seguradoras **podem** passar a oferecer condição diferenciada — por exemplo, exigência reduzida de outras cautelas, ou tratamento preferencial de carga com evidência SILD — a seu próprio critério. Qualquer benefício de prêmio ou de prazo é decisão da seguradora, não promessa do SILD.
3. Essa condição, se ocorrer, cria pressão de mercado: embarcadores querem o benefício, transportadores se adequam para manter contratos.
4. A linguagem SILD de evidência tende a virar referência contratual entre embarcador, transportador e seguradora.

A regra é:

> **O embarcador adota o SILD por valor próprio. A seguradora pode transformar esse valor próprio em pressão de cadeia. O SILD organiza a prova; ele não promete a consequência jurídica ou comercial dessa prova.**

### O que isso exige do produto

Para que a seguradora seja âncora, o SILD precisa, em ciclos posteriores ao MVP-0:

- formato de dossiê reconhecível e estável, com hashes, trilha de eventos e limites probatórios claros;
- linguagem factual e não acusatória, compatível com uso em sinistro e regresso;
- retenção e legal hold compatíveis com prazos de ação regressiva;
- mapeamento entre reason codes e categorias de risco que a seguradora já usa.

Nenhum desses requisitos pertence ao MVP-0. Mas todos devem ser antecipados no desenho do Evidence Object e do dossiê, para que a âncora seguradora seja possível quando o volume permitir.

## 91. Ameaças ao próprio protocolo · [BASE]

Um padrão de evidência que se torna valioso vira alvo. Quanto mais o SILD funcionar como moeda de confiança — capaz de influenciar prêmio de seguro, regresso, faturamento e disputa — maior o incentivo para corrompê-lo. Esta seção trata o SILD como algo a ser atacado, não apenas usado.

Ignorar isso seria repetir o erro que o próprio SILD critica em outros sistemas: presumir que a evidência é confiável porque veio de uma fonte autorizada. A Confiança Zero deve se aplicar também ao próprio protocolo.

### Vetores de ataque previsíveis

**Falsificação de objeto físico.** Clonagem de lacre N1, reimpressão de QR, reuso de serial, etiqueta PIP duplicada. Mitigação progressiva: controle de reutilização e lote desde o N1; QR assinado, NFC e padrão físico não trivial nos níveis superiores; detecção de serial repetido no Evidence Register.

**Reaproveitamento de mídia.** Foto antiga de lacre íntegro reapresentada para uma operação nova. Esta é a brecha central do C0, e é por isso que a seção 22 estrutura o vínculo serial-documento-operador-horário no ponto físico de fechamento — com leitura automática preferencial e fallback manual com ressalva — e por isso o PACC Lite (sessão viva, nonce, frames congelados) existe na arquitetura-alvo. Mídia sem sessão atestada deve sempre carregar teto probatório menor.

**Conluio de operador autenticado.** Operador próprio do pátio que captura evidência forjada de propósito. Mitigação: o operador aciona evidência, não autentica verdade sozinho (princípio da seção 6); recorrência restrita por operador (seção 41); revisão humana e exigência probatória progressiva quando há padrão anômalo. Nunca blacklist automática.

**Adulteração de dossiê.** Alteração de mídia, hash, reason code ou status depois do registro. Mitigação: Evidence Register com trilha de criação/alteração/exportação no MVP-0; Custody Ledger append-only na arquitetura-alvo, onde correções são novos eventos, nunca sobrescrita; hash manifest no dossiê exportado.

**Ataque ao tempo.** Manipulação de relógio local, reboot para resetar tempo monotônico, sincronização tardia forjada. Já tratado na seção 20; o tempo local nunca é fonte absoluta, e reboot é evento técnico a reconciliar.

**Falsificação de certificação.** Componente, lacre, doca ou transportadora que se diz "SILD Certified" sem ser. Mitigação: registro público verificável de certificados, com validade e revogação; o selo só vale se for checável contra a fonte de governança (seção 77).

**Captura ou manipulação da governança.** Ator que influencia o padrão para favorecer o próprio produto, ou que usa a certificação como arma comercial. Tratado na seção 77 (separação institucional, transparência de financiamento, certificação contestável).

**Envenenamento da inteligência de rede.** Injeção deliberada de eventos para distorcer sinais agregados, prejudicar concorrente ou esconder padrão real. Mitigação na seção 92 (federação, agregação, revisão humana, ausência de efeito automático condenatório).

### Princípio de segurança do protocolo

A regra é:

> **A Confiança Zero do SILD se aplica ao próprio SILD. Nenhum lacre, dossiê, certificado, operador ou sinal de rede deve ser tratado como verdade absoluta só porque carrega a marca SILD. O protocolo classifica a força da própria evidência — inclusive contra tentativas de falsificá-la.**

Uma consequência de produto: cada nível de conformidade (L0–L5) deve declarar não apenas o que ele prova, mas **contra qual classe de ataque ele resiste**. Um L0 resiste a desorganização e perda de evidência, mas não a falsificação determinada. Um L2 atestado resiste a reaproveitamento de mídia. Um L5 certificado resiste a conluio isolado e adulteração de dossiê. Vender resistência que o nível não oferece é tão perigoso quanto a falsificação em si.

## 91-A. Saturação Probatória Adversarial e Proteção de Fluxo · [BASE/PADRÃO]

A seção 91 trata ataques contra a evidência. Esta seção trata uma ameaça de segunda ordem: ataques contra a **reação à evidência**. O alvo não é uma carga, é a legitimidade operacional do próprio SILD.

### 91-A.1 Definição

A **Saturação Probatória Adversarial** ocorre quando agentes hostis produzem ou induzem múltiplas anomalias logísticas deliberadas — lacres rompidos, cargas violadas, mídia cega, divergências físicas — em volume suficiente para sobrecarregar inspeções, atrasar cadeias lícitas, degradar a percepção pública do protocolo e induzir reação regulatória, comercial ou institucional contra o próprio sistema de evidência.

É um ataque reflexivo: o adversário tenta usar a reação defensiva do sistema como arma contra ele. A tática não busca capturar valor econômico direto numa carga específica; busca produzir a conclusão de que "o SILD atrapalha a logística", para que mercado, imprensa ou Estado pressionem contra o protocolo.

Isso é diferente de roubo, desvio ou fraude documental. Aqui o objeto atacado é a confiança no SILD, não a carga.

### 91-A.2 Risco de falso positivo: o ataque espelhado

Há uma falha lógica que precisa ser endereçada de frente, porque o próprio mecanismo de defesa pode virar vetor de ataque. Se o SILD reage a "aumento anômalo de anomalias", o adversário inteligente não precisa sabotar carga alguma: basta **induzir o SILD a declarar saturação onde não há ataque**, para então alegar que "o SILD acusa ataques fantasmas e paralisa o fluxo". Um falso alerta de saturação é tão danoso à legitimidade quanto a saturação real.

Por isso:

> **O SILD deve ser resistente tanto à saturação real quanto à falsa alegação de saturação.**

E a trava central da seção:

> **A classificação de Saturação Probatória Adversarial nunca é automática. Ela exige múltiplos sinais independentes, revisão humana, registro da decisão, justificativa técnica, possibilidade de reversão e separação entre anomalia operacional, degradação sistêmica e hipótese adversarial.**

Declarar saturação adversarial é, por si só, um ato sensível, auditável e reversível.

### 91-A.3 Condições mínimas para suspeita

Nenhuma suspeita de saturação se sustenta sem o conjunto:

- aumento acima da linha de base estabelecida;
- múltiplos sinais independentes — não apenas volume, mas independência de origem;
- distribuição temporal ou material incomum;
- impacto mensurável em throughput;
- ausência de explicação operacional simples (sazonalidade, mudança de processo, fornecedor de lacre ruim, treinamento);
- revisão humana antes de qualquer classificação alta.

A ausência de explicação operacional simples é condição necessária: a maioria dos picos de anomalia tem causa banal, e o SILD deve esgotar a hipótese banal antes de cogitar a hipótese adversarial.

### 91-A.4 Escala de resposta proporcional

A resposta é escalonada, nunca binária entre "liberar" e "parar":

- **Nível 0 — Ruído normal:** fluxo normal, sem ação.
- **Nível 1 — Anomalia local:** aumentar captura e auditoria amostral no ponto afetado.
- **Nível 2 — Recorrência restrita:** exigir evidência adicional apenas para a combinação afetada (rota, doca, transportadora), conforme a lógica de recorrência restrita já existente no protocolo.
- **Nível 3 — Risco de saturação operacional provável:** ativar o Modo de Proteção de Fluxo e triagem seletiva, sempre com revisão humana.
- **Nível 4 — Risco institucional ou regulatório:** gerar dossiê institucional de saturação. O SILD **não aciona autoridade automaticamente**; o dossiê fica disponível mediante base legal, solicitação formal, governança interna ou decisão do cliente, seguradora ou jurídico.

Mesmo no Nível 4, o SILD não vira polícia, não determina bloqueio geral e não atribui autoria. A regra do protocolo permanece: risco aumenta exigência probatória; não substitui prova.

### 91-A.5 Modo de Proteção de Fluxo

A reação errada à saturação seria parar tudo. A reação correta:

> **Quando a anomalia cresce, o SILD não paralisa a cadeia; ele separa fluxo, prioriza risco e aumenta evidência por camada.**

No Modo de Proteção de Fluxo:

- cargas com evidência forte continuam fluindo;
- cargas com anomalia leve recebem observação, não bloqueio;
- cargas com anomalia material entram em triagem;
- inspeção profunda é reservada para casos com múltiplos sinais independentes;
- o sistema evita recomendar inspeção massiva de todos os veículos;
- o protocolo mede o impacto de qualquer ação sobre a cadência logística;
- nenhuma rota inteira é bloqueada e nenhuma blacklist é criada.

A regra é:

> **O SILD não pode ser usado para transformar anomalia estatística em congestionamento sistêmico.**

### 91-A.6 Dossiê de Saturação Probatória

Quando o padrão excede o caso individual, o SILD gera um relatório distinto do dossiê de regresso. Ele é factual, sem autoria e sem acusação, e mostra: janela temporal, rotas e nós afetados, tipos de anomalia, volume comparado à linha de base, impacto em tempo de inspeção e em throughput, proporção de cargas legais atrasadas, evidências físicas preservadas, reason codes agregados, limites da inferência e recomendação de resposta proporcional.

Redação-padrão:

> **O SILD registra aumento anômalo de eventos de comprometimento físico e/ou baixa qualidade probatória em múltiplas operações, com potencial de saturação operacional. Este dossiê não atribui autoria nem confirma ilícito; organiza sinais para auditoria, gestão de risco, seguradora, governança do protocolo e autoridade competente quando aplicável.**

Esse dossiê protege o SILD inclusive politicamente: ele demonstra que o sistema não está "travando a logística", e sim identificando um padrão anômalo e recomendando resposta proporcional.

### 91-A.7 Limite por fase

A detecção de saturação adversarial **não pertence ao MVP-0** e depende da camada federada, pelas mesmas razões das seções 81 e 92 — volume, governança e base legal.

- **MVP-0:** apenas preserva sinais e reason codes. Não detecta saturação, não classifica nível, não ativa Modo de Proteção de Fluxo. Um cliente único enxerga só a fração de eventos que passa por ele, e fração não é padrão coordenado.
- **MVP-3:** recorrência interna por cliente, restrita ao próprio ambiente.
- **MVP-5:** inteligência federada que torna a detecção multiorigem possível, dentro da base legal e da governança da seção 92.
- **MVP-6:** resiliência institucional do padrão.

Qualquer linguagem de "detecção de saturação" antes da camada federada é incorreta. No ciclo zero, a única entrega é preservar o sinal para que a detecção seja possível depois.

Reason codes de preservação de sinal (registráveis desde cedo, sem efeito automático): `adversarial_saturation_suspected`, `inspection_load_risk_detected`, `coordinated_anomaly_pattern`, `throughput_degradation_risk`, `institutional_pressure_risk`. No MVP-0 eles, se existirem, são apenas marcações analíticas, nunca gatilhos de ação.

### 91-A.8 Comunicação pública

Coerente com a seção 93, a gramática externa é de triagem e proteção de fluxo, nunca de combate ao crime.

O SILD nunca comunica:

> "O SILD descobriu uma rede criminosa."

O SILD comunica:

> **Foi identificado aumento anômalo de inconsistências logísticas. O protocolo recomenda triagem proporcional para preservar o fluxo de cargas regulares e concentrar inspeção apenas onde há múltiplos sinais independentes.**

A mensagem externa tem três objetivos: mostrar que o SILD não causa o congestionamento, que ele reduz inspeção cega e que ele protege o fluxo lícito.

### 91-A.9 Regras de ouro

> **O adversário quer que o SILD responda com paralisia. O SILD deve responder com triagem, preservação de fluxo lícito e aumento seletivo de evidência.**

> **O falso alerta de saturação é também um ataque possível; por isso, nenhum modo avançado de saturação deve ser declarado sem revisão humana, múltiplos sinais independentes e registro auditável da decisão.**

## 92. Inteligência de rede federada e base legal · [ALVO/PADRÃO]

A inteligência de rede do SILD (seções 35, 81) só é legítima se nascer dentro de uma base legal explícita e de um desenho que separe dado operacional identificável de sinal estatístico agregado. Esta seção amarra essa exigência ao quadro regulatório brasileiro atual, porque "inteligência federada e privacidade-preservada" não é trivial — é um problema jurídico e técnico sério, e tratá-lo como detalhe convida a passivo.

### A pergunta dura que o mercado fará

Para virar padrão, o SILD terá que responder, de forma convincente: **"meus dados logísticos vão alimentar uma inteligência que pode ser usada contra mim, meus clientes ou meus trabalhadores?"** Uma resposta vaga inviabiliza adoção institucional.

### Base legal no Brasil

O tratamento de dados para prevenção a fraude e segurança tem amparo na LGPD, mas condicionado. No âmbito da LGPD, o tratamento de dados com finalidade de prevenção a fraudes encontra respaldo principalmente no legítimo interesse do controlador, previsto no art. 7º, IX, e na garantia de prevenção à fraude e segurança do titular. Esse amparo não é incondicional: previamente ao tratamento com base no legítimo interesse, a ANPD determina que seja realizada uma avaliação de proporcionalidade — o teste de balanceamento — aplicado para cada finalidade específica, ponderando legitimidade do interesse, necessidade do tratamento, impactos sobre os direitos dos titulares e suas legítimas expectativas.

Há ainda o cuidado com dados sensíveis e com a possibilidade de exigência regulatória de relatório de impacto. A ANPD pode solicitar ao controlador a elaboração de Relatório de Impacto à Proteção de Dados Pessoais (RIPD), observados os segredos comercial e industrial.

### O que isso impõe ao desenho da inteligência SILD

Da base legal decorrem requisitos de arquitetura, não apenas de política:

- **Finalidade específica e declarada.** A inteligência de rede deve ter finalidade explícita — aumentar exigência probatória em padrões recorrentes de baixa confiabilidade — e não pode ser usada para finalidade incompatível depois (princípio da não-reutilização).
- **Teste de balanceamento documentado por finalidade.** Antes de operar qualquer sinal agregado que toque dado pessoal incidental (operador, motorista), o SILD deve ter teste de balanceamento registrado, como a ANPD exige para legítimo interesse.
- **Minimização e agregação na origem.** A inteligência deve operar preferencialmente sobre sinais estatísticos agregados (aumento de mídia cega por rota, reincidência de lacre ilegível por tipo de operação, concentração de claims após certo evento), não sobre dado individual identificável exportado entre clientes.
- **Federação em vez de centralização.** Quando envolver múltiplos clientes, o desenho preferencial é federado: o sinal é computado localmente e só o agregado, sem identificação, compõe a visão de rede. Isso protege segredo comercial de rota e cliente, e reduz o risco de re-identificação por cruzamento.
- **Segregação por cliente.** Dados operacionais identificáveis de um cliente não devem ser visíveis a outro. A rede vê padrões, não prontuários.
- **Registro de operações e RIPD quando aplicável.** Manter o registro das operações de tratamento e estar preparado para produzir RIPD se a ANPD solicitar, preservando segredo comercial.

### Honestidade sobre a dificuldade

Separar "dado operacional identificável" de "sinal estatístico agregado" parece simples e não é. Re-identificação por cruzamento de rota, horário e volume é um risco real; agregados pequenos podem expor um único cliente; e a base legal para uso secundário precisa ser revista a cada nova finalidade. Por isso a inteligência de rede pertence a fases tardias (MVP-5), depende de volume, governança e maturidade jurídica, e nunca deve produzir efeito automático condenatório.

A regra é:

> **A inteligência de rede aumenta exigência probatória; não substitui prova, não acusa e não condena automaticamente. Ela só é legítima dentro de finalidade declarada, teste de balanceamento documentado, minimização, federação, segregação por cliente e direito de contestação.**

## 93. Comunicação estratégica: visão interna versus mensagem de mercado · [BASE]

O SILD tem uma camada de ambição — impacto sobre mercados ilícitos, negação logística ilícita (seções 82, 83) — que é legítima como visão de longo prazo, mas arriscada como mensagem pública de mercado. Esta seção separa as duas coisas, porque confundi-las prejudica a adoção.

### O risco de comunicar o SILD como ferramenta anticrime

Posicionar publicamente o SILD como instrumento de combate ao crime, mesmo que indireto, produz três efeitos adversos:

- **Escrutínio regulatório e jurídico precoce.** Um sistema que se anuncia como anticrime atrai questionamento sobre vigilância, devido processo, presunção de inocência e papel de fiscalização privada — exatamente os terrenos que o SILD diz não ocupar.
- **Resistência dos atores observados.** Transportadoras, operadores e motoristas que se sentem alvos de um "sistema de vigilância" resistem à adoção, ainda que o SILD observe ativos e não pessoas.
- **Expectativa que o produto não cumpre.** "Combate ao crime" cria expectativa de detecção e punição que o SILD, por princípio, não entrega. Isso prepara frustração e desconfiança.

### A separação

> **A camada de impacto sobre mercados ilícitos é visão interna e tese de longo prazo. Ela orienta o porquê profundo do projeto. Ela não deve ser a mensagem de venda, nem no MVP-0 nem nos ciclos seguintes.**

A mensagem de mercado deve permanecer ancorada em valor econômico verificável: defesa de receita, regresso, sinistro, redução de disputa, qualificação de evidência. O impacto sobre o ilícito aparece, quando aparece, como **consequência** descrita em linguagem sóbria, nunca como promessa.

A formulação filosófica da seção 83 — tornar a logística lícita mais difícil de ser parasitada por narrativas falsas — é excelente como princípio orientador e perigosa como pitch comercial. Ela deve viver no documento e na visão, não no material de vendas.

A regra é:

> **Internamente, o SILD pode sonhar com impacto sobre mercados ilícitos. Externamente, o SILD vende prova, defesa e redução de disputa. A filosofia orienta; ela não anuncia.**

## 94. Segmentação ampliada por valor da prova · [MVP-0]

Esta seção amplia a seção 87. O critério de entrada do SILD não é o tamanho do setor, mas a combinação de três fatores que tornam a prova economicamente desejável: **valor por unidade, risco de desvio e custo de disputa.** Onde os três coincidem, a evidência melhor gera ganho imediato e o SILD vira referência rápido.

Setores prioritários, ordenados por aderência ao MVP-0 e aos ciclos seguintes:

- **Farmacêuticos e distribuição hospitalar** — alto valor por unidade, regulação de rastreabilidade, cadeia fria, baixa tolerância a desvio.
- **Eletrônicos** — alvo clássico de roubo e desvio, alto chargeback em marketplace, alto valor por volume.
- **Químicos sensíveis e defensivos agrícolas** — risco regulatório e de segurança, valor alto, exigência documental.
- **Autopeças** — desvio recorrente, glosa frequente, alto custo de disputa.
- **Cadeia fria e alimentos de alto valor** — avaria e perda por quebra de custódia, prova de condição essencial.
- **Bebidas e cigarros legais** — alvo de furto e desvio, valor concentrado.
- **Cosméticos e perfumaria** — alto valor por volume, furto recorrente.
- **Peças aeronáuticas** — valor extremo por unidade, exigência probatória e de conformidade alta.
- **Cargas seguradas em geral** — onde a seguradora já exige prova, o SILD encaixa via âncora de adoção (seção 90).
- **Embarcadores com alto volume de chargeback de marketplace** — entram por Claim Intake e defesa documental, com a ressalva honesta de que o MVP-0 não vence a glosa do marketplace, mas organiza regresso e sinistro.
- **Operadores com histórico de roubo ou desvio recorrente** — onde o custo de disputa e sinistro já é dor explícita.

Por outro lado, o SILD **não** deve começar por logística genérica de baixa margem nem por last-mile capilar não cooperativo, onde a prova vale pouco e a topologia não sustenta evidência forte (seções 57, 70).

A regra de segmentação é:

> **Comece onde valor por unidade, risco de desvio e custo de disputa coincidem. Nesses setores, uma evidência melhor vira dinheiro rápido — e é assim que o SILD acumula a massa de casos que, repetida, vira padrão.**

## 95. Síntese final · [BASE]

O SILD não controla toda a estrada.

O SILD não controla todo o armazém.

O SILD não prova pureza interna da carga.

O SILD não elimina crime estruturado.

O SILD não força alta garantia onde a operação não permite alta garantia.

O SILD não presume que WMS, EDI, cliente, motorista, pátio ou smartphone são fontes absolutas de verdade.

A arquitetura-alvo do SILD faz algo específico e operacionalmente defensável:

> **mede a confiabilidade da narrativa logística.**

Sua força está em transformar eventos dispersos em uma cadeia probatória organizada. Quando a história da carga é consistente, o SILD mostra por quê. Quando a história é fraca, incompleta ou contraditória, o SILD mostra onde a confiança se perdeu.

O MVP-0 é deliberadamente menor:

> **captura evidência simples de saída, importa glosa em template SILD e gera dossiê de defesa/regresso.**

Ele não tenta julgar redes logísticas, certificar destino ou provar ausência de fraude. Ele prova a primeira hipótese comercial: uma evidência de saída vinculada a uma glosa posterior reduz a investigação improvisada e melhora a capacidade de defesa do embarcador.

Depois, o SILD pode evoluir para captura atestada, simetria, granularidade G2, RPI completa, reconciliação avançada, certificação, interoperabilidade e inteligência de rede.

Em escala institucional, o SILD pretende transformar evidência de custódia em linguagem comum entre embarcadores, transportadores, destinatários, seguradoras, auditores, sistemas legados, operadores logísticos e, quando aplicável, autoridades competentes.

A ambição global não muda a disciplina do MVP-0. O primeiro degrau continua sendo pequeno. O padrão nasce quando esse degrau pequeno já fala a gramática correta de evidência, objeto, evento, ator, contexto, limite probatório e dossiê.

As frases finais do sistema são:

> **O SILD não torna a fraude impossível; torna a mentira logística mensurável, contestável e cara de sustentar.**

> **O SILD não combate crime como polícia. Ele torna a logística lícita mais difícil de ser parasitada por narrativas falsas.**

---

# APÊNDICES — RECORTES INTERNOS DO DOCUMENTO-MÃE

> Os apêndices a seguir são recortes do mesmo documento único, não arquivos separados. Cada um filtra o conteúdo para um leitor específico. Em caso de divergência, o corpo do documento (seções 1–95) prevalece; os apêndices são vistas, não fontes paralelas.

---

## Apêndice A — SILD MVP-0 Field Spec

Recorte técnico-operacional para engenharia e piloto. Sem Confiança Zero, sem padrão global, sem Negação Logística Ilícita, sem MVP-5/MVP-6. Só o que se constrói no ciclo zero.

### A.1 Entidades

- **Operação** — criada por NF, pedido ou manifesto; chave de vínculo de tudo.
- **Documento** — NF/chave de acesso, pedido ou manifesto, com valor bruto e normalizado preservados.
- **Lacre** — serial, método de vínculo, estágio de vínculo, mídia associada.
- **Mídia** — foto aproximada do lacre, foto de contexto traseiro, hashes.
- **Ator** — operador autenticado do pátio.
- **Dispositivo** — identificador do aparelho de captura.
- **Glosa (claim)** — registro comercial importado em template SILD.
- **Dossiê** — PDF de defesa/regresso com teto probatório explícito.
- **RPI Lite** — flag documental aberta por claim match; sem ciclo de vida.

### A.2 Eventos do backend (MVP-0)

```text
operation_created
manifest_or_nf_linked
closure_point_reached
seal_bound                 (só no ponto físico de fechamento)
seal_read_failed
invalid_pre_scan_blocked
origin_media_captured
origin_capture_confirmed
claim_file_imported
commercial_claim_received
claim_line_rejected
claim_linked_to_origin_evidence
claim_line_pending_exported
defense_dossier_generated
rpi_lite_opened_by_claim_match   (derivado opcional)
```

### A.3 Campos de backend do lacre e da captura

- `seal_bind_method` — `qr_read`, `barcode_read`, `nfc_read`, `manual_entry`, `not_verified`;
- `seal_bind_stage` — `post_lock_installed`, `at_closure_point`, `invalid_pre_scan`;
- `seal_read_attempts` — inteiro;
- `seal_fallback_reason` — enum;
- `manual_entry_visual_support` — `not_yet_audited`, `serial_visible_in_photo`, `serial_partially_visible`, `serial_not_visible`, `not_applicable`;
- `manual_visual_audited_at` — timestamp opcional;
- `manual_visual_audited_by` — usuário opcional;
- `probative_ceiling` — `origin_evidence_registered`, `origin_evidence_registered_with_observation`, `origin_evidence_incomplete`;
- `reason_code` — enum (ver A.5);
- `seal_photo_hash` — hash;
- `context_photo_hash` — hash;
- `operator_id` — ID;
- `server_timestamp` — timestamp;
- `capture_instruction_acknowledged` — boolean opcional.

### A.4 Estados de lacre

| Cenário | `seal_bind_method` | `seal_bind_stage` | `manual_entry_visual_support` | `probative_ceiling` | Ação |
| --- | --- | --- | --- | --- | --- |
| Leitura no ponto de fechamento | `qr_read`/`barcode_read`/`nfc_read` | `post_lock_installed` | `not_applicable` | `origin_evidence_registered` | Dossiê automático |
| Falha de leitura, serial digitado, foto não auditada | `manual_entry` | `post_lock_installed` | `not_yet_audited` | `origin_evidence_registered_with_observation` | Dossiê com ressalva |
| Serial digitado, auditoria confirma foto nítida | `manual_entry` | `post_lock_installed` | `serial_visible_in_photo` | `origin_evidence_registered_with_observation` | Dossiê mantém ressalva |
| Serial digitado, auditoria acha foto parcial | `manual_entry` | `post_lock_installed` | `serial_partially_visible` | `..._with_observation` ou `..._incomplete` | Decisão humana pós-glosa |
| Serial digitado, foto cega | `manual_entry` | `post_lock_installed` | `serial_not_visible` | `origin_evidence_incomplete` | Dossiê fraco |
| Pré-escaneamento | bloqueado | `invalid_pre_scan` | `not_applicable` | nenhum | Não gera `seal_bound` |
| Sem leitura, sem serial, sem foto útil | `not_verified` | `post_lock_installed` | `serial_not_visible` | `origin_evidence_incomplete` | Evidência incompleta |

### A.5 Reason codes (taxonomia única do MVP-0)

Lacre e captura: `origin_evidence_registered`, `seal_photo_captured`, `context_photo_captured`, `seal_read_success`, `seal_read_failed`, `manual_seal_entry`, `seal_not_verified`, `invalid_pre_scan_blocked`, `manual_entry_pending_visual_audit`, `manual_entry_visual_confirmed`, `manual_entry_visual_blind`, `origin_evidence_registered_with_observation`, `origin_evidence_incomplete`.

Glosa e dossiê: `claim_template_imported`, `claim_line_rejected`, `claim_linked_to_origin_evidence`, `claim_line_pending_exported`, `rpi_lite_opened_by_claim_match`, `defense_dossier_generated`, `claim_without_matching_origin_evidence`.

### A.6 Fluxo do app de pátio

Abrir operação → ir ao ponto de fechamento → leitura do lacre instalado (câmera abre só aqui) → leitura OK salva método/serial/mídia; falha libera contingência manual com foto aproximada obrigatória → foto de contexto obrigatória → confirmar saída (salva hash, operador, horário, reason code, teto). Sem leitura em lote. Pré-scan bloqueado.

### A.7 Telas (UX mínima)

- Leitura: "Leia o lacre já instalado no ponto de fechamento." Sem modo lote.
- Falha: botão único "Digitar código manual — lacre instalado". Não perguntar se está travado.
- Foto: "Se o metal refletir, desligue o flash e fotografe a cerca de 20 cm." Foto aproximada obrigatória antes de confirmar contingência.
- Final: status simples — "Evidência registrada", "Registrada com observação" ou "Incompleta".

### A.8 Claim Intake

Um template oficial SILD. A plataforma não limpa planilha bruta; a conversão é do cliente, assistida por planilha-matriz de implantação (fora do software). Normalização de chaves (NF, pedido, CNPJ, datas, valor) e cascata determinística de matching (NF → NF+série+CNPJ → pedido+CNPJ → referência). Linha não conciliada vira CSV de pendência para correção e novo upload — sem tela de investigação no P0.

### A.9 Dossiê PDF

Capa mostra teto probatório. Seção de lacre mostra método de vínculo e reason code; se manual, declara que o serial foi informado pelo operador e depende de suporte visual. Seção de mídia exibe foto aproximada e de contexto. Seção de limites: "Origem registrada; destino não provado; conteúdo interno não certificado." Marca "suporte visual pendente de auditoria" quando `not_yet_audited` e "falha visual de contingência" quando foto cega após auditoria. Linguagem factual: "documenta evidência disponível", nunca "prova responsabilidade".

### A.10 Auditoria visual

A foto de serial manual não é auditada em tempo real. `manual_entry_visual_support` nasce `not_yet_audited`. A auditoria ocorre sob demanda, só quando houver glosa, sinistro, regresso ou revisão amostral. Sem Mesa Humana formal no MVP-0.

### A.11 Métricas

Tempo em duas medidas: `human_claim_preparation_time` (processo do cliente) e `sild_template_upload_to_pdf_time` (core do software). Mais: `origin_capture_completion_rate`, `manual_seal_entry_rate`, `seal_not_verified_rate`, `qr_read_success_rate`, `claim_template_rejection_rate`, `claim_auto_match_rate`, `claim_pending_export_rate`, taxa de novo upload após correção, taxa de dossiês com ressalva, distribuição do método de vínculo do lacre.

---

## Apêndice B — SILD Commercial Brief MVP-0

Recorte comercial curto. Foco em glosa, regresso, sinistro, transportadora, tempo de dossiê, limite probatório e piloto. Sem linguagem de protocolo.

**A dor.** Toda entrega contestada vira uma investigação improvisada: canhoto, foto de WhatsApp, e-mail, ligação para a transportadora. Demora, custa e muitas vezes a empresa começa a defesa sem prova organizada.

**A promessa.**

> **Da glosa recebida ao dossiê de regresso e sinistro em minutos.**

**Como funciona.** Na saída, o pátio registra a operação por NF, vincula o lacre no ponto de fechamento, tira foto do lacre e foto de contexto. Quando a glosa chega ao financeiro, ela é importada no template SILD, cruzada com a operação e vira um dossiê estruturado.

**Onde o dossiê ajuda primeiro.** Apoio ao pleito de regresso contra a transportadora e à instrução de sinistro junto à seguradora — terrenos onde prova organizada tem peso. Secundariamente, defesa comercial interna e contestação.

**O que o MVP-0 não promete.** Não vence automaticamente glosa de marketplace dominante. Não prova chegada. Não prova conteúdo interno. Não detecta fraude. E — importante — **não promete resultado jurídico, desconto de prêmio, aceite automático de seguradora nem aceleração garantida de sinistro.** Ele organiza a prova; a consequência depende de contrato e análise jurídica.

**Limite probatório explícito.** Todo dossiê declara o que a evidência permite afirmar e o que não permite. Origem registrada; destino não provado; conteúdo interno não certificado.

**O piloto.** 30 dias, uma rota/cliente/CD. Semana 1 mede a linha de base (qualidade dos lacres atuais, tempo de preparação de glosa do financeiro). Semanas 2–4 rodam o MVP-0. O sucesso separa falha de software, falha de lacre e falha de processo financeiro.

**A frase de fechamento.** O SILD não obriga ninguém a aceitar sua versão; ele impede que sua equipe comece a defesa sem prova organizada e apoia o pleito de regresso e a instrução de sinistro com evidência estruturada.

*(Nota interna, não usar como slogan: a descrição técnica do MVP-0 é "estruturador de prova de origem para defesa e regresso".)*

---

## Apêndice C — SILD Protocol Thesis

Recorte institucional. Aqui ficam Confiança Zero, padrão global, certificação, governança, interoperabilidade, rede federada e impacto sobre mercados ilícitos. Este apêndice **não** contamina a venda do MVP-0.

**Tese.** O SILD é um padrão progressivo de evidência de custódia para cadeias de entrega. Ele mede a confiabilidade da narrativa logística e define como eventos de custódia devem ser registrados, classificados, reconciliados, certificados e preservados.

**Confiança Zero.** Princípio do protocolo-alvo: não confiar isoladamente em operador, smartphone, lacre, WMS, TMS, cliente ou sistema legado. Combina sessão viva, objeto verificável, ambiente ancorado, dispositivo conhecido, ator identificado, evidência física e reconciliação auditável. Aplica-se inclusive ao próprio SILD (ver seção 91).

**Três camadas.** Protocol (vocabulário, eventos, reason codes, estados, dossiê), Platform (implementação SaaS) e Certification (conformidade de componentes e organizações).

**Níveis de conformidade.** L0 Registered → L1 Controlled → L2 Attested → L3 Symmetric → L4 Granular → L5 Certified Network. Cada nível declara o que prova e contra qual classe de ataque resiste.

**Interoperabilidade.** Contratos de evidência antes de conectores: Operation API, Evidence Event API, Claim Intake API, RPI API, Dossier Export API, Conformance API, webhooks. Modelo internacional desde o schema (shipment document, party identifier, custody unit), com NF/DANFE/CNPJ como mapeamento local.

**Governança.** Em fases: custódia única do mantenedor → comitê técnico com participação externa → governança separada da operação comercial. Conflito Platform-vende/Protocol-governa nomeado e mitigado por separação de papéis, especificação aberta, certificação contestável e transparência de financiamento.

**Inteligência federada.** Tardia (MVP-5), ancorada na base legal da LGPD (legítimo interesse, teste de balanceamento da ANPD, possível RIPD), com minimização, agregação na origem, federação, segregação por cliente e direito de contestação. Aumenta exigência probatória; não acusa nem condena.

**Adoção.** Valor unilateral antes da rede; seguradora como possível âncora de adoção (sem prometer consequência jurídica); segmentação por valor da prova.

**Impacto sobre mercados ilícitos.** Visão de longo prazo, **interna**: reduzir a zona cega onde narrativas falsas se escondem. Não é mensagem de mercado (ver seção 93). O SILD não combate crime como polícia; torna a logística lícita mais difícil de parasitar.

---

## Apêndice D — Matriz de Escopo Congelado do MVP-0

Checklist final do ciclo zero. O MVP-0 está congelado nesta frase:

> **Receber dado normalizado, registrar prova de origem, vincular lacre no ponto físico de fechamento, preservar mídia, cruzar chaves em cascata e gerar dossiê de defesa/regresso com teto probatório explícito.**

### D.1 Entra no MVP-0

- Console Web: criar operação por NF, pedido ou manifesto;
- Captura C0: foto do lacre + foto de contexto, vínculo à operação;
- vínculo de lacre no ponto físico de fechamento (leitura preferencial; fallback manual com foto);
- Evidence Register simples com trilha de criação/alteração/exportação;
- Claim Intake por template único, com normalização e cascata de matching;
- CSV de rejeições/pendências para correção externa e novo upload;
- Dossiê PDF com teto probatório explícito;
- RPI Lite como flag documental por claim match.

### D.2 Fica fora do MVP-0

Confiança Zero como linguagem comercial; mapper visual de planilhas; parser nativo de marketplace; UI de associação manual de glosas; leitura prévia de lacre como vínculo probatório; troca obrigatória de lacre metálico já travado; homologação obrigatória de novo lacre para piloto; IA de legibilidade de foto; auditoria visual em tempo real; Mesa Humana formal; PACC Lite; SILD Hub; Symmetry; G2 Lite; PIP físico; Fast Track; cold storage; API/EDI/SFTP; inteligência visual; inteligência federada; bloqueio financeiro automático.

### D.3 Reason codes congelados

Ver Apêndice A.5 — taxonomia única, sem duplicação (`seal_read_failed` substitui `seal_unreadable`).

### D.4 Campos de backend congelados

Ver Apêndice A.3.

### D.5 Matriz de lacre congelada

Ver Apêndice A.4.

### D.6 Métricas congeladas

Ver Apêndice A.11. Métrica principal: tempo core do software (upload do template ao PDF). Métrica de saúde: taxa de match automático. Tempo total da glosa bruta ao dossiê é diagnóstico de processo do cliente, nunca métrica comercial isolada.

### D.7 Critérios de piloto

30 dias, uma rota/cliente/CD. Linha de base na semana 1 (incluindo qualidade dos lacres existentes e tempo de preparação de glosa). MVP-0 nas semanas 2–4. Resultado separa falha de software, falha de lacre e falha de processo financeiro. Não medir sucesso por Symmetry, Fast Track, G2 Lite, PACC ou cold storage.
