# SILD — Sistema de Integridade Logística Dinâmica

## Protocolo Progressivo de Evidência Logística baseado em Confiança Zero

## 1. Definição geral

O **SILD — Sistema de Integridade Logística Dinâmica** é um protocolo progressivo de evidência logística. Sua função é medir, registrar e classificar a confiabilidade da narrativa operacional de uma carga, começando pelo estado inicial da custódia e evoluindo para simetria origem-destino, certificação probatória e inteligência de rede apenas quando a operação demonstrar maturidade suficiente.

O SILD não promete provar que uma carga é lícita, não certifica pureza material do conteúdo e não substitui inspeções físicas, perícia, fiscalização pública, gerenciamento de risco, seguradora ou autoridade competente. Sua função central é mais específica: **calcular quão confiável é a evidência que sustenta a história logística de uma carga**.

A lógica central do SILD é:

> **A fraude logística raramente depende de um único evento falso. Ela depende da manutenção artificial de uma história coerente entre carga, lacre, veículo, rota, manifesto, operador, destino e evidência.**

O SILD torna essa história mensurável.

Em vez de perguntar apenas “há algo ilegal dentro da carga?”, o sistema pergunta:

> **A carga, o veículo, o lacre, o manifesto, a rota, os eventos de custódia e as evidências capturadas continuam formando uma narrativa logisticamente coerente e tecnicamente confiável?**

O SILD não torna a fraude impossível. Ele torna a mentira logística **mais cara, mais complexa, mais auditável e mais difícil de sustentar sem contradições**.

O SILD nasce pequeno. No primeiro estágio, ele registra manifesto, lacre, veículo e saída. Quando há destino próprio ou cooperativo, adiciona confirmação de chegada. Quando há maturidade operacional, evolui para certificação probatória. Só depois, com volume de dados, governança jurídica e base contratual suficiente, passa a operar inteligência de rede.


## 2. Problema enfrentado

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


## 3. Princípios fundamentais

O SILD opera sob o princípio de **Confiança Zero aplicada à logística**.

Isso significa que o sistema não presume automaticamente que uma evidência é confiável porque veio de um operador autorizado, de um aplicativo, de um manifesto, de um smartphone, de um lacre, de uma transportadora, de uma gerenciadora de risco ou de um sistema corporativo.

Cada dado é avaliado conforme sua qualidade probatória, origem, contexto, independência e coerência com os demais eventos.

As três regras centrais do SILD são:

> **Imagem valida objeto. Contexto valida evento. Ator valida independência.**

> **Offline mantém a operação; online fortalece a prova.**

> **Reconciliação explica a perda probatória; não purifica o passado.**

A primeira regra separa o que uma imagem mostra do que ela consegue provar. Uma foto pode mostrar um lacre correto, mas não comprova sozinha que a foto foi feita no destino, no horário correto ou por ator independente.

A segunda regra impede que falhas de conectividade travem a logística, mas também impede que capturas offline recebam a mesma força probatória de eventos online com validação de servidor.

A terceira regra impede a criação retroativa de uma história perfeita. Evidência posterior pode explicar, reconciliar e encerrar uma disputa operacional, mas não apaga a lacuna original.


## 4. O que o SILD não é

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


## 5. Protocolo progressivo de evidência

O SILD deve ser implantado em camadas. A força probatória aumenta apenas quando a operação real suporta a camada seguinte.

### 5.1 SILD Origin Snap

Registra o estado inicial da custódia no momento da saída: manifesto, veículo, lacre, fechamento físico e captura pelo pátio controlado.

É o estágio inicial do produto.

### 5.2 SILD Symmetry

Adiciona observação de destino, formando simetria origem-destino. Quando o destino é próprio, a confirmação deve ser feita por aplicativo autenticado. Quando o destino é terceiro cooperativo, pode haver WebSnap com controles. Quando o destino não coopera, o SILD reduz o escopo.

### 5.3 SILD Proof

Gera certificado probatório de custódia para operações logisticamente elegíveis, com origem e destino suficientemente controlados, atores identificados, lacres vinculados, eventos coerentes e evidência independente.

### 5.4 SILD Reconciliation

Gerencia exceções, falhas técnicas, ausência de geolocalização, divergências, evidências compensatórias e reconciliação assíncrona sem apagar a falha original.

### 5.5 SILD Intelligence

Camada futura, aplicada apenas após volume, governança e base jurídica. Mede padrões recorrentes de baixa qualidade probatória em rotas, nós logísticos, transportadoras, operadores e destinos.

A ordem correta de construção é:

> **gesto operacional mínimo → evidência confiável → relatório útil → simetria origem-destino → certificado → inteligência de rede.**


## 6. Função central

A função central do SILD é criar uma trilha auditável de custódia logística e classificar a qualidade dessa trilha.

O sistema busca responder:

- se a operação possui estrutura mínima para produzir evidência;
- qual manifesto ou documento foi associado à saída;
- qual veículo ou unidade logística assumiu a operação;
- qual lacre foi vinculado ao evento;
- se a carga saiu com fechamento físico registrado;
- quem capturou a evidência;
- qual dispositivo produziu a evidência;
- onde e quando a evidência foi registrada;
- se a chegada foi confirmada por ator independente;
- se houve divergência de lacre, placa, manifesto ou destino;
- se a prova é forte, limitada, incompleta ou contraditória;
- se a operação precisou de reconciliação;
- quais evidências compensatórias foram usadas;
- quais limites probatórios permanecem.

O produto inicial não é uma acusação e não é uma liberação automática. É um **dossiê mínimo de custódia**.


## 7. SILD Origin Snap

