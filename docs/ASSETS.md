# Auditoria de Assets — Ecos de Valdoria

> Varredura feita em 27/10/2026 no repositório `rpg-sidescroller` e em **todo** o Google Drive de contato.alanrezende@gmail.com (≈2.800 imagens, áudios e pacotes .zip, não só a pasta `RPG / TCG`). As imagens candidatas foram baixadas e inspecionadas visualmente.

## 1. Resultado em uma linha

**Nenhum personagem, inimigo, cenário ou interface de fantasia medieval existe hoje.** O repositório estava vazio e o conteúdo 2D do Drive pertence a outros projetos (jogo de zumbis, Sokoban da Kenney, jogos js13k, card game de faroeste). Dá para reaproveitar **4 efeitos visuais** (fogo no chão, arcos de corte, projétil ácido, névoa/poeira/vento), **explosões** e **~18 SFX CC0**. Todo o resto precisa ser produzido ou obtido.

---

## 2. O que foi verificado

### 2.1 Repositório `rpg-sidescroller`
| Item | Situação |
|---|---|
| Arquivos | Nenhum (repositório recém-criado, sem commits) |

### 2.2 Google Drive — pastas com conteúdo 2D

| Pasta (caminho) | Conteúdo | Serve para este jogo? |
|---|---|---|
| `RPG / TCG` → `Jogos RPG` | PDFs de livros de RPG de mesa (Ordem Paranormal, Rune, Fortuito, Hora da Seis, Blanc & Noir, Casos Não Resolvidos) | ❌ Só referência de regras/lore |
| `RPG / TCG` → `Jogos RPG` → `Cardgame` | Card game "Sessão Maldita": 35 cartas 63×88 (faroeste/ratos/queijo), 12 desenhos para colorir, cenário em PDF | ❌ Ilustração de carta, não sprite; tema incompatível |
| `Último Dia de Aula` → `Spritesheet` (**106 PNGs**, 0,5–3,5 MB) | Atlas gerados por IA para o jogo de zumbis "Último Dia de Aula". Inspecionados um a um: zumbis (operário, chef, enfermeira, guarda, treinador com corda, Boss Diretor), professor/sobrevivente com taco, NPCs 1–4 (andar/interagir/morrer), armas modernas, itens de sobrevivência (água, enlatados, kit médico), tiles de escola, padaria, rua e bairro, carros destruídos | ⚠️ Personagens, tiles e itens incompatíveis (cenário moderno). **VFX reaproveitáveis** — ver seção 3 |
| `HTML5 Apps e Jogos` → `Aventura de Luis` → `images` | Pack **Kenney Sokoban** (CC0): `Crates` (51), `Ground/Explosion/Keys` (35, inclui `explosion_0…8` e bombas), `Player` (30, visão de cima), `Environment` (26), `Blocks` (8) | ⚠️ Jogo top-down. Só as explosões e bombas servem (estilo cartoon, diferente do pixel art) |
| `HTML5 Apps e Jogos` → `Aventura de Luis` → `sounds` | Subset do pack *512 Retro SFX* de Juhani Junkala (**CC0**), 52 arquivos (≈18 sons em .wav/.mp3) + 1 MIDI | ✅ Reaproveitável |
| `HTML5 Apps e Jogos` → `Planta vs Cubinhos` → `build/images` | `planty1-3.gif` + `plantyShoot.gif` (37×59, planta que atira) | ⚠️ Estilo minimalista; serve só como placeholder de inimigo-planta |
| `HTML5 Apps e Jogos` → `Oh Não!`, `Blackout`, `Missão Espacial`, `Donzela de Valhalla`, `Gelecas contra Elementais`, `Monstria` etc. | Jogos js13k/minimalistas: `tileset.png` 96×16 (6 tiles), `sprites.png` 128×128, nave espacial, ícones/capas dos jogos | ❌ Resolução e estilo incompatíveis (só capas/ícones) |
| `CodePen` → `Soltos` | 11 .zip de projetos CodePen: `pixel-platformer-engine`, `microvania`, `game-the-dungeon`, `top-down-2d-game-camera`, `canvas-fireworks`… | ⚠️ Referência de código (física de plataforma, câmera, partículas). Sem arte utilizável |
| `HTML5 Apps e Jogos` → `Fonética Game` / `Alfabetização em Jogo` | Áudios de vogais (a/e/i/o/u.wav) | ❌ Educativo |
| `assets_glb` | Modelos 3D (.glb/.blend) de vila, pets, props | ❌ 3D |
| `Primeira Versão` → `Principais`, `Alunas em geral` etc. | Fotos de pessoas reais (retratos) | ❌ Não usar (imagem de pessoas reais) |
| Demais pastas (`Materiais`, `Práticas`, capas de livros, screenshots e fotos de 2019, podcasts .m4a) | Material pedagógico e pessoal | ❌ |

