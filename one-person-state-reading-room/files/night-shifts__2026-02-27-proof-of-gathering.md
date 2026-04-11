# Proof of Gathering: Почему физическое со-присутствие — главный незанятый примитив Network State

*Night research — 27 февраля 2026*

---

## Тезис

В спорах о Network State все говорят о территории, токенах и законах. Но самый мощный и недооценённый строительный блок — **верифицируемое физическое со-присутствие** (Proof of Gathering). Это не просто POAP на стероидах. Это фундамент гражданства, который решает обе проблемы Виталика — governance и membership — одновременно.

---

## 1. Проблема: два нерешённых вопроса Виталика

На Network State Conference 2024 в Сингапуре Виталик Бутерин признал, что после Zuzalu остаются два нерешённых вопроса:

1. **Governance** — как принимать решения без центральной власти?
2. **Membership** — кто вообще "гражданин" и как это определять?

Балажи Сринивасан предложил формулу: Network State = онлайн-сообщество + общие ценности + коллективное действие + физический meetup. Но последний элемент остался наименее проработанным. Все думают, что meetup — это результат. На самом деле meetup — это **инфраструктура**.

---

## 2. Что такое Proof of Gathering (PoG)

Proof of Gathering — это верифицируемое криптографическое доказательство того, что конкретный человек физически присутствовал на конкретном событии вместе с другими участниками.

**Это НЕ просто POAP.** POAP — это «я был на ивенте» (и часто фармится ботами). PoG — это тройка:

- **Кто** (ZK-identity, без раскрытия конкретной личности, как в Zupass)
- **Где** (верифицированная геолокация + time-bounded attestation)
- **С кем** (граф со-присутствия — кто был в одной комнате)

Zupass от 0xPARC уже реализовал часть этого: ZK-proof что «я — участник Zuzalu» без раскрытия «кто именно я». Но Zupass работал только внутри Zuzalu. PoG — это обобщение на любое сообщество.

---

## 3. Почему со-присутствие — лучший примитив для citizenship

### 3.1 Каждое историческое государство начиналось с gathering

- Афинская демократия: право голоса = тот, кто может физически прийти на Pnyx
- Швейцарская Landsgemeinde: голосуют те, кто стоит на площади
- Исландский Althing (930 г.): закон принимается теми, кто доехал до Thingvellir

Физическое присутствие всегда было первым фильтром гражданства — задолго до паспортов, налогов и территорий.

### 3.2 Со-присутствие решает Sybil-resistance

Главная проблема DAO governance — Sybil-атаки (один человек = много аккаунтов). Токены не решают проблему (купил больше — голосуешь больше). Quadratic voting помогает, но требует proof of personhood.

Физическое присутствие — **самый дорогой для фейка сигнал**. Чтобы подделать участие в 7 ивентах в 4 городах за год, нужно буквально быть 7 раз в 4 городах. Тело не масштабируется.

### 3.3 Со-присутствие создаёт natural reputation

Не все gatherings равны. PoG создаёт многослойную репутацию:

| Тип gathering | Вес | Что доказывает |
|---|---|---|
| Meetup (2-3 часа) | 1x | Интерес |
| Weekend retreat | 3x | Commitment |
| Pop-up city (1-2 месяца) | 10x | Deep alignment |
| Co-living (6+ мес.) | 25x | Full citizenship |

Это не произвольные числа — это отражение реального skin in the game. Каждый уровень требует экспоненциально больше ресурсов (время, деньги, отказ от альтернатив).

---

## 4. Scaffolded Spontaneity: что говорит академия

В ноябре 2025 на arXiv вышла работа «Infrastructuring Pop-Up Cities with Social Layer» — первое серьёзное академическое исследование инфраструктуры pop-up городов.

Ключевой концепт — **scaffolded spontaneity**: баланс между структурой и открытостью. Исследование покрывает 5 реальных deployments: ShanHaiWoo (Китай), muChiangmai (Таиланд), Edge Esmeralda (Калифорния), Aleph (Буэнос-Айрес), Gathering of Tribe (Лиссабон!).

Находки, релевантные для PoG:

1. **Privacy-preserving credentials** — участники хотят доказать принадлежность без раскрытия личности
2. **Portable community memory** — опыт со-присутствия должен переноситься между gatherings
3. **Lightweight governance через participation visibility** — кто пришёл, кто организовал, кто вовлечён

Это буквально описание PoG-системы, только авторы ещё не дали ей имя.

---

## 5. Zuzalu → Archipelago → ? Эволюция модели