O **SILD Origin Snap** é o modo inicial do SILD. Ele registra o estado físico e documental da custódia no momento de saída da carga.

Sua finalidade é provar, com baixo atrito, que determinada carga saiu de uma origem controlada associada a um manifesto, veículo e lacre.

O Origin Snap não prova entrega.

O Origin Snap não prova conteúdo interno.

O Origin Snap não depende de app no celular do motorista.

O Origin Snap não fotografa o rosto do motorista no MVP.

O Origin Snap não exige integração com TMS, ERP ou GR para rodar o piloto.

O Origin Snap deve ser executado por operador do pátio, conferente, lacrador, portaria ou agente autorizado do embarcador.

A regra é:

> **Motorista terceirizado não é usuário do SILD. Ele é parte observada da operação por meio dos ativos físicos que conduz.**


## 8. Objeto do Origin Snap

O Origin Snap registra:

- operação;
- manifesto, DANFE ou documento equivalente;
- placa traseira da carreta ou unidade de carga;
- lacre instalado;
- porta ou baú fechado;
- origem;
- destino esperado;
- transportadora;
- operador do pátio;
- dispositivo de captura;
- horário de servidor;
- local de origem;
- hash da mídia;
- status da saída.

A presença do motorista é consequência operacional do veículo liberado, não raiz de confiança do sistema.

O SILD observa ativos logísticos, não rostos de terceiros.


## 9. Entrada de dados sem gargalo de TI

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

O lacre deve ser preferencialmente vinculado no pátio, no momento físico da lacração, por leitura direta do lacre instalado.


## 10. Captura traseira única

A captura de origem deve ocorrer em uma única posição física, preferencialmente na traseira da carreta, onde a carga está lacrada.

O operador não deve caminhar até a frente do caminhão para produzir prova.

Fluxo mínimo:

1. Operador abre a viagem no app pelo manifesto, placa ou lista de operações pendentes.
2. Captura a placa traseira da carreta ou unidade logística.
3. Captura o lacre instalado de perto.
4. Captura a porta fechada em plano de contexto, incluindo lacre e, quando possível, placa traseira.
5. Confirma saída.

A captura deve ser desenhada para pátios reais: sol, chuva, ruído, EPI, pressa, empilhadeiras, baixa conectividade e operadores sob carga operacional.

Metas de desempenho:

- p50 abaixo de 25 segundos;
- p95 abaixo de 60 segundos no início do piloto;
- p95 abaixo de 45 segundos após ajuste de processo.

O SILD não sobrevive se virar ritual burocrático.


## 11. SILD Snap App

O **SILD Snap App** é o aplicativo de captura controlado pelo SILD.

No MVP, ele deve rodar preferencialmente em aparelho corporativo do pátio ou do CD, não no celular pessoal do motorista.

Características mínimas:

- login do operador ou turno;
- seleção de viagem pendente;
- câmera direta pelo app;
- bloqueio de upload de galeria;
- leitura de QR ou OCR quando possível;
- confirmação visual assistida;
- fila local para falhas de conexão;
- sincronização posterior;
- assinatura local do pacote quando disponível;
- registro de dispositivo;
- hash de mídia;
- timestamp de servidor quando online.

O app deve guiar o operador, não transformá-lo em perito.


## 12. Smartphone como coletor oportunístico

O smartphone é tratado como coletor oportunístico, não como raiz absoluta de confiança.

No MVP, a força da captura aumenta quando o dispositivo é corporativo, autenticado, online e associado a um ponto controlado. A força diminui quando o evento é offline, quando há falha de leitura, quando a mídia é ruim, quando há divergência ou quando o ator não é independente.

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


## 13. Modo offline

O modo offline existe para preservar o fluxo operacional, não para preservar força probatória máxima.

A falta de conexão não deve travar automaticamente a logística. Também não deve permitir que um evento offline receba a mesma força de um evento online validado em tempo real.

Classificação operacional:

### Captura online

O app recebe validação do servidor, registra o evento, captura a mídia, associa manifesto e lacre, e sincroniza imediatamente.

Pode receber status máximo no MVP.

### Captura offline reconciliada

O app captura localmente e sincroniza depois. O servidor valida coerência temporal, sequência local, dispositivo, operação, mídia e delta de sincronização.

Pode receber status com observação.

### Captura offline suspeita

Há reboot, delta temporal incompatível, sequência anormal, sincronização tardia sem justificativa, inconsistência de dispositivo ou metadados frágeis.

Recebe status pendente de reconciliação.

### Captura offline contraditória

Há lacre divergente, operação incompatível, mídia duplicada, tentativa de galeria, evento impossível ou contradição objetiva.

Recebe status divergente.

A regra é:

> **Offline mantém a operação; online fortalece a prova.**


## 14. Tempo local, reboot e reconciliação técnica

O SILD não deve confiar cegamente no relógio local do smartphone.

O app deve registrar sinais técnicos auxiliares:

- horário local declarado;
- último horário de servidor conhecido;
- delta entre relógio local e servidor na última sincronização;
- índice incremental local de eventos;
- identificador do dispositivo;
- ocorrência de reboot quando detectável;
- sequência de capturas;
- horário real de recebimento no servidor;
- hash de mídia;
- operação vinculada.

O tempo monotônico do sistema pode resetar após reinicialização do aparelho. Por isso, o app deve manter um estado local persistente e um indexador próprio de eventos. Se houver reboot, o servidor deve tratar como evento técnico a reconciliar, não como fraude automática.

O desafio pré-gerado offline não deve ser vendido como anti-replay forte sem ambiente confiável de tempo e atestação.