---

## 3. Assets reaproveitáveis

| Asset (Drive) | O que é (verificado) | Uso em Ecos de Valdoria |
|---|---|---|
| `Spritesheet/Chamas no chão.png` (2172×724) | 6 quadros de chamas no chão, da ignição ao fogo baixo | Chão em chamas do **Meteoro Ancestral** (Mago), lava das Minas, ataque do **Golem de Magma** |
| `Spritesheet/Projeçao do Taco.png` (1774×887) | 4 arcos de corte brancos com rastro | **Slash VFX** do combo do Guerreiro e da Ladina (aplicar tint por classe) |
| `Spritesheet/Sprite Sheet de Gosma Tóxica Retro.png` (1672×941) | 12 quadros de projétil ácido verde em voo e respingo | Cuspe do **Lodo Pútrido** e magia da **Bruxa Morvena** |
| `Spritesheet/Atlas de Efeitos Ambientais em Pixel Art.png` (1536×1024) | Neblina baixa/alta, folhas rolando e no ar, poeira ao andar/correr, linhas de vento, detritos, partículas | Névoa de Brumaverde e do Pântano, poeira de corrida/pouso, vento das Ruínas (descartar a linha "papel") |
| `Aventura de Luis/images/.../explosion_0…8.png`, `bomb_*.png` | Explosão em 9 quadros + bomba (Kenney, CC0) | Bombas dos **Kobolds Mineiros** — placeholder até arte definitiva (estilo cartoon) |
| `Planta vs Cubinhos/build/images/planty*.gif` | Planta 37×59, 3 quadros idle + 1 tiro | Placeholder de inimigo-planta em Brumaverde |
| `sounds/sfx_coin_*` | Moedas | Coleta de ouro e itens |
| `sounds/sfx_exp_medium5`, `sfx_exp_various4` | Explosões | Magias e morte de chefe |
| `sounds/sfx_movement_footsteps1a/1b` | Passos | Passos |
| `sounds/sfx_movement_portal2` | Portal | Fim de fase / teletransporte do Mago |
| `sounds/sfx_sounds_impact11` | Impacto | Golpe acertando |
| `sounds/sfx_sounds_falling*` | Queda | Queda em abismo |
| `sounds/sfx_sounds_pause*_in`, `sfx_sounds_error3`, `sfx_sound_nagger2` | UI | Pausa, ação inválida, alerta |

**Tratamento necessário nos atlas gerados por IA:** vários estão em RGB com fundo preto (sem transparência), em grid irregular e com quadros de ~250 px. Antes de usar é preciso remover o fundo, recortar em grid uniforme e reduzir para a escala do jogo (personagem ~40 px de altura) com redução de paleta. Isso será feito por script no pipeline de build (`tools/slice-atlas`).

> **Recomendação:** baixar o pack completo *The Essential Retro Video Game Sound Effects Collection [512 sounds]* (CC0, mesmo autor). Ele já contém espada (`sfx_wpn_sword1-3`), adaga, socos, pulo/pouso (20 variações), menu, power-up, level-up (fanfarras), alarme de vida baixa e gritos de morte — cobre ~70% dos SFX faltantes sem custo.

---

## 4. O que FALTA (lista de produção)

Legenda de prioridade: **P0** = necessário para o protótipo jogável · **P1** = versão completa · **P2** = polimento.

### 4.1 Personagens jogáveis (4 classes) — tudo faltando

Frame base **64×64 px** (personagem ocupa ~24×40), olhando para a direita (espelhamento no código).

| Animação | Frames | Guerreiro | Arqueira | Mago | Ladina |
|---|---|---|---|---|---|
| idle | 6 | P0 | P0 | P0 | P0 |
| run | 8 | P0 | P0 | P0 | P0 |
| jump / fall / land | 3 / 2 / 2 | P0 | P0 | P0 | P0 |
| dash / esquiva | 4 | P0 | P0 | P0 | P0 |
| ataque básico (combo 3 golpes) | 4+4+5 | P0 | P0 | P0 | P0 |
| ataque aéreo | 4 | P1 | P1 | P1 | P1 |
| habilidade 1 | 6 | P0 | P0 | P0 | P0 |
| habilidade 2 | 6 | P1 | P1 | P1 | P1 |
| ultimate | 8–10 | P1 | P1 | P1 | P1 |
| hurt | 2 | P0 | P0 | P0 | P0 |
| death | 6 | P0 | P0 | P0 | P0 |
| retrato (HUD 32×32 + seleção 128×128) | — | P0 | P0 | P0 | P0 |
| arte de seleção de classe (corpo inteiro) | — | P1 | P1 | P1 | P1 |