| Год | Модель | Что нового |
|---|---|---|
| 2023 | Zuzalu 1.0 (Черногория) | 200 человек, 2 месяца, один город |
| 2024 | Archipelago (Чиангмай) | Децентрализация: 5+ параллельных pop-up villages |
| 2024 | Edge Esmeralda | Путь от pop-up к permanent community |
| 2024 | Aleph (Буэнос-Айрес) | Crecimiento movement, латиноамериканский контекст |
| 2025 | Network State Conference | Виталик: «governance и membership не решены» |
| 2026? | **PoG-based citizenship** | Gatherings как строительные блоки гражданства |

Edge City (команда за Edge Esmeralda) уже движется к permanent community в Sonoma County. Но у них нет формализованного citizenship — только vibes. PoG может стать недостающим примитивом.

---

## 6. Belarus Case: идеальный тестовый полигон

### Почему именно беларуская диаспора?

**100,000+ беларусов** покинули страну после 2020 года. Они распределены по Вильнюсу, Варшаве, Берлину, Лиссабону, и десяткам других городов. У них уже есть:

- **Регулярные gatherings**: Конференция беларуской диаспоры (4-я прошла в Варшаве, май 2025, 100+ предложений от разных стран), New Belarus Conference 2025 (420+ участников, август 2025)
- **Культурные ивенты**: Купалле, Каляды, Дзяды — календарь уже существует
- **Политическая легитимность**: Офис Тихановской как координирующий центр
- **Техническая грамотность**: сильное IT-сообщество (Беларусь = «европейская Кремниевая долина»)

### Чего не хватает?

Верифицируемого графа со-присутствия. Сейчас «гражданство» в беларуском движении — это примерно «я подписался на канал» или «я пришёл на митинг». Но между «лайкнул пост в Telegram» и «приехал в Варшаву на 3 дня за свой счёт» — пропасть вовлечённости, которую никто не измеряет.

### Конкретное предложение: Belarus Gathering Graph

```
┌─────────────────────────────────────────┐
│          BELARUS NETWORK STATE          │
│          Citizenship Tiers              │
│                                         │
│  🌱 Observer      0 PoG    Read-only   │
│  🌿 Participant   3 PoG    Proposals   │
│  🌳 Citizen      10 PoG    Voting      │
│  🏛️ Elder        25 PoG    Governance  │
│                                         │
│  PoG = Proof of Gathering credits       │
│  1 meetup = 1 PoG                       │
│  1 conference = 3 PoG                   │
│  1 multi-day retreat = 5 PoG            │
│  Organizing event = 2x multiplier       │
│  Cross-city gathering = 1.5x multiplier │
└─────────────────────────────────────────┘
```

**Cross-city multiplier** — ключевая фишка. Если ты был на ивенте в Лиссабоне И в Варшаве — это доказывает, что ты часть сети, а не локальной тусовки. Для diaspora network state это критически важно.

---

## 7. Техническая реализация (эскиз)

### Слой 1: Identity (уже существует)
- Zupass / Semaphore для ZK identity
- Ethereum attestations (EAS) для on-chain записи

### Слой 2: Gathering Verification
- **NFC tap** при входе на ивент (как POAP, но с geolocation check)
- **Mutual attestation**: 3+ участника подтверждают присутствие друг друга (Byzantine fault tolerant: нужно 2/3 подтверждений)
- **Time-bounded**: attestation работает только в окне ±2 часа от события

### Слой 3: Reputation Graph
- Soulbound token (SBT) с accumulated PoG score
- Decay function: PoG теряет 20% веса в год (нужно продолжать участвовать)
- Cross-community portability: PoG из беларуского ивента имеет вес в более широком network state экосистеме

### Слой 4: Governance
- Voting weight = f(PoG score)
- Quadratic voting с PoG-based voice credits
- Proposals require minimum PoG threshold (нельзя предлагать, если не был ни на одном gathering)

---

## 8. Неочевидные следствия

### 8.1 Gathering as Mining
В Bitcoin proof-of-work майнит блоки. В PoG-системе «майнинг» — это организация gatherings. Тот, кто создаёт ивенты и приводит людей, получает 2x multiplier. Это инвертирует экономику: **вместо pay-to-play — show-up-to-earn-voice**.

### 8.2 DJ Set как Governance Event
Если Ray играет DJ-сет на беларуском ивенте — это не развлечение. Это governance infrastructure. Каждый пришедший получает PoG. Танцпол = voting booth. (Rave States из прошлого ресёрча получает конкретный механизм.)