## 15. Lacre verificável

O lacre é componente de continuidade, não prova de pureza da carga.

Sua função é vincular o evento de origem ao fechamento físico do veículo, pallet, contêiner, caixa ou unidade logística.

O lacre pode incluir:

- número único;
- QR code;
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

A categoria correta para muitos eventos será:

> **origem logisticamente coerente, cadeia externa preservada, conteúdo interno não certificado.**


## 16. Níveis de lacre

O SILD deve operar com níveis de lacre proporcionais ao risco e ao valor protegido.

### Nível 1 — Lacre operacional serializado

Número único e QR. Serve para vínculo operacional, controle de reutilização e registro básico.

### Nível 2 — Lacre destrutível com evidência visual

Inclui material que demonstra rompimento, foto do lacre instalado, comparação origem-destino e controle de lote.

### Nível 3 — Lacre antifraude reforçado

Pode incluir NFC, padrão físico não trivial, microelemento visual, embalagem controlada e auditoria amostral.

### Nível 4 — Lacre ou dispositivo testemunha premium

Pode incluir sensor de abertura, luz, movimento, choque, permanência ou ruptura. É aplicável apenas a cargas críticas.

O MVP deve usar Nível 1 ou 2, sem prometer inviolabilidade sofisticada.


## 17. SILD Symmetry

O **SILD Symmetry** é a fase que adiciona observação de destino ao Origin Snap, formando simetria origem-destino.

A simetria aumenta a força probatória porque compara o estado da carga na saída com o estado observado na chegada.

A regra é:

> **Sem observação independente no destino, não há simetria probatória forte.**

O SILD Symmetry deve ser aplicado quando houver destino próprio ou destino terceiro cooperativo.


## 18. Destino próprio

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


## 19. Destino terceiro cooperativo

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


## 20. Destino não cooperativo

Destino não cooperativo não destrói o SILD. Ele apenas reduz o escopo.

Quando o destinatário não aceita app, WebSnap, confirmação oficial, leitura de lacre ou qualquer colaboração mínima, o sistema pode emitir relatório de evidência parcial.

Esse relatório pode comprovar bem a saída, mas não deve afirmar simetria forte de chegada.

A regra é:

> **Destino não cooperativo impede prova forte de chegada; não invalida a evidência de origem.**


## 21. QR do lacre e QR de recebimento

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


## 22. WebSnap

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


## 23. Objeto, evento e ator

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


## 24. Estados externos do MVP

O MVP deve usar linguagem operacional simples.

### Saída Validada

Manifesto, veículo, lacre e fechamento foram registrados corretamente na origem.

### Saída Validada com Observação

A saída foi registrada, mas houve detalhe operacional: OCR falhou, lacre foi digitado manualmente, conexão oscilou ou houve pequena limitação técnica.

### Saída Pendente de Reconciliação

Faltou elemento relevante, mas a operação ainda pode ser reconciliada por evidência adicional.

### Saída Divergente

Há incompatibilidade objetiva: lacre reutilizado, lacre cancelado, placa divergente contra fonte confiável, manifesto incompatível ou tentativa inválida de mídia.

### Custódia Concluída

Origem e destino foram registrados com contexto e ator válidos.

### Custódia Concluída e Reconciliada

A operação foi encerrada com evidência compensatória independente, preservando registro de que o evento original teve limitação técnica.

### Custódia Pendente

A cadeia ainda depende de evidência complementar ou análise.

### Custódia Divergente

Há contradição relevante entre origem, destino, lacre, veículo, localização, ator ou tempo.


## 25. Critérios de Custódia Concluída

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


## 26. Matriz de uso interno, operacional e externo

O SILD deve separar linguagem técnica, linguagem operacional e linguagem externa.

| Evento interno | Status operacional | Status externo | Uso permitido |
| --- | --- | --- | --- |
| `origin_snap_validated` | Saída Validada | Evidência de origem registrada | Encerrar evento de saída |
| `seal_manual_entry` | Saída Validada com Observação | Saída registrada com confirmação manual | Monitorar qualidade de leitura |
| `offline_reconciled` | Saída Validada com Observação | Evidência sincronizada posteriormente | Aceitar com ressalva operacional |
| `arrival_context_missing` | Custódia Pendente | Fechamento de destino pendente de evidência | Acionar reconciliação |
| `auto_reconciled_via_wms` | Custódia Concluída e Reconciliada | Fechamento confirmado por evidência independente | Encerrar disputa operacional |
| `legacy_only_insufficient` | Custódia Pendente | Evidência externa insuficiente | Exigir fonte independente |
| `websnap_geolocation_missing` | Custódia Pendente | Confirmação de destino sem contexto suficiente | Reconciliar ou manter pendência |
| `websnap_outside_geofence` | Custódia Divergente | Evento de destino incompatível | Escalar exceção |
| `driver_controlled_evidence_rejected` | Custódia Pendente ou Divergente | Evidência não independente rejeitada | Impedir fechamento por ator interessado |
| `custody_divergent` | Custódia Divergente | Divergência objetiva de custódia | Acionar revisão, jurídico ou auditoria |

A linguagem externa deve ser factual e defensável. Ela não deve ocultar eventos relevantes, mas também não deve transformar limitação técnica em confissão comercial desnecessária.


## 27. Classes internas

As classes técnicas podem existir no motor do SILD, mas não devem dominar a interface do MVP.

### Classes de captura V0–V4

Medem a qualidade técnica da mídia, do dispositivo e da sessão.

### Classes de cadeia C0–C4

Medem a força total da custódia, considerando origem, destino, contexto, ator, lacre, rota, independência e reconciliação.