**Total aproximado:** ~70 frames por classe → **~280 frames**.

### 4.2 Projéteis e VFX de combate — tudo faltando

| Asset | Prioridade |
|---|---|
| Rastro de corte (slash) 3 variações | P0 — **4 arcos disponíveis** (`Projeçao do Taco`) |
| Faísca de impacto (hit spark) | P0 |
| Flecha + flecha carregada + chuva de flechas | P0 |
| Bola de fogo, lança de gelo, corrente de raio, meteoro | P0 / P1 — **chão em chamas disponível** (`Chamas no chão`) |
| Adagas arremessadas, nuvem de fumaça, rastro de sombra | P0 / P1 |
| Escudo / aura (Guerreiro), círculo arcano (Mago) | P1 |
| Explosão de morte de inimigo (fumaça + almas) | P0 — explosão Kenney como placeholder |
| Level-up (pilar de luz), cura, buff, debuff (veneno, queimadura, congelamento) | P1 |
| Números de dano (fonte bitmap) | P0 |

### 4.3 Inimigos comuns (hordas) — 0 de 15 disponíveis

Frame base 32×32 (pequenos), 48×48 (médios), 64×64 (grandes). Animações mínimas: idle, walk, attack, hurt, death.

| Região | Inimigo | Tamanho | Status |
|---|---|---|---|
| 1 Brumaverde | Goblin Saqueador | 32 | Falta (P0) |
| 1 Brumaverde | Goblin Lanceiro | 32 | Falta (P0) |
| 1 Brumaverde | Lobo Sombrio | 48 | Falta (P0) |
| 2 Pântano Cinzento | Esqueleto Afogado | 48 | Falta (P1) |
| 2 Pântano Cinzento | Aranha Tecelã | 32 | Falta (P1) |
| 2 Pântano Cinzento | Lodo Pútrido | 32 | Falta (P1) — o projétil ácido já existe |
| 3 Minas de Ferroprofundo | Kobold Mineiro | 32 | Falta (P1) |
| 3 Minas de Ferroprofundo | Morcego de Cristal | 32 | Falta (P1) |
| 3 Minas de Ferroprofundo | Golem de Pedra | 64 | Falta (P1) |
| 4 Ruínas de Aethel | Cultista do Eclipse | 48 | Falta (P1) |
| 4 Ruínas de Aethel | Gárgula | 48 | Falta (P1) |
| 4 Ruínas de Aethel | Cavaleiro Caído | 64 | Falta (P1) |
| 5 Cidadela do Eclipse | Cria do Vazio | 32 | Falta (P1) |
| 5 Cidadela do Eclipse | Sentinela Eclipsada | 64 | Falta (P1) |
| 5 Cidadela do Eclipse | Devorador de Luz | 48 | Falta (P1) |

**Variantes de elite** (paleta alternativa + aura) podem ser geradas por shader/tint no código — não exigem arte extra.

### 4.4 Chefes — 0 de 5 disponíveis

Frame 96×96 a 160×160; animações: intro, idle, 3 ataques, transição de fase, hurt, death.

| Chefe | Região | Prioridade |
|---|---|---|
| Grukk, o Rei Goblin | 1 | P0 |
| Morvena, a Bruxa do Lodo | 2 | P1 |
| Brasa-Viva, o Golem de Magma | 3 | P1 |
| Sir Aldric, o Cavaleiro Negro | 4 | P1 |
| Vaelor, o Arauto do Eclipse (2 fases) | 5 | P1 |

### 4.5 Cenários — tudo faltando

Por região: **tileset 16×16** (chão, plataformas, rampas, paredes, decoração) + **parallax de 4–5 camadas** em 480×270 + props.

| Região | Tileset | Parallax | Props | Prioridade |
|---|---|---|---|---|
| 1 Floresta de Brumaverde | Falta | Falta | Falta (árvores, cogumelos, acampamento goblin) | P0 |
| 2 Pântano Cinzento | Falta | Falta | Falta | P1 |
| 3 Minas de Ferroprofundo | Falta | Falta | Falta (trilhos, carrinhos, cristais, lava) | P1 |
| 4 Ruínas de Aethel | Falta | Falta | Falta | P1 |
| 5 Cidadela do Eclipse | Falta | Falta | Falta | P1 |
| Hub: Vila de Pedralume (loja, ferreiro, treino) | Falta | Falta | Falta | P2 |

Efeitos ambientais: **parcial** (atlas do Drive — neblina, folhas, poeira, vento). Faltam chuva, brasas, bolhas do pântano, partículas do vazio (P1).

### 4.6 Itens e coletáveis — tudo faltando