### 8.3 The Anti-Remote Paradox
Network State — вроде бы цифровая концепция. Но PoG делает физическое присутствие самым ценным ресурсом. Это не баг — это фича. Цифровые инструменты делают координацию дешёвой, но **легитимность** остаётся дорогой. PoG — это proof-of-stake, где stake = твоё тело и время.

### 8.4 Эстонский урок наоборот
E-Residency Эстонии = цифровое гражданство без физического присутствия. 110,000+ e-residents, но сообщества нет. Это бизнес-инструмент, не nation-building. PoG — инверсия: физическое присутствие как основа, цифровые инструменты как надстройка.

---

## 9. Risks & Limitations

- **Exclusion bias**: люди с ограниченной мобильностью получают меньше PoG. Нужны accessibility mechanisms (remote attestation от trusted nodes, но с пониженным весом)
- **Geographic privilege**: живущие в hub-городах (Варшава, Вильнюс) имеют преимущество. Cross-city multiplier частично компенсирует
- **Gaming**: друзья attestируют друг друга без реального участия. Mutual attestation с рандомизированными парами и minimum crowd size снижает риск
- **Privacy concerns**: ZK proofs решают «кто я», но сам факт участия в беларуском оппозиционном ивенте может быть опасен для тех, чьи семьи в Беларуси. Нужен полный ZK: «я — участник сообщества с 10+ PoG» без раскрытия конкретных ивентов

---

## 10. Actionable Next Steps для Belarus Network State 2030

1. **Пилот на Купалле 2026**: NFC-тапы + mutual attestation на ближайшем крупном беларуском ивенте. Минимальный MVP на Zupass
2. **Gathering Calendar as Citizenship Pipeline**: формализовать существующий календарь диаспорных ивентов как citizenship acquisition path
3. **Partnership с Edge City / Social Layer**: их инфраструктура (Social Layer) уже deployed в Лиссабоне (Gathering of Tribe 2024). Беларуское сообщество в Лиссабоне — perfect bridge
4. **PoG Standard Proposal**: написать EIP/ERC-подобный стандарт для Proof of Gathering, чтобы другие network states могли использовать
5. **f27.club как первый PoG node**: каждый ивент f27 генерирует PoG credentials для участников

---

## Заключение

Proof of Gathering — это не просто технология. Это переосмысление того, что значит быть гражданином. Государства XX века строились на территории и документах. Network States XXI века могут строиться на верифицируемом со-присутствии.

Для беларуской диаспоры это особенно мощно: **у нас отняли территорию, но не могут отнять способность собираться вместе**. Каждое Купалле, каждая конференция, каждый DJ-сет — это не просто культурное событие. Это акт state-building.

Тело не масштабируется. В этом его сила.

---

## Источники

1. Vitalik Buterin — Network State Conference 2024, Singapore (Sept 22, 2024) — [Cointelegraph](https://cointelegraph.com/news/vitalik-shares-vision-zuzalu-implications-network-states)
2. «Infrastructuring Pop-Up Cities with Social Layer» — arXiv:2511.15680 (Nov 2025) — [arXiv](https://arxiv.org/html/2511.15680)
3. Zupass / Proof-Carrying Data — [GitHub](https://github.com/proofcarryingdata/zupass)
4. New Belarus Conference 2025 — 420+ participants, Warsaw, Aug 9-10, 2025 — [Tsikhanouskaya.org](https://tsikhanouskaya.org/en/news/new-belarus-conference-2025-outcomes-resolutions-and-common-course.html)
5. 4th Conference of the Belarusian Diaspora — Warsaw, May 23-25, 2025 — [Tsikhanouskaya.org](https://tsikhanouskaya.org/en/event/iv-conference-of-belarusians-of-the-world)
6. Belarusian Diaspora 2025: 100,000+ relocated — [Belarus Partisan](https://belaruspartisan.org/en/politics/belarusian-diaspora-2025/)
7. Edge City / Edge Esmeralda — [edgecity.live](https://www.edgecity.live)
8. Soulbound Tokens & DAO Governance — [Outlook India, Jan 2026](https://www.outlookindia.com/xhub/blockchain-insights/how-soulbound-tokens-are-transforming-dao-membership-participation)
9. Estonian e-Residency — [e-Estonia](https://e-estonia.com/solutions/estonian-e-identity/e-residency/)
10. Granovetter, M. (1973) — «The Strength of Weak Ties» — American Journal of Sociology