No MVP, essas classes devem ser usadas internamente para cálculo, auditoria e evolução de produto. O usuário operacional deve ver estados simples.


## 28. Pacote de evidência

Cada evento SILD gera um pacote de evidência.

O pacote pode conter:

- ID da operação;
- manifesto ou DANFE;
- hash do documento quando disponível;
- placa capturada;
- lacre capturado;
- fotos ou burst da captura;
- operador;
- dispositivo;
- origem ou destino;
- timestamp de servidor;
- timestamp local;
- status da captura;
- metadados técnicos;
- hash da mídia;
- resultado de OCR ou leitura;
- reason codes;
- vínculo com eventos anteriores;
- classificação externa;
- classificação interna.

O SILD não armazena apenas fotos. Ele armazena um transcrito probatório estruturado.


## 29. Custody Ledger

O SILD utiliza um livro de eventos de custódia append-only.

Eventos não são apagados. Correções são feitas por novos eventos.

O ledger deve registrar:

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

A confiança degrada conforme materialidade, atraso, recorrência e impacto da correção, não pela mera existência de erro humano.


## 30. Eventos mínimos do backend

O backend do SILD deve registrar eventos discretos, auditáveis e encadeados.

Eventos mínimos:

- `operation_created`;
- `manifest_scanned`;
- `manifest_uploaded`;
- `seal_bound`;
- `origin_snap_started`;
- `rear_plate_captured`;
- `seal_image_captured`;
- `origin_context_captured`;
- `origin_snap_confirmed`;
- `origin_exception_opened`;
- `arrival_snap_started`;
- `arrival_plate_captured`;
- `arrival_seal_captured`;
- `arrival_condition_recorded`;
- `arrival_snap_confirmed`;
- `custody_closed`;
- `reconciliation_opened`;
- `compensatory_evidence_received`;
- `reconciliation_auto_closed`;
- `reconciliation_manual_closed`;
- `custody_divergence_opened`.

Cada evento deve conter, quando aplicável:

- ID da operação;
- ator;
- dispositivo;
- canal;
- horário de servidor;
- horário local;
- origem ou destino;
- hash da mídia;
- vínculo com evento anterior;
- reason code;
- status interno;
- status externo.

A regra é:

> **O SILD não edita eventos. Ele acrescenta eventos que explicam, corrigem ou contradizem eventos anteriores.**


## 31. Reconciliação assíncrona

A reconciliação assíncrona permite tirar uma viagem do limbo operacional sem reescrever a história probatória.

Princípio:

> **Evidência posterior explica; não purifica.**

Quando um evento falha, por exemplo por ausência de geolocalização no destino, o SILD registra o evento original e abre uma pendência.

A evidência compensatória pode fechar a disputa operacional, mas não transforma retroativamente a captura falha em captura perfeita.

O teto após falha relevante deve ser:

> **Custódia Concluída e Reconciliada.**

Não se deve retornar para Custódia Concluída plena se a validação original perdeu contexto essencial.


## 32. Evidências compensatórias

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


## 33. Fast Track de reconciliação

Para evitar paralisia por compliance, o SILD deve possuir uma esteira automatizada de reconciliação.

O **Fast Track** pode fechar automaticamente uma pendência quando houver evidência forte, nativamente digital e independente, como:

- webhook do WMS do destino;
- evento de app autenticado no CD;
- portaria digital validada;
- canal oficial do destinatário;
- API corporativa;
- registro de balança integrado.

O sistema aplica o teto de reconciliação, registra o reason code e encerra a pendência sem análise humana.

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


## 34. Sistemas legados

TMS, GR, POD, ERP e WMS podem compor a narrativa logística, mas não possuem a mesma força probatória.

A regra é:

> **Sistema legado não eleva sozinho a força de evidência física SILD.**

Ele pode:

- corroborar;
- contradizer;
- explicar;
- acionar reconciliação;
- compor conjunto independente;
- ajudar a reconstruir cronologia.

Ele não pode lavar uma falha de contexto físico sozinho.

Se o WebSnap não possui geolocalização e apenas o TMS da transportadora diz “entregue”, o evento não deve ser elevado.

Se há WMS do comprador, portaria digital e app autenticado no destino, a cadeia pode ser reconciliada.


## 35. Contingência

Contingência é parte da logística real.

Pode haver falha de rede, chuva, baixa iluminação, QR ilegível, câmera danificada, pressa de doca, erro operacional, pátio metálico, queda de energia ou indisponibilidade temporária do aplicativo.

A contingência não deve bloquear automaticamente a operação.

A contingência também não deve virar caminho padrão para escapar do sistema.

Ela deve gerar:

- evento auditável;
- causa declarada;
- status proporcional;
- possível evidência compensatória;
- monitoramento de recorrência;
- melhoria de processo.

Contingência recorrente não prova fraude. Ela prova perda de qualidade operacional ou tentativa de evasão a investigar.

Não se deve usar teto rígido universal de contingência. A análise deve considerar contexto: rota, base, conectividade, turno, tipo de pátio, operador, carga e destino.


## 36. MEP — Motor de Elegibilidade Probatória

O **MEP — Motor de Elegibilidade Probatória** define qual produto SILD é aplicável à operação.

No produto maduro, o MEP avalia:

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
- histórico operacional.

No MVP, o MEP deve ser simplificado.

Perguntas mínimas:

- a origem é controlada?
- a carga sai lacrada?
- há manifesto ou documento associável?
- há placa ou unidade logística capturável?
- há operador do pátio disponível?
- o destino é próprio, cooperativo ou não cooperativo?
- o piloto precisa de Origin Snap, Symmetry ou apenas evidência parcial?