| Asset | Prioridade |
|---|---|
| Moeda de ouro (animada), gema de alma (XP) | P0 |
| Poções de vida e mana (P/M/G) | P0 |
| Baú (fechado/abrindo/aberto), barril e caixote quebráveis | P1 |
| Ícones de equipamentos: 4 armas × 3 tiers, armadura, amuleto, anel | P1 |
| Fragmentos do Selo (item de história, 5) | P1 |

### 4.7 Interface (UI/HUD) — tudo faltando

| Asset | Prioridade |
|---|---|
| Barras de HP / MP / XP + moldura com retrato | P0 |
| Ícones de habilidades (4 classes × 4 = 16) + overlay de cooldown | P0 |
| Barra de vida de chefe | P0 |
| Fonte bitmap pixel (acentos PT-BR obrigatórios) | P0 |
| Logo "Ecos de Valdoria" | P1 |
| Tela de título, seleção de classe, pausa, game over, vitória | P0 / P1 |
| Painel de level-up / árvore de habilidades, inventário, loja | P1 |
| Botões virtuais para mobile (direcional + 4 ações) | P1 |
| Caixa de diálogo + retratos de NPCs (Elara, Ferreiro Borin) | P1 |
| Ícones PWA (192, 512, maskable, apple-touch) | P2 |

### 4.8 Áudio

| Categoria | Disponível | Falta |
|---|---|---|
| Música | Nenhuma (só um MIDI de terceiro, com direitos autorais — **não usar**) | Tema do menu, 5 temas de região, tema de chefe, chefe final, vitória, game over, vila (**10 faixas, P0: menu + região 1 + chefe**) |
| SFX combate | Impacto, explosões | Espada, flecha, magias (fogo/gelo/raio), adagas, esquiva, crítico, bloqueio |
| SFX movimento | Passos, quedas, portal | Pulo, pouso, dash |
| SFX inimigos | — | Rosnados/gritos por tipo, morte, rugidos de chefe |
| SFX UI/progressão | Moedas, pausa, erro | Navegação de menu, confirmar, level-up, coleta de poção, baú |
| Ambiência | — | Floresta, pântano, caverna, vento das ruínas, zumbido do vazio |

---

## 5. Especificações técnicas obrigatórias (para quem produzir os assets)

- **Estilo:** pixel art, contorno escuro de 1 px, iluminação vinda de cima-esquerda.
- **Paleta:** limitada e compartilhada (sugestão: *Endesga 64* ou *Resurrect 64*) para manter coerência entre artistas/IA.
- **Resolução base do jogo:** 480×270. Nunca redimensionar sprites com suavização (nearest-neighbor apenas).
- **Grid:** tiles 16×16; spritesheets em grid uniforme, sem espaçamento, fundo **transparente** (PNG-32). Os atlas atuais do Drive têm rótulos de texto e grid irregular — precisam ser limpos antes de usar.
- **Pivô:** pés do personagem centralizados na base do frame.
- **Nomenclatura:** `classe_animacao.png` (ex.: `guerreiro_run.png`), `inimigo_goblin_attack.png`, `tiles_brumaverde.png`, `bg_brumaverde_l1.png`.
- **Áudio:** SFX em `.ogg` + `.mp3` (fallback), mono, 44.1 kHz; músicas em `.ogg`, loop sem emenda.
- **Licenças:** registrar autor e licença de cada asset de terceiros em `assets/CREDITS.md`.

## 6. Fontes sugeridas para cobrir as lacunas

| Necessidade | Opção gratuita/barata |
|---|---|
| Classes de fantasia | Packs "Fantasy Knight / Archer / Wizard / Rogue" no itch.io (vários CC0 ou licença comercial barata) |
| Inimigos e chefes | Packs "Monsters Creatures Fantasy", "Goblin / Skeleton pack" (itch.io, OpenGameArt) |
| Tilesets + parallax | "Legacy Fantasy", "Oak Woods", "Cave tileset" (itch.io) |
| SFX | Pack completo Juhani Junkala 512 (CC0) — já parcialmente no Drive |
| Música | OpenGameArt (CC0/CC-BY), ou composição própria |
| Geração por IA | Viável para retratos e artes de seleção; para spritesheets animadas exige limpeza manual (como visto nos atlas do Drive) |

## 7. Estratégia para não travar o desenvolvimento

O código será escrito com **placeholders procedurais** (formas geométricas coloridas por classe/inimigo, gerados em runtime) e um **manifesto de assets** (`assets/manifest.json`). Quando o sprite real chegar, basta colocá-lo na pasta com o nome padronizado — o jogo troca o placeholder automaticamente. Assim o protótipo jogável não depende da produção de arte.