A regra é:

> **O SILD só promete a força probatória que a topologia permite.**


## 37. Topologias operacionais

O SILD classifica operações conforme capacidade de gerar evidência.

### T1 — Origem controlada e destino próprio

Cenário ideal para Origin Snap + Symmetry com app autenticado nas duas pontas.

### T2 — Origem controlada e destino cooperativo

Elegível para Origin Snap + WebSnap, app do destino, portal, WMS ou canal oficial.

### T3 — Multi-drop cooperativo

Elegível para Proof Segmentado por unidade logística, destino, pallet, gaiola ou volume crítico.

### T4 — LTL aberto e varejo fracionado

Não deve receber Proof Completo. Pode operar com evidência parcial, volumes críticos ou relatório documental.

### T5 — Last-mile capilar não cooperativo

Não deve receber certificado forte. Pode gerar rastreabilidade parcial e evidência documental.

A matriz impede que o sistema force alta confiança em operações estruturalmente incapazes de produzi-la.


## 38. Índice de Cooperação do Destino

O **ICD — Índice de Cooperação do Destino** mede se o destino pode funcionar como pilar probatório.

No MVP, o ICD deve ser operacional, não estatístico.

Categorias:

### Destino próprio

Usa app autenticado ou sistema controlado.

### Destino cooperativo

Aceita WebSnap, app, e-mail oficial, WMS, API, PIN ou confirmação estruturada.

### Destino parcialmente cooperativo

Aceita alguma evidência, mas sem autenticação forte.

### Destino não cooperativo

Não permite confirmação confiável.

A regra é:

> **Destino não cooperativo não destrói a prova de origem; apenas impede simetria forte.**


## 39. Índice de Granularidade da Custódia

O **IGC — Índice de Granularidade da Custódia** define o objeto certificado pelo SILD.

Possíveis níveis:

### G1 — Caminhão, carreta, baú ou contêiner inteiro

Adequado para FTL, hub-to-hub e cargas lacradas como unidade única.

### G2 — Pallet, gaiola ou unidade logística intermediária

Adequado para operações fracionadas controladas.

### G3 — Caixa, volume ou remessa individual

Adequado para cargas sensíveis em LTL, desde que haja identificação e lacre por unidade.

### G4 — Remessa documental

Adequado para varejo capilar sem controle físico granular.

A regra é:

> **Se a operação é multi-drop e não há lacre ou identificação por unidade logística, o SILD não deve emitir certificação forte por entrega individual.**


## 40. Disputas internas à unidade lacrada

O SILD deve distinguir disputa sobre a unidade lacrada de disputa dentro da unidade lacrada.

Se a operação opera em granularidade **G1** — carreta, baú ou contêiner inteiro — o sistema pode demonstrar que a unidade saiu lacrada e chegou com lacre compatível. Isso não resolve, sozinho, disputas sobre falta de caixa, avaria interna, pallet incompleto ou divergência de conteúdo dentro da unidade lacrada.

Quando a dor comercial recorrente envolve faltas internas, o piloto deve migrar para granularidade superior:

- **G2**, com pallet, gaiola ou unidade logística intermediária identificada;
- **G3**, com caixa, volume ou remessa individual identificada;
- ou inspeção/materialidade adicional fora do escopo do Origin Snap.

A regra é:

> **Lacre íntegro protege a narrativa da unidade lacrada. Não prova composição interna se a granularidade não foi capturada.**

Essa regra evita vender Origin Snap como solução para disputas que exigem granularidade de pallet, volume ou conteúdo.


## 41. Relação com Gerenciamento de Risco

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
- se há dossiê defensável para disputa.

A formulação comercial é:

> **Gerenciamento de risco controla o veículo. O SILD qualifica a confiança da história da carga.**

No piloto, o SILD deve rodar independente. Integrações com GR, TMS, ERP e WMS entram depois da prova de valor.


## 42. Relatório SILD

O relatório SILD deve ter linguagem adequada ao público.

### Camada operacional

Mostra status simples, pendências, divergências, tempo de captura, lacres e ações necessárias.

### Camada técnica

Mostra reason codes, classes internas, qualidade da mídia, sincronização, reconciliação e limitações.

### Camada comercial externa

Deve ser factual, defensável e não autoincriminatória.

Exemplos de status externos:

- Custódia Concluída;
- Custódia Concluída e Reconciliada;
- Custódia Pendente;
- Custódia Divergente.

A expressão “limitação probatória” pode existir na camada técnica interna, mas deve ser tratada com cuidado em relatórios externos. O relatório externo deve descrever fatos e evidências, sem linguagem que transforme uma limitação técnica em confissão de falha operacional.


## 43. Governança financeira e bloqueio de faturamento

O status SILD não deve ser usado como gatilho automático de bloqueio financeiro.

O SILD qualifica a evidência da entrega, organiza a defesa operacional e sinaliza pendências, reconciliações ou divergências. A decisão de faturamento, retenção, glosa, cobrança, aceite comercial ou contestação deve permanecer sujeita à política financeira, comercial e contratual da empresa.

A regra é:

> **O SILD informa a qualidade da evidência; ele não substitui a política de faturamento.**

Aplicações corretas:

- priorizar reconciliação antes de disputa;
- acelerar resposta ao cliente;
- anexar dossiê a cobrança contestada;
- separar pendência documental de divergência física;
- proteger receita com documentação estruturada.

Aplicações incorretas:

- bloquear automaticamente faturamento por qualquer observação técnica;
- tratar Custódia Concluída e Reconciliada como inadimplência operacional;
- transformar status técnico interno em punição financeira automática;
- permitir que exceção de conectividade vire glosa interna sem análise.

O SILD deve reduzir disputa cega, não criar uma nova fila burocrática de bloqueio financeiro.


## 44. Defesa de receita

O SILD deve ser posicionado comercialmente como defesa de receita operacional.

Toda entrega contestada vira uma investigação improvisada. O SILD transforma essa investigação em dossiê automático.

O problema comercial não é apenas fraude. É a incapacidade de defender rapidamente uma entrega quando o cliente, o financeiro, a auditoria, a seguradora ou o comercial questionam.

O SILD não promete que grandes varejistas, marketplaces ou clientes dominantes aceitarão automaticamente a entrega. Ele melhora a posição de negociação do embarcador.

A formulação comercial é:

> **O SILD não muda a personalidade do cliente difícil. Ele muda a sua posição na mesa de negociação.**

> **Do canhoto disperso ao dossiê de custódia em minutos.**

> **Quando o cliente contestar, sua equipe já entra com a história montada.**


## 45. Promessa comercial do primeiro ciclo

No primeiro ciclo de implantação, o SILD não deve prometer redução imediata de horas administrativas.

É possível que a carga administrativa aumente temporariamente, porque o sistema passa a revelar falhas de evidência que antes ficavam escondidas pelo canhoto, pelo WhatsApp ou pela baixa manual.

A promessa inicial é outra:

- reduzir tempo de resposta a contestações;
- organizar evidências antes da cobrança;
- transformar investigação improvisada em dossiê;
- separar disputa real de falha documental;
- criar linha de base objetiva para melhoria de processo.

A redução de retrabalho administrativo vem depois da estabilização do processo.

A regra comercial é:

> **No primeiro ciclo, o SILD reduz o tempo da disputa, não necessariamente o volume de trabalho administrativo.**


## 46. Playbook de reunião comercial

A primeira reunião deve começar pela dor operacional do Diretor de Logística, não por tecnologia, criptografia, score ou integração.

Abertura recomendada:

> **Toda entrega contestada vira uma investigação improvisada. O SILD transforma essa investigação em dossiê automático.**

Sequência de abordagem:

1. Perguntar qual rota, cliente ou CD mais exige reconstrução de entrega.
2. Explicar que o piloto não exige integração de TI no dia zero.
3. Explicar que o motorista terceirizado não usa app, não faz login e não produz prova.
4. Explicar que o pátio controlado captura a saída e o CD próprio captura a chegada.
5. Explicar que o SILD não garante aceite automático de grandes clientes, mas melhora a posição de negociação.
6. Propor piloto de 30 dias em uma rota lacrada, com linha de base na primeira semana.

Perguntas úteis:

- qual cliente mais contesta entrega;
- qual rota mais exige busca manual de comprovantes;
- onde o canhoto mais falha;
- onde o lacre mais gera discussão;
- qual CD ou portaria consegue capturar chegada com menor atrito.

Frases de apoio:

> **O SILD não muda a personalidade do cliente difícil. Ele muda sua posição na mesa de negociação.**

> **O SILD não cria divergência. Ele organiza sua defesa antes que a divergência vire cobrança.**

> **O motorista rotativo não é validador. O pátio e o CD são as testemunhas controladas da custódia.**


## 47. Valor contra canhoto tradicional

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
- quais evidências sustentam o fechamento.

O SILD não substitui necessariamente o canhoto. Ele mostra se o encerramento da entrega merece confiança.

A frase comercial é:

> **O canhoto encerra a entrega. O SILD qualifica a confiança do encerramento.**


## 48. Separação entre MVP técnico e piloto comercial

O SILD deve separar claramente produto mínimo de implantação comercial.

O **MVP técnico** é o conjunto mínimo de módulos, regras, estados e controles que permite ao sistema existir com integridade operacional.

O **piloto comercial** é o recorte controlado de aplicação desse MVP em uma rota, cliente, CD ou operação específica para provar valor.

A regra é:

> **MVP técnico valida capacidade do produto. Piloto comercial valida valor em uma operação real.**

Essa separação evita dois erros:

- tratar o piloto como se fosse o produto final;
- vender uma transformação sistêmica antes de provar o gesto operacional mínimo.

O MVP técnico deve ser estável, pequeno e repetível. O piloto comercial deve ser limitado, mensurável e reversível.


## 49. MVP técnico recomendado

O MVP recomendado é o **SILD Origin Snap com Symmetry em destino próprio**.

Cenário ideal:

- origem controlada;
- CD próprio ou destino cooperativo;
- carga lacrada;
- motoristas terceirizados e rotativos;
- captura feita por operador do pátio;
- captura de chegada feita por app autenticado no CD;
- sem app no celular do motorista;
- sem foto do motorista;
- sem API obrigatória;
- sem inteligência de rede;
- sem CTM completo;
- sem NRI ou ICE.

Hipótese crítica:

> **É possível registrar manifesto, lacre, veículo e saída sem aumentar materialmente o tempo de pátio?**

Hipótese secundária:

> **É possível comparar origem e destino em ambiente próprio sem depender do motorista?**

O MVP técnico deve existir sem depender de fila de TI do cliente.

A integração por API é evolução, não premissa do piloto. O produto deve provar valor com barcode, CSV, entrada mínima e aparelhos corporativos controlados pela operação.


## 50. Piloto comercial recomendado

O piloto deve durar 30 dias e operar em uma rota controlada.

### Semana 1 — Linha de base

A equipe observa o processo atual sem alterar a operação.

Mede:

- tempo de liberação;
- qualidade dos canhotos;
- frequência de lacres não fotografados;
- tempo para localizar evidência;
- tipos de divergência;
- retrabalho de reconstrução;
- fluxo real de pátio.

### Semanas 2 a 4 — SILD em operação

Na origem:

- manifesto bipado no Console Web;
- lacre vinculado no pátio;
- captura traseira única;
- saída validada.

No destino próprio:

- app autenticado;
- captura de placa traseira;
- captura do lacre;
- condição do fechamento;
- comparação com origem.

Resultado do piloto:

- tempo médio de captura;
- p95 de captura;
- taxa de Saída Validada;
- taxa de Saída com Observação;
- taxa de chegada validada;
- taxa de divergência;
- taxa de reconciliação;
- tempo para montar dossiê;
- redução da caça manual a comprovantes.

O piloto comercial deve comparar explicitamente o modelo tradicional com o modelo SILD.

A primeira semana cria linha de base. As semanas seguintes testam o SILD. O resultado não deve ser apenas taxa de captura, mas diferença prática entre reconstrução manual e dossiê automático.


## 51. Critérios de inviabilidade do piloto

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
- não há responsável interno para tratar reconciliações.

A regra é:

> **O SILD deve começar onde há chance real de produzir evidência útil.**

Se a dor principal está no destino, o piloto deve incluir Symmetry. Se a dor principal está dentro do pallet, o piloto deve elevar a granularidade. Se a dor principal é conteúdo interno, o SILD precisa de inspeção ou integração material adicional.


## 52. Métricas de sucesso

As métricas do SILD não devem começar por “contrabando detectado”.

No MVP, as métricas relevantes são:

- tempo p50 de captura;
- tempo p95 de captura;
- taxa de operações capturadas sem atrasar pátio;
- taxa de Saída Validada;
- taxa de Saída Validada com Observação;
- taxa de Saída Pendente;
- taxa de Saída Divergente;
- taxa de lacres reutilizados bloqueados;
- taxa de captura offline;
- taxa de reconciliação automática;
- taxa de reconciliação humana;
- taxa de chegada validada;
- tempo para montar dossiê de entrega contestada;
- tempo médio de resposta a contestação;
- número de casos em que o SILD substituiu busca manual por canhoto, print ou ligação;
- aceitação operacional pelo pátio;
- impacto no tempo de liberação.

A métrica principal é:

> **reduzir investigação improvisada de entrega sem degradar o fluxo logístico.**

No primeiro ciclo, não se deve medir sucesso pela redução imediata de horas administrativas totais. O indicador mais relevante é a redução do tempo de resposta e a melhora da qualidade da defesa quando a entrega é contestada.


## 53. Arquitetura mínima do MVP

Módulos iniciais:

### SILD Console Web

Criação simples de viagem por barcode, QR, CSV ou entrada mínima.

### SILD Snap App

Captura autenticada em aparelho corporativo na origem e no destino próprio.

### SILD Seal Registry

Controle de lacres, serialização, vínculo, reutilização, cancelamento e status.

### SILD Custody Ledger

Registro append-only de eventos, correções, reconciliações e divergências.

### SILD Evidence Report

Geração de relatório HTML/PDF/CSV com dossiê da operação.

### SILD Reconciliation Engine

Fast Track automático e mesa humana para exceções.

Módulos futuros:

- SILD Network Intelligence;
- NRI;
- ICE;
- desvio homólogo;
- CTM completo;
- multimodal;
- auditoria estatística;
- dossiês institucionais.


## 54. Reason codes internos

O SILD deve usar reason codes para padronizar decisões.

Lista inicial:

- `origin_snap_validated`;
- `rear_plate_captured`;
- `seal_captured`;
- `seal_unreadable`;
- `seal_manual_entry`;
- `seal_reused`;
- `seal_cancelled`;
- `manifest_barcode_scanned`;
- `manual_manifest_entry`;
- `gallery_upload_blocked`;
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
- `custody_divergent`.


## 55. Segurança, LGPD e direito de imagem

O MVP deve seguir minimização de dados.

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
- registrar acesso aos dossiês.

O motorista terceirizado pode ser identificado pelos meios contratuais e operacionais já existentes, quando necessários, mas o SILD não deve criar uma camada adicional de vigilância pessoal no MVP.

A regra é:

> **O SILD observa ativos de custódia, não rostos de terceiros.**


## 56. Política de retenção e acesso às evidências

A retenção das evidências deve ser proporcional à finalidade operacional, contratual e jurídica.

Diretrizes:

- evidências de operações comuns devem ter prazo de retenção definido em contrato;
- evidências de operações contestadas podem ter retenção ampliada enquanto durar a disputa;
- evidências vinculadas a sinistro, auditoria, seguradora ou litígio devem seguir prazo jurídico aplicável;
- mídias sem valor probatório residual devem ser descartadas ou anonimizadas ao final da finalidade;
- acesso aos dossiês deve ser registrado;
- exportações devem gerar trilha de auditoria;
- usuários devem ter perfis de acesso proporcionais;
- evidências com terceiros, quando inevitáveis, devem ter controle de compartilhamento;
- dados pessoais incidentais devem ser minimizados.

A regra é:

> **O SILD preserva evidência enquanto houver finalidade legítima; depois reduz, anonimiza ou descarta.**

A retenção não deve transformar o SILD em arquivo indefinido de vigilância operacional.


## 57. Limites técnicos

O SILD possui limites explícitos.

O Origin Snap não prova entrega.

O Arrival Snap não prova conteúdo interno.

O lacre comum não prova inviolabilidade sofisticada.

Captura offline não mantém força máxima.

Foto sem contexto não valida evento.

Sistema legado não cura falha sozinho.

Reconciliação não apaga lacuna original.

Motorista terceirizado não é raiz de confiança.

WebSnap anônimo não deve ser usado em destino próprio.

QR de recebimento não pode viajar com a carga.

O SILD não consegue provar ausência de ilícito dentro da carga sem inspeção de conteúdo.

O SILD não impede fraude perfeita em ambiente totalmente comprometido.

O SILD não transforma smartphone em equipamento forense absoluto.

O SILD certifica a qualidade da evidência logística disponível.


## 58. Decisões operacionais

O SILD deve operar com ações proporcionais.

A resposta a um evento anômalo pode incluir:

- registrar sem interromper;
- solicitar nova captura;
- exigir leitura no destino;
- emitir relatório com status correto;
- abrir pendência de reconciliação;
- aplicar Fast Track automático;
- acionar mesa humana;
- exigir evidência compensatória;
- reconciliar sem apagar evento original;
- recomendar ajuste de processo;
- escalar para auditoria, jurídico ou seguradora quando necessário.

A regra é:

> **primeiro aumentar evidência; depois aumentar controle; só por último impedir fluxo.**

Isso reduz impacto operacional e responsabilidade civil.


## 59. CTM e mutações topológicas como fase futura

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

No MVP Origin Snap, o CTM completo não deve ser implementado.

A lógica de mutação deve aparecer apenas como exceção simples quando houver divergência entre saída, chegada e reconciliação.


## 60. Inteligência de rede como fase futura

A inteligência de rede não deve fazer parte do MVP.

NRI, ICE, desvio homólogo, degradação de nós, deslocamento adversarial e dossiês institucionais dependem de:

- volume de dados suficiente;
- padronização;
- base contratual;
- governança jurídica;
- segregação de clientes;
- minimização de dados;
- revisão humana;
- direito de contestação;
- controle de uso externo.

Esses índices não devem gerar condenação automática, bloqueio automático ou blacklist opaca.

Quando implementados, devem aumentar exigência probatória, orientar auditoria e gerar dossiês apenas quando houver base adequada.

A regra é:

> **Risco de rede aumenta exigência probatória; não substitui prova.**


## 61. Núcleo de Negação Logística Ilícita como visão estratégica

A camada de Negação Logística Ilícita permanece como visão de longo prazo.

Sua função não é punir, fiscalizar ou investigar no lugar do Estado. Sua função é reduzir a previsibilidade logística que permite a mercados ilícitos operarem em escala.

Essa camada só deve surgir depois de o SILD provar sua base operacional:

1. captura de origem;
2. simetria destino;
3. relatórios confiáveis;
4. reconciliação madura;
5. volume de dados;
6. governança jurídica;
7. inteligência de rede.

A linguagem institucional deve permanecer:

> **Há recorrência logística anômala com base probatória documentada.**

E não:

> **Este nó é criminoso.**


## 62. Multimodal como fase futura

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

O MVP deve permanecer rodoviário, lacrado e controlado.


## 63. Modelo comercial

O SILD pode operar como SaaS de evidência logística e defesa de receita.

Modelos possíveis:

- cobrança por operação capturada;
- cobrança por dossiê gerado;
- assinatura mensal por pátio;
- assinatura por embarcador;
- pacote por rota crítica;
- licença por CD;
- cobrança premium para Symmetry;
- módulos adicionais para API, WMS, auditoria e relatórios jurídicos.

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


## 64. Segmentação de mercado

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
- operações hub-to-hub controladas.

O SILD não deve começar pela logística genérica de baixa margem nem pelo last-mile capilar não cooperativo.


## 65. Formulação institucional revisada

O SILD pode ser apresentado assim:

> **O SILD é um protocolo progressivo de evidência logística baseado em Confiança Zero. No primeiro estágio, ele documenta a saída da carga por meio de manifesto, lacre, veículo e captura feita pelo pátio controlado. Quando há destino próprio ou cooperativo, adiciona simetria de chegada. Quando há maturidade operacional, evolui para certificação probatória. Só depois, com volume, governança e base jurídica, passa a operar inteligência de rede. O sistema não promete detectar todo ilícito; ele mede a força da evidência que sustenta a história logística, reduz disputas cegas, organiza a defesa da entrega e torna a mentira logística mais difícil de sustentar sem contradições.**


## 66. Síntese final

O SILD não controla toda a estrada.

O SILD não controla todo o armazém.

O SILD não prova pureza interna da carga.

O SILD não elimina crime estruturado.

O SILD não força alta garantia onde a operação não permite alta garantia.

O SILD faz algo mais específico e operacionalmente viável:

> **mede a confiabilidade da narrativa logística.**

Sua força está em transformar eventos dispersos em uma cadeia probatória organizada. Quando a história da carga é consistente, o SILD mostra por quê. Quando a história é fraca, incompleta ou contraditória, o SILD mostra onde a confiança se perdeu.

No estágio inicial, o SILD não tenta julgar redes logísticas. Ele captura o estado inicial da custódia com baixo atrito. Quando há destino próprio, compara saída e chegada. Quando há divergência, preserva a verdade técnica. Quando há reconciliação, fecha a disputa sem reescrever o passado.

O objetivo estratégico é reduzir reconstruções improvisadas, fortalecer defesa operacional, qualificar a confiança da entrega e tornar fraudes logísticas mais caras de sustentar.

A frase final do sistema é:

> **O SILD não torna a fraude impossível; torna a mentira logística mensurável, contestável e cara de sustentar.**
