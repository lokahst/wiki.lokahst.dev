---
title: Configuration
description: Default settings from configs
updated: July 19, 2026
---

:::spoiler achievements.yml
```yaml
#####################################################################
# Note: Plugin is in Early Access - its very experimental right now #
#####################################################################

enabled: true
entries:
  first_discovery:
    display-name: "Beyond the Hearth"
    reward-experience: 20
  first_rare_fish:
    display-name: "A Fisher's Tale"
    reward-experience: 35
  legendary_catch:
    display-name: "Whisper of the Deep"
    reward-experience: 150
  first_elite:
    display-name: "Proven in Danger"
    reward-experience: 60
  first_quest:
    display-name: "A Tale Brought Home"
    reward-experience: 30
  quest_veteran:
    display-name: "Road-Worn Hero"
    reward-experience: 200
  five_enchantments:
    display-name: "Rune Scholar"
    reward-experience: 80
  level_fifty:
    display-name: "Legend in the Making"
    reward-experience: 250
  master_skill:
    display-name: "Master of a Discipline"
    reward-experience: 250
```
:::

:::spoiler alchemy.yml
```yaml
#####################################################################
# Note: Plugin is in Early Access - its very experimental right now #
#####################################################################

schema-version: 1

enabled: true
messages:
  no-curable-injury: "&7You have no LOTN injury that this potion can cure."
study:
  learn-chance: 0.30
  skill-xp-success: 6.0
  skill-xp-failure: 1.0
brewing:
  skill-xp: 12.0
  alchemy-buff-duration-seconds: 300
  alchemy-buff-strength: 0.15
  fishing-buff-duration-seconds: 60
  fishing-extra-catch-chance: 0.35
  weightless-duration-seconds: 300
  weightless-capacity-bonus: 0.20

ingredients:
  SWEET_BERRIES: [RESTORE_HEALTH, CURE]
  POTATO: [RESTORE_STAMINA, FORTIFY_WEIGHT]
  SPIDER_EYE: [CURE, FORTIFY_ALCHEMY]
  CARROT: [RESTORE_HEALTH, FORTIFY_FISHING]
  WHEAT: [RESTORE_STAMINA, FORTIFY_WEIGHT]
  EGG: [RESTORE_HEALTH, CURE]
  FEATHER: [FORTIFY_WEIGHT, FORTIFY_FISHING]
  NETHER_WART: [FORTIFY_ALCHEMY, CURE]
  GLOWSTONE_DUST: [RESTORE_HEALTH, FORTIFY_ALCHEMY]
  GUNPOWDER: [FORTIFY_FISHING, FORTIFY_ALCHEMY]
  FERMENTED_SPIDER_EYE: [CURE, FORTIFY_ALCHEMY]
  BLAZE_POWDER: [RESTORE_STAMINA, FORTIFY_ALCHEMY]
  SUGAR: [RESTORE_STAMINA, FORTIFY_WEIGHT]
  RABBIT_FOOT: [FORTIFY_WEIGHT, CURE, RESTORE_STAMINA]
  FLOWER: [RESTORE_HEALTH, CURE]
  BAMBOO: [FORTIFY_FISHING, FORTIFY_WEIGHT]
  SUGAR_CANE: [FORTIFY_FISHING, RESTORE_STAMINA]
  SEEDS: [RESTORE_STAMINA, FORTIFY_FISHING]
  KELP: [FORTIFY_FISHING, CURE]

recipes:
  cure:
    display-name: "Potion of Cure"
    ingredients: [SPIDER_EYE, FERMENTED_SPIDER_EYE, FLOWER]
    effect: CURE
    color: "88CC88"
  fishing:
    display-name: "Potion of Fishing"
    ingredients: [KELP, GUNPOWDER, SUGAR_CANE]
    effect: FISHING
    color: "3FA7D6"
  alchemy:
    display-name: "Potion of Alchemy"
    ingredients: [NETHER_WART, BLAZE_POWDER, GLOWSTONE_DUST]
    effect: ALCHEMY
    color: "9B59B6"
  weightless:
    display-name: "Weightless Potion"
    ingredients: [FEATHER, BAMBOO, RABBIT_FOOT]
    effect: WEIGHTLESS
    color: "E6E6FA"
  minor_health:
    display-name: "Minor Potion of Health"
    ingredients: [SWEET_BERRIES, CARROT, FLOWER]
    effect: HEALTH
    potency: 4.0
    color: "D94B4B"
  health:
    display-name: "Potion of Health"
    ingredients: [SWEET_BERRIES, EGG, GLOWSTONE_DUST]
    effect: HEALTH
    potency: 10.0
    color: "B71C1C"
  greater_health:
    display-name: "Greater Potion of Health"
    ingredients: [SWEET_BERRIES, GLOWSTONE_DUST, RABBIT_FOOT]
    effect: HEALTH
    potency: 20.0
    color: "7F0000"
  minor_stamina:
    display-name: "Minor Potion of Stamina"
    ingredients: [SEEDS, WHEAT, SUGAR]
    effect: STAMINA
    potency: 15.0
    color: "66BB6A"
  stamina:
    display-name: "Potion of Stamina"
    ingredients: [POTATO, BLAZE_POWDER, RABBIT_FOOT]
    effect: STAMINA
    potency: 30.0
    color: "2E7D32"
```
:::

:::spoiler attributes.yml
```yaml
#####################################################################
# Note: Plugin is in Early Access - its very experimental right now #
#####################################################################

settings:
  enabled: true
  points-per-character-level: 1
  migration-points-per-existing-level: 1
  max-points-per-attribute: 50

strength:
  melee-damage-per-point: 0.005
  carry-weight-per-point: 2.5
agility:
  movement-speed-per-point: 0.002
  dodge-chance-per-point: 0.0015
  max-dodge-chance: 0.12
endurance:
  stamina-per-point: 3.0
  injury-resistance-per-point: 0.01
  temperature-resistance-per-point: 0.01
intelligence:
  magicka-per-point: 3.0
wisdom:
luck:
  rare-roll-bonus-per-point: 0.002
```
:::

:::spoiler bosses.yml
```yaml
#####################################################################
# Note: Plugin is in Early Access - its very experimental right now #
#####################################################################

schema-version: 4

enabled: true
respect-existing-custom-name: true

format:
  name-color: "&5"
  custom-name-visible: false

names:
  ender-dragon:
    display-name: "Enderodian"
    level: 80
    maximum-health: 400.0
  wither:
    display-name: "Wither"
    level: 70
    maximum-health: 200.0
  elder-guardian:
    display-name: "Leviathan"
    level: 55
    maximum-health: 120.0
  warden:
    display-name: "Ehrnal"
    level: 75
    maximum-health: 700.0

dragon:
  enhanced-ai-enabled: true
  tick-interval: 10
  target-range: 80.0
  decision-interval-ticks: 70
  phase-steering-enabled: true
  fire-breath:
    enabled: true
    chance-per-decision: 0.35
    cooldown-ticks: 260
    windup-ticks: 24
    range: 45.0
    cone-angle-degrees: 18.0
    damage: 7.0
    fire-ticks: 80
    duration-ticks: 12
    particles-per-step: 26
    respect-line-of-sight: true
  wing-gust:
    enabled: true
    chance-per-decision: 0.45
    cooldown-ticks: 140
    range: 11.0
    damage: 3.0
    horizontal-force: 1.8
    vertical-force: 0.35
```
:::

:::spoiler codex.yml
```yaml
#####################################################################
# Note: Plugin is in Early Access - its very experimental right now #
#####################################################################

enabled: true
categories:
  fish:
    display-name: "Fish"
    icon: COD
  discovery:
    display-name: "Discoveries"
    icon: COMPASS
  enchant:
    display-name: "Enchantments"
    icon: ENCHANTED_BOOK
  faction:
    display-name: "Factions"
    icon: SHIELD
  quest:
    display-name: "Completed Tales"
    icon: WRITABLE_BOOK
  elite:
    display-name: "Elite Enemies"
    icon: WITHER_SKELETON_SKULL
  achievement:
    display-name: "Achievements"
    icon: NETHER_STAR
```
:::

:::spoiler combat.yml
```yaml
#####################################################################
# Note: Plugin is in Early Access - its very experimental right now #
#####################################################################

schema-version: 3

critical:
  base-chance: 0.05
  base-multiplier: 1.5
  max-chance: 0.75
  heavy-armor-penalty: -0.02

ambient-effects:
  enabled: false

bleed:
  base-chance: 0.08
  duration-ticks: 60
  damage-per-tick: 1.0
  interval-ticks: 20

poison:
  base-chance: 0.05
  duration-ticks: 100
  level: 1

burn:
  chance: 0.10
  ticks: 40

frost:
  chance: 0.10
  duration-ticks: 60
  level: 2
  damage-multiplier: 1.0
  freeze-mobs: true

shock:
  chance: 0.08
  duration-ticks: 40
  level: 1
  damage-multiplier: 1.15
  chain-chance: 0.25
  chain-radius: 3.0

damage-variation: 0.1
max-damage-reduction: 0.8

mob-shield-damage:
  enabled: true
  base-damage-through: 0.10
  damage-through-per-level: 0.0075
  minimum-damage-through: 0.05
  maximum-damage-through: 0.75

combat-effects:
  secondary-damage:
    allow-pvp: false
    allow-friendly-mobs: false
  mob-dodge:
    enabled: true
    base-chance: 0.02
    chance-per-tier: 0.008
    maximum-chance: 0.12
  particles:
    enabled: true
    viewing-distance: 32.0
    dodge:
      amount: 5
    hit:
      amount: 4
      damage-indicator-amount: 1
    burning:
      interval-ticks: 8
      amount: 3
      small-flame-chance: 0.35
    freezing:
      interval-ticks: 8
      amount: 3
      snowflake-chance: 0.45
```
:::

:::spoiler config.yml
```yaml
#####################################################################
# Note: Plugin is in Early Access - its very experimental right now #
#####################################################################

schema-version: 14

leveling:
  max-level: 100
  base-required: 125.0
  growth: 1.45
  xp-curve:
    base-xp: 125.0
    exponent: 1.80
  perk-points-per-level: 1
  legacy-direct-xp-enabled: false
  show-gain-message: false
  skill-level-contribution:
    base-xp: 75.0
    skill-level-exponent: 1.35
    overlevel-gap-penalty: 0.018
    minimum-diversity-multiplier: 0.65
  messages:
    level-up: "&6Level increased to {level}. &ePerk Points: {perk_points}"
    attribute-choice: "&eChoose Health, Stamina, or Magicka to increase by 10. Pending choices: {pending_choices}."
    xp-gain: "&7LotN: +{amount} overall XP from {reason}."
  feedback:
    enabled: true
    sound: UI_TOAST_CHALLENGE_COMPLETE
    sound-volume: 0.65
    sound-pitch: 1.2
    particle: END_ROD
    particle-amount: 12

systems:
  attributes: true
  skills: true
  quests: true
  discovery: true
  reputation: true
  codex: true
  achievements: true
  fishing: true
  temperature: true
  injuries: true
  weight: true
  fast-travel: true
  water-currents: true
  mob-scaling: true
  alchemy: true

# Player Shout controls. Existing effect values remain under each Shout.
shouts:
  enabled-by-default: true
  unlocked-words-by-default: 3
  activation:
    double-shift-window-ms: 350
  gui:
    title: "Shouts"
    show-locked-shouts: true
    show-cooldowns: true
    show-magicka-cost: true
  unrelenting-force:
    cooldown-seconds: 12
    magicka-cost: 25
    range: 10.0
    cone-angle-degrees: 55.0
    damage: 2.0
    horizontal-force: 2.4
    vertical-force: 0.45
    stagger-duration-ticks: 40
    affect-players: false
    affect-tamed-animals: false
    respect-line-of-sight: true
    force:
      minimum-distance-multiplier: 0.45
      minimum-edge-multiplier: 0.65
      small-mob-multiplier: 1.15
      large-mob-multiplier: 0.70
      iron-golem-multiplier: 0.45
      ravager-multiplier: 0.45
      warden-multiplier: 0.25
      wither-multiplier: 0.15
      maximum-horizontal-velocity: 3.0
    visual:
      rings: 7
      particles-per-ring: 18
      duration-ticks: 5
  whirlwind-sprint:
    cooldown-seconds: 10
    magicka-cost: 25
    distance-by-words: [7.0, 11.0, 15.0]
    speed-by-words: [2.0, 2.6, 3.2]
    safety-margin: 1.25
  fire-breath:
    cooldown-seconds: 18
    magicka-cost: 30
    range-by-words: [10.0, 14.0, 18.0]
    damage-by-words: [4.0, 7.0, 10.0]
    fire-ticks-by-words: [80, 120, 160]
    cone-angle-degrees: 55.0
    affect-players: false
    affect-tamed-animals: false
    respect-line-of-sight: true
    dragon-damage-multiplier: 0.15
    visual:
      rings: 12
      particles-per-ring: 28
      duration-ticks: 12
  become-ethereal:
    cooldown-seconds: 45
    magicka-cost: 35
    duration-ticks-by-words: [60, 100, 160]

worlds:
  whitelist: []
  blacklist: []

storage:
  autosave-ticks: 6000
  backup-legacy-profiles: true

character-creation:
  enabled: true
  setup-title: "&0Create your LOTN Character"
  admin-bypass-permission: lotn.admin.character.bypass
  chat-input:
    prompt: "&6Type your LOTN character name in chat. Type &ecancel &6to stop."
    cancel-word: "cancel"
  name:
    minimum-length: 3
    maximum-length: 20
    allowed-pattern: "[A-Za-z][A-Za-z0-9 _'\\-]*"
    blacklist: []
    unique: true
  command-whitelist:
    - "/lotn character"
    - "/character"
    - "/help"
    - "/msg"
    - "/tell"
    - "/login"
    - "/register"

vitals:
  health-upgrade: 10.0
  stamina-upgrade: 10.0
  magicka-upgrade: 10.0
  health-display-per-minecraft-health: 5.0
  health-scale: 20.0
  stamina-drain-multiplier: 0.50
  stamina-sprint-drain-per-second: 10.0
  stamina-shield-drain-per-second: 12.0
  stamina-regen-per-second: 18.0
  exhaustion-slowness-level: 5
  exhaustion-duration-ticks: 40
  exhaustion-recovery-threshold: 0.25
  magicka-regen-per-second: 20.0
  empty-stamina-shield-cooldown-ticks: 25
  attacks:
    sword-cost: 2.0
    axe-cost: 3.5
    mace-cost: 5.0
    spear-cost: 3.0
    ranged-cost: 2.5
    regeneration-delay-ticks: 80
    exhausted-cooldown-ticks: 24

world-settings:
  disable-vanilla-enchanting: true

trading:
  enabled: true
  price-multiplier: 1.4

weight:
  base-capacity: 200.0
  heavy-armor-capacity-per-rank: 10.0
  heavy-armor-capacity-max: 50.0
  light-armor-capacity-per-rank: 6.0
  light-armor-capacity-max: 30.0
  heavy-regen-multiplier: 0.5
```
:::

:::spoiler custom-enchants.yml:
```yaml
#####################################################################
# Note: Plugin is in Early Access - its very experimental right now #
#####################################################################

mob-drops:
  base-chance: 0.035
  chance-per-mob-level: 0.00035
  max-chance: 0.12

knowledge:
  learn-skill-xp: 12.0
  apply-skill-xp: 3.0

effects:
  flame:
    fire-ticks: 80
  frostbite:
    duration-ticks: 60
  shockwave:
    nausea-duration-ticks: 40
    slow-duration-ticks: 40
  poisoned:
    duration-ticks: 80
  critical_strike:
    chance: 0.10
    multiplier: 0.5
  lifesteal:
    percent: 0.10
  frozen_edge:
    duration-ticks: 100
  block:
    damage-reduction: 0.08
  windwalker:
    speed-bonus: 0.05
  springheeled:
    jump-boost-level: 1
  feather_fall:
    damage-reduction: 0.50
  bear:
    health-bonus: 0.20
  vitality:
    regen-interval-ticks: 20
  rebreathing:
    air-replenish-ticks: 300
  fortitude:
    knockback-resistance: 0.25
```
:::

:::spoiler discoveries.yml
```yaml
#####################################################################
# Note: Plugin is in Early Access - its very experimental right now #
#####################################################################

enabled: true
check-cell-size: 32
milestones:
  high-mountain-y: 180
  deep-underground-y: -20
rewards:
  biome:
    experience: 12
  dimension:
    experience: 60
  milestone:
    experience: 35
```
:::

:::spoiler effects.yml
```yaml
#####################################################################
# Note: Plugin is in Early Access - its very experimental right now #
#####################################################################

schema-version: 4
enabled: true
combat:
  enabled: true
  legacy-weapon-impacts-enabled: false
  particles-per-hit: 7
  boss-particle-multiplier: 3
  boss-burst-cooldown-ms: 300
  boss-death-particles: 75
fishing:
  enabled: true
  cast-particles: 5
  catch-particles: 14
quests:
  enabled: true
  accept-particles: 12
  complete-particles: 35
discoveries:
  enabled: true
  particles: 14
alchemy:
  enabled: true
  learn-particles: 18
  brew-particles: 24
  potion-particles: 16
```
:::

:::spoiler equipment.yml
```yaml
#####################################################################
# Note: Plugin is in Early Access - its very experimental right now #
#####################################################################

schema-version: 2
debug: false

armor:
  reduction-scaling: 250.0
  maximum-reduction: 0.70
  mitigated-causes:
    - ENTITY_ATTACK
    - ENTITY_SWEEP_ATTACK
    - PROJECTILE
    - ENTITY_EXPLOSION
    - BLOCK_EXPLOSION
  unmitigated-causes:
    - VOID
    - KILL
    - SONIC_BOOM

quality:
  levels:
    0: {name: "Normal", bonus: 0.00, required-smithing: 0, material-cost: 0}
    1: {name: "Fine", bonus: 0.04, required-smithing: 15, material-cost: 1}
    2: {name: "Superior", bonus: 0.08, required-smithing: 30, material-cost: 2}
    3: {name: "Exquisite", bonus: 0.12, required-smithing: 50, material-cost: 3}
    4: {name: "Flawless", bonus: 0.16, required-smithing: 70, material-cost: 4}
    5: {name: "Legendary", bonus: 0.20, required-smithing: 90, material-cost: 5}

tempering:
  enabled: true
  enforce-material-perks: false
  enchanted-items-require-perk: arcane_blacksmith
  allow-shift-click-result: false
  smithing-xp-base: 8.0
  smithing-xp-tier-multiplier: 0.35
  smithing-xp-quality-multiplier: 0.50
  armor-weight-increase-per-quality-rank: 0.025

# One immutable definition is produced for every entry. Lore is never used as data.
definitions:
  WOODEN_SWORD: {kind: WEAPON, category: one_handed, base-damage: 4, attack-speed: 1.6, weight: 2.0, material-tier: 0, material-family: wood, tempering-material: OAK_PLANKS, relevant-skill: one_handed, smithing-perk: leatherworking, maximum-quality-rank: 5}
  STONE_SWORD: {kind: WEAPON, category: one_handed, base-damage: 5, attack-speed: 1.6, weight: 3.0, material-tier: 1, material-family: stone, tempering-material: COBBLESTONE, relevant-skill: one_handed, smithing-perk: toolsmith, maximum-quality-rank: 5}
  COPPER_SWORD: {kind: WEAPON, category: one_handed, base-damage: 5, attack-speed: 1.6, weight: 4.0, material-tier: 2, material-family: copper, tempering-material: COPPER_INGOT, relevant-skill: one_handed, smithing-perk: toolsmith, maximum-quality-rank: 5}
  IRON_SWORD: {kind: WEAPON, category: one_handed, base-damage: 6, attack-speed: 1.6, weight: 5.0, material-tier: 2, material-family: iron, tempering-material: IRON_INGOT, relevant-skill: one_handed, smithing-perk: iron_smithing, maximum-quality-rank: 5}
  GOLDEN_SWORD: {kind: WEAPON, category: one_handed, base-damage: 4, attack-speed: 1.6, weight: 4.0, material-tier: 2, material-family: gold, tempering-material: GOLD_INGOT, relevant-skill: one_handed, smithing-perk: golden_smithing, maximum-quality-rank: 5}
  DIAMOND_SWORD: {kind: WEAPON, category: one_handed, base-damage: 7, attack-speed: 1.6, weight: 4.0, material-tier: 3, material-family: diamond, tempering-material: DIAMOND, relevant-skill: one_handed, smithing-perk: diamond_smithing, maximum-quality-rank: 5}
  NETHERITE_SWORD: {kind: WEAPON, category: one_handed, base-damage: 8, attack-speed: 1.6, weight: 7.0, material-tier: 4, material-family: netherite, tempering-material: NETHERITE_INGOT, relevant-skill: one_handed, smithing-perk: netherite_smithing, maximum-quality-rank: 5}

  WOODEN_AXE: {kind: WEAPON, category: one_handed, base-damage: 7, attack-speed: 0.8, weight: 3.0, material-tier: 0, material-family: wood, tempering-material: OAK_PLANKS, relevant-skill: one_handed, smithing-perk: toolsmith, maximum-quality-rank: 5}
  STONE_AXE: {kind: WEAPON, category: one_handed, base-damage: 9, attack-speed: 0.8, weight: 5.0, material-tier: 1, material-family: stone, tempering-material: COBBLESTONE, relevant-skill: one_handed, smithing-perk: toolsmith, maximum-quality-rank: 5}
  COPPER_AXE: {kind: WEAPON, category: one_handed, base-damage: 8, attack-speed: 0.9, weight: 6.0, material-tier: 2, material-family: copper, tempering-material: COPPER_INGOT, relevant-skill: one_handed, smithing-perk: toolsmith, maximum-quality-rank: 5}
  IRON_AXE: {kind: WEAPON, category: one_handed, base-damage: 9, attack-speed: 0.9, weight: 7.0, material-tier: 2, material-family: iron, tempering-material: IRON_INGOT, relevant-skill: one_handed, smithing-perk: toolsmith, maximum-quality-rank: 5}
  GOLDEN_AXE: {kind: WEAPON, category: one_handed, base-damage: 7, attack-speed: 1.0, weight: 6.0, material-tier: 2, material-family: gold, tempering-material: GOLD_INGOT, relevant-skill: one_handed, smithing-perk: toolsmith, maximum-quality-rank: 5}
  DIAMOND_AXE: {kind: WEAPON, category: one_handed, base-damage: 9, attack-speed: 1.0, weight: 6.0, material-tier: 3, material-family: diamond, tempering-material: DIAMOND, relevant-skill: one_handed, smithing-perk: toolsmith, maximum-quality-rank: 5}
  NETHERITE_AXE: {kind: WEAPON, category: one_handed, base-damage: 10, attack-speed: 1.0, weight: 9.0, material-tier: 4, material-family: netherite, tempering-material: NETHERITE_INGOT, relevant-skill: one_handed, smithing-perk: toolsmith, maximum-quality-rank: 5}
  MACE: {kind: WEAPON, category: one_handed, base-damage: 6, attack-speed: 0.6, weight: 16.0, material-tier: 3, material-family: mace, tempering-material: BREEZE_ROD, relevant-skill: one_handed, smithing-perk: advanced_smithing, maximum-quality-rank: 5}
  BOW: {kind: WEAPON, category: bow, base-damage: 6, attack-speed: 1.0, weight: 3.0, material-tier: 0, material-family: bow, tempering-material: STRING, relevant-skill: archery, smithing-perk: leatherworking, maximum-quality-rank: 5}
  CROSSBOW: {kind: WEAPON, category: crossbow, base-damage: 9, attack-speed: 0.75, weight: 8.0, material-tier: 2, material-family: crossbow, tempering-material: IRON_INGOT, relevant-skill: archery, smithing-perk: iron_smithing, maximum-quality-rank: 5}
  TRIDENT: {kind: WEAPON, category: spear, base-damage: 9, attack-speed: 1.1, weight: 8.0, material-tier: 3, material-family: prismarine, tempering-material: PRISMARINE_SHARD, relevant-skill: "", smithing-perk: advanced_smithing, maximum-quality-rank: 5}
  WOODEN_SPEAR: {kind: WEAPON, category: spear, base-damage: 4, attack-speed: 1.2, weight: 2.5, material-tier: 0, material-family: wood, tempering-material: OAK_PLANKS, relevant-skill: "", smithing-perk: toolsmith, maximum-quality-rank: 5}
  STONE_SPEAR: {kind: WEAPON, category: spear, base-damage: 5, attack-speed: 1.2, weight: 4.0, material-tier: 1, material-family: stone, tempering-material: COBBLESTONE, relevant-skill: "", smithing-perk: toolsmith, maximum-quality-rank: 5}
  COPPER_SPEAR: {kind: WEAPON, category: spear, base-damage: 6, attack-speed: 1.2, weight: 5.0, material-tier: 2, material-family: copper, tempering-material: COPPER_INGOT, relevant-skill: "", smithing-perk: toolsmith, maximum-quality-rank: 5}
  IRON_SPEAR: {kind: WEAPON, category: spear, base-damage: 7, attack-speed: 1.2, weight: 6.0, material-tier: 2, material-family: iron, tempering-material: IRON_INGOT, relevant-skill: "", smithing-perk: toolsmith, maximum-quality-rank: 5}
  GOLDEN_SPEAR: {kind: WEAPON, category: spear, base-damage: 5, attack-speed: 1.3, weight: 4.5, material-tier: 2, material-family: gold, tempering-material: GOLD_INGOT, relevant-skill: "", smithing-perk: toolsmith, maximum-quality-rank: 5}
  DIAMOND_SPEAR: {kind: WEAPON, category: spear, base-damage: 8, attack-speed: 1.2, weight: 6.5, material-tier: 3, material-family: diamond, tempering-material: DIAMOND, relevant-skill: "", smithing-perk: toolsmith, maximum-quality-rank: 5}
  NETHERITE_SPEAR: {kind: WEAPON, category: spear, base-damage: 9, attack-speed: 1.2, weight: 9.0, material-tier: 4, material-family: netherite, tempering-material: NETHERITE_INGOT, relevant-skill: "", smithing-perk: toolsmith, maximum-quality-rank: 5}

  WOODEN_PICKAXE: {kind: TOOL, category: pickaxe, weight: 3.0, material-tier: 0, material-family: wood, tempering-material: OAK_PLANKS, relevant-skill: smithing, smithing-perk: toolsmith, maximum-quality-rank: 5}
  STONE_PICKAXE: {kind: TOOL, category: pickaxe, weight: 5.0, material-tier: 1, material-family: stone, tempering-material: COBBLESTONE, relevant-skill: smithing, smithing-perk: toolsmith, maximum-quality-rank: 5}
  COPPER_PICKAXE: {kind: TOOL, category: pickaxe, weight: 6.0, material-tier: 2, material-family: copper, tempering-material: COPPER_INGOT, relevant-skill: smithing, smithing-perk: toolsmith, maximum-quality-rank: 5}
  IRON_PICKAXE: {kind: TOOL, category: pickaxe, weight: 7.0, material-tier: 2, material-family: iron, tempering-material: IRON_INGOT, relevant-skill: smithing, smithing-perk: toolsmith, maximum-quality-rank: 5}
  GOLDEN_PICKAXE: {kind: TOOL, category: pickaxe, weight: 6.0, material-tier: 2, material-family: gold, tempering-material: GOLD_INGOT, relevant-skill: smithing, smithing-perk: toolsmith, maximum-quality-rank: 5}
  DIAMOND_PICKAXE: {kind: TOOL, category: pickaxe, weight: 6.0, material-tier: 3, material-family: diamond, tempering-material: DIAMOND, relevant-skill: smithing, smithing-perk: toolsmith, maximum-quality-rank: 5}
  NETHERITE_PICKAXE: {kind: TOOL, category: pickaxe, weight: 9.0, material-tier: 4, material-family: netherite, tempering-material: NETHERITE_INGOT, relevant-skill: smithing, smithing-perk: toolsmith, maximum-quality-rank: 5}
  WOODEN_HOE: {kind: TOOL, category: hoe, weight: 2.0, material-tier: 0, material-family: wood, tempering-material: OAK_PLANKS, relevant-skill: smithing, smithing-perk: toolsmith, maximum-quality-rank: 5}
  STONE_HOE: {kind: TOOL, category: hoe, weight: 3.0, material-tier: 1, material-family: stone, tempering-material: COBBLESTONE, relevant-skill: smithing, smithing-perk: toolsmith, maximum-quality-rank: 5}
  COPPER_HOE: {kind: TOOL, category: hoe, weight: 3.0, material-tier: 2, material-family: copper, tempering-material: COPPER_INGOT, relevant-skill: smithing, smithing-perk: toolsmith, maximum-quality-rank: 5}
  IRON_HOE: {kind: TOOL, category: hoe, weight: 4.0, material-tier: 2, material-family: iron, tempering-material: IRON_INGOT, relevant-skill: smithing, smithing-perk: toolsmith, maximum-quality-rank: 5}
  GOLDEN_HOE: {kind: TOOL, category: hoe, weight: 4.0, material-tier: 2, material-family: gold, tempering-material: GOLD_INGOT, relevant-skill: smithing, smithing-perk: toolsmith, maximum-quality-rank: 5}
  DIAMOND_HOE: {kind: TOOL, category: hoe, weight: 4.0, material-tier: 3, material-family: diamond, tempering-material: DIAMOND, relevant-skill: smithing, smithing-perk: toolsmith, maximum-quality-rank: 5}
  NETHERITE_HOE: {kind: TOOL, category: hoe, weight: 6.0, material-tier: 4, material-family: netherite, tempering-material: NETHERITE_INGOT, relevant-skill: smithing, smithing-perk: toolsmith, maximum-quality-rank: 5}

  LEATHER_HELMET: {kind: ARMOR, category: light_armor, armor-class: LIGHT, base-armor-rating: 5, weight: 3.0, material-tier: 0, material-family: leather, tempering-material: LEATHER, relevant-skill: light_armor, smithing-perk: leatherworking, maximum-quality-rank: 5}
  LEATHER_CHESTPLATE: {kind: ARMOR, category: light_armor, armor-class: LIGHT, base-armor-rating: 15, weight: 8.0, material-tier: 0, material-family: leather, tempering-material: LEATHER, relevant-skill: light_armor, smithing-perk: leatherworking, maximum-quality-rank: 5}
  LEATHER_LEGGINGS: {kind: ARMOR, category: light_armor, armor-class: LIGHT, base-armor-rating: 12, weight: 6.0, material-tier: 0, material-family: leather, tempering-material: LEATHER, relevant-skill: light_armor, smithing-perk: leatherworking, maximum-quality-rank: 5}
  LEATHER_BOOTS: {kind: ARMOR, category: light_armor, armor-class: LIGHT, base-armor-rating: 5, weight: 2.0, material-tier: 0, material-family: leather, tempering-material: LEATHER, relevant-skill: light_armor, smithing-perk: leatherworking, maximum-quality-rank: 5}
  CHAINMAIL_HELMET: {kind: ARMOR, category: light_armor, armor-class: LIGHT, base-armor-rating: 15, weight: 5.0, material-tier: 1, material-family: chainmail, tempering-material: IRON_NUGGET, relevant-skill: light_armor, smithing-perk: chain_smithing, maximum-quality-rank: 5}
  CHAINMAIL_CHESTPLATE: {kind: ARMOR, category: light_armor, armor-class: LIGHT, base-armor-rating: 25, weight: 13.0, material-tier: 1, material-family: chainmail, tempering-material: IRON_NUGGET, relevant-skill: light_armor, smithing-perk: chain_smithing, maximum-quality-rank: 5}
  CHAINMAIL_LEGGINGS: {kind: ARMOR, category: light_armor, armor-class: LIGHT, base-armor-rating: 20, weight: 10.0, material-tier: 1, material-family: chainmail, tempering-material: IRON_NUGGET, relevant-skill: light_armor, smithing-perk: chain_smithing, maximum-quality-rank: 5}
  CHAINMAIL_BOOTS: {kind: ARMOR, category: light_armor, armor-class: LIGHT, base-armor-rating: 8, weight: 4.0, material-tier: 1, material-family: chainmail, tempering-material: IRON_NUGGET, relevant-skill: light_armor, smithing-perk: chain_smithing, maximum-quality-rank: 5}
  GOLDEN_HELMET: {kind: ARMOR, category: light_armor, armor-class: LIGHT, base-armor-rating: 12, weight: 6.0, material-tier: 2, material-family: gold, tempering-material: GOLD_INGOT, relevant-skill: light_armor, smithing-perk: golden_smithing, maximum-quality-rank: 5}
  GOLDEN_CHESTPLATE: {kind: ARMOR, category: light_armor, armor-class: LIGHT, base-armor-rating: 25, weight: 15.0, material-tier: 2, material-family: gold, tempering-material: GOLD_INGOT, relevant-skill: light_armor, smithing-perk: golden_smithing, maximum-quality-rank: 5}
  GOLDEN_LEGGINGS: {kind: ARMOR, category: light_armor, armor-class: LIGHT, base-armor-rating: 15, weight: 12.0, material-tier: 2, material-family: gold, tempering-material: GOLD_INGOT, relevant-skill: light_armor, smithing-perk: golden_smithing, maximum-quality-rank: 5}
  GOLDEN_BOOTS: {kind: ARMOR, category: light_armor, armor-class: LIGHT, base-armor-rating: 8, weight: 5.0, material-tier: 2, material-family: gold, tempering-material: GOLD_INGOT, relevant-skill: light_armor, smithing-perk: golden_smithing, maximum-quality-rank: 5}
  TURTLE_HELMET: {kind: ARMOR, category: light_armor, armor-class: LIGHT, base-armor-rating: 18, weight: 5.0, material-tier: 1, material-family: turtle, tempering-material: TURTLE_SCUTE, relevant-skill: light_armor, smithing-perk: leatherworking, maximum-quality-rank: 5}

  COPPER_HELMET: {kind: ARMOR, category: heavy_armor, armor-class: HEAVY, base-armor-rating: 17, weight: 6.0, material-tier: 2, material-family: copper, tempering-material: COPPER_INGOT, relevant-skill: heavy_armor, smithing-perk: advanced_smithing, maximum-quality-rank: 5}
  COPPER_CHESTPLATE: {kind: ARMOR, category: heavy_armor, armor-class: HEAVY, base-armor-rating: 28, weight: 15.0, material-tier: 2, material-family: copper, tempering-material: COPPER_INGOT, relevant-skill: heavy_armor, smithing-perk: advanced_smithing, maximum-quality-rank: 5}
  COPPER_LEGGINGS: {kind: ARMOR, category: heavy_armor, armor-class: HEAVY, base-armor-rating: 22, weight: 12.0, material-tier: 2, material-family: copper, tempering-material: COPPER_INGOT, relevant-skill: heavy_armor, smithing-perk: advanced_smithing, maximum-quality-rank: 5}
  COPPER_BOOTS: {kind: ARMOR, category: heavy_armor, armor-class: HEAVY, base-armor-rating: 10, weight: 5.0, material-tier: 2, material-family: copper, tempering-material: COPPER_INGOT, relevant-skill: heavy_armor, smithing-perk: advanced_smithing, maximum-quality-rank: 5}
  IRON_HELMET: {kind: ARMOR, category: heavy_armor, armor-class: HEAVY, base-armor-rating: 20, weight: 7.0, material-tier: 2, material-family: iron, tempering-material: IRON_INGOT, relevant-skill: heavy_armor, smithing-perk: iron_smithing, maximum-quality-rank: 5}
  IRON_CHESTPLATE: {kind: ARMOR, category: heavy_armor, armor-class: HEAVY, base-armor-rating: 32, weight: 18.0, material-tier: 2, material-family: iron, tempering-material: IRON_INGOT, relevant-skill: heavy_armor, smithing-perk: iron_smithing, maximum-quality-rank: 5}
  IRON_LEGGINGS: {kind: ARMOR, category: heavy_armor, armor-class: HEAVY, base-armor-rating: 25, weight: 14.0, material-tier: 2, material-family: iron, tempering-material: IRON_INGOT, relevant-skill: heavy_armor, smithing-perk: iron_smithing, maximum-quality-rank: 5}
  IRON_BOOTS: {kind: ARMOR, category: heavy_armor, armor-class: HEAVY, base-armor-rating: 12, weight: 6.0, material-tier: 2, material-family: iron, tempering-material: IRON_INGOT, relevant-skill: heavy_armor, smithing-perk: iron_smithing, maximum-quality-rank: 5}
  DIAMOND_HELMET: {kind: ARMOR, category: heavy_armor, armor-class: HEAVY, base-armor-rating: 25, weight: 6.0, material-tier: 3, material-family: diamond, tempering-material: DIAMOND, relevant-skill: heavy_armor, smithing-perk: diamond_smithing, maximum-quality-rank: 5}
  DIAMOND_CHESTPLATE: {kind: ARMOR, category: heavy_armor, armor-class: HEAVY, base-armor-rating: 40, weight: 16.0, material-tier: 3, material-family: diamond, tempering-material: DIAMOND, relevant-skill: heavy_armor, smithing-perk: diamond_smithing, maximum-quality-rank: 5}
  DIAMOND_LEGGINGS: {kind: ARMOR, category: heavy_armor, armor-class: HEAVY, base-armor-rating: 30, weight: 13.0, material-tier: 3, material-family: diamond, tempering-material: DIAMOND, relevant-skill: heavy_armor, smithing-perk: diamond_smithing, maximum-quality-rank: 5}
  DIAMOND_BOOTS: {kind: ARMOR, category: heavy_armor, armor-class: HEAVY, base-armor-rating: 15, weight: 5.0, material-tier: 3, material-family: diamond, tempering-material: DIAMOND, relevant-skill: heavy_armor, smithing-perk: diamond_smithing, maximum-quality-rank: 5}
  NETHERITE_HELMET: {kind: ARMOR, category: heavy_armor, armor-class: HEAVY, base-armor-rating: 28, weight: 9.0, material-tier: 4, material-family: netherite, tempering-material: NETHERITE_INGOT, relevant-skill: heavy_armor, smithing-perk: netherite_smithing, maximum-quality-rank: 5}
  NETHERITE_CHESTPLATE: {kind: ARMOR, category: heavy_armor, armor-class: HEAVY, base-armor-rating: 45, weight: 24.0, material-tier: 4, material-family: netherite, tempering-material: NETHERITE_INGOT, relevant-skill: heavy_armor, smithing-perk: netherite_smithing, maximum-quality-rank: 5}
  NETHERITE_LEGGINGS: {kind: ARMOR, category: heavy_armor, armor-class: HEAVY, base-armor-rating: 35, weight: 20.0, material-tier: 4, material-family: netherite, tempering-material: NETHERITE_INGOT, relevant-skill: heavy_armor, smithing-perk: netherite_smithing, maximum-quality-rank: 5}
  NETHERITE_BOOTS: {kind: ARMOR, category: heavy_armor, armor-class: HEAVY, base-armor-rating: 18, weight: 8.0, material-tier: 4, material-family: netherite, tempering-material: NETHERITE_INGOT, relevant-skill: heavy_armor, smithing-perk: netherite_smithing, maximum-quality-rank: 5}
```
:::

:::spoiler factions.yml
```yaml
#####################################################################
# Note: Plugin is in Early Access - its very experimental right now #
#####################################################################

settings:
  enabled: true
  minimum: -1000
  maximum: 1000
  show-change-messages: true

ranks:
  hated:
    minimum: -1000
    display-name: "Hated"
  untrusted:
    minimum: -200
    display-name: "Untrusted"
  neutral:
    minimum: 0
    display-name: "Neutral"
  known:
    minimum: 100
    display-name: "Known"
  respected:
    minimum: 250
    display-name: "Respected"
  honored:
    minimum: 500
    display-name: "Honored"
  legendary:
    minimum: 850
    display-name: "Legendary"

factions:
  northfolk:
    display-name: "Northfolk"
    icon: SPRUCE_LOG
  wardens:
    display-name: "Frontier Wardens"
    icon: SHIELD
  anglers:
    display-name: "Tidebound Anglers"
    icon: FISHING_ROD
    sell-bonus-per-point: 0.0002
    maximum-sell-bonus: 0.15
  scholars:
    display-name: "Veiled Archive"
    icon: ENCHANTED_BOOK
```
:::

:::spoiler fishing.yml
```yaml
#####################################################################
# Note: Plugin is in Early Access - its very experimental right now #
#####################################################################

schema-version: 1

fishing:
  enabled: true
  catch-cooldown-ticks: 20
  base-catch-chance: 0.85
  junk-chance: 0.10
  treasure-chance: 0.03
  base-catch-experience: 6.0
  experience-per-fishing-level: 0.15
  skill-xp-multiplier: 0.75

fishing-skill:
  max-level: 100
  fast-hook-wait-multiplier: 0.75
  catch-chance-per-level: 0.002
  junk-reduction-per-level: 0.001
  rarity-bonus-per-level: 0.003
  sell-price-per-level: 0.01
  fishmonger-price-bonus: 0.05
  enchant-steal-chance: 0.0002
  legendary-fish-chance: 0.002
  mythic-fish-chance: 0.0002
  max-sell-multiplier: 2.0
  double-catch-chance-per-level: 0.001
  max-double-catch-chance: 0.25

rarities:
  common:
    weight: 100.0
    color: GRAY
    price-multiplier: 1.0
    experience-multiplier: 1.0
    weight-multiplier: 1.0
    length-multiplier: 1.0
  uncommon:
    weight: 45.0
    color: GREEN
    price-multiplier: 2.5
    experience-multiplier: 1.5
    weight-multiplier: 1.2
    length-multiplier: 1.1
  rare:
    weight: 18.0
    color: BLUE
    price-multiplier: 6.0
    experience-multiplier: 3.0
    weight-multiplier: 1.5
    length-multiplier: 1.3
  epic:
    weight: 6.0
    color: DARK_PURPLE
    price-multiplier: 15.0
    experience-multiplier: 6.0
    weight-multiplier: 2.0
    length-multiplier: 1.6
  legendary:
    weight: 1.5
    color: GOLD
    price-multiplier: 40.0
    experience-multiplier: 12.0
    weight-multiplier: 3.0
    length-multiplier: 2.0
  mythic:
    weight: 0.3
    color: AQUA
    price-multiplier: 100.0
    experience-multiplier: 25.0
    weight-multiplier: 4.0
    length-multiplier: 2.5

fish:
  trout:
    display-name: "Trout"
    base-cost: 5.0
    base-weight: 1.2
    base-length: 30.0
    icon: COD
    biomes: [RIVER, SWAMP, FOREST, PLAINS]
  salmon:
    display-name: "Salmon"
    base-cost: 8.0
    base-weight: 3.5
    base-length: 50.0
    icon: SALMON
    biomes: [RIVER, OCEAN, BEACH]
  pike:
    display-name: "Pike"
    base-cost: 12.0
    base-weight: 4.0
    base-length: 60.0
    icon: COD
    biomes: [RIVER, SWAMP]
  carp:
    display-name: "Carp"
    base-cost: 4.0
    base-weight: 2.5
    base-length: 40.0
    icon: COD
    biomes: [RIVER, SWAMP]
  perch:
    display-name: "Perch"
    base-cost: 3.5
    base-weight: 0.8
    base-length: 25.0
    icon: COD
    biomes: [RIVER, FOREST, SWAMP]
  catfish:
    display-name: "Catfish"
    base-cost: 10.0
    base-weight: 5.0
    base-length: 70.0
    icon: COD
    biomes: [RIVER, SWAMP]
  cod:
    display-name: "Cod"
    base-cost: 6.0
    base-weight: 3.0
    base-length: 45.0
    icon: COD
    biomes: [OCEAN, BEACH]
  tuna:
    display-name: "Tuna"
    base-cost: 20.0
    base-weight: 15.0
    base-length: 120.0
    icon: SALMON
    biomes: [OCEAN]
  swordfish:
    display-name: "Swordfish"
    base-cost: 35.0
    base-weight: 25.0
    base-length: 200.0
    icon: SALMON
    biomes: [OCEAN]
  mackerel:
    display-name: "Mackerel"
    base-cost: 5.5
    base-weight: 1.0
    base-length: 35.0
    icon: COD
    biomes: [OCEAN, BEACH]
  clownfish:
    display-name: "Clownfish"
    base-cost: 15.0
    base-weight: 0.3
    base-length: 15.0
    icon: TROPICAL_FISH
    biomes: [OCEAN]
  pufferfish:
    display-name: "Pufferfish"
    base-cost: 18.0
    base-weight: 1.5
    base-length: 30.0
    icon: PUFFERFISH
    biomes: [OCEAN]
  anglerfish:
    display-name: "Anglerfish"
    base-cost: 45.0
    base-weight: 8.0
    base-length: 90.0
    icon: COD
    biomes: [OCEAN]
  goldfish:
    display-name: "Golden Koi"
    base-cost: 80.0
    base-weight: 0.5
    base-length: 20.0
    icon: TROPICAL_FISH
    biomes: [RIVER, SWAMP]
  crystal_bass:
    display-name: "Crystal Bass"
    base-cost: 120.0
    base-weight: 2.0
    base-length: 50.0
    icon: COD
    biomes: [OCEAN, RIVER]
  shadow_eel:
    display-name: "Shadow Eel"
    base-cost: 150.0
    base-weight: 3.0
    base-length: 80.0
    icon: SALMON
    biomes: [SWAMP, OCEAN]
  starfish:
    display-name: "Starfin"
    base-cost: 200.0
    base-weight: 1.0
    base-length: 40.0
    icon: TROPICAL_FISH
    biomes: [OCEAN]
  leviathan:
    display-name: "Leviathan Spawn"
    base-cost: 500.0
    base-weight: 50.0
    base-length: 300.0
    icon: SALMON
    biomes: [OCEAN]
  northern_kraken:
    display-name: "Northern Kraken"
    base-cost: 2500.0
    base-weight: 120.0
    base-length: 900.0
    icon: SALMON
    legendary-only: true
    biomes: [OCEAN]
  aurora_dragonfish:
    display-name: "Aurora Dragonfish"
    base-cost: 3200.0
    base-weight: 18.0
    base-length: 180.0
    icon: TROPICAL_FISH
    legendary-only: true
    biomes: [OCEAN, RIVER]
    time: [NIGHT]
  stormglass_herring:
    display-name: "Stormglass Herring"
    base-cost: 1800.0
    base-weight: 4.0
    base-length: 55.0
    icon: COD
    legendary-only: true
    biomes: [OCEAN, DEEP_OCEAN]
    weather: [THUNDER]
  pale_ice_koi:
    display-name: "Pale Ice Koi"
    base-cost: 2200.0
    base-weight: 2.0
    base-length: 48.0
    icon: TROPICAL_FISH
    legendary-only: true
    biomes: [FROZEN_RIVER, FROZEN_OCEAN]
    time: [NIGHT]

junk:
  stick:
    display-name: "Waterlogged Stick"
    base-cost: 0.5
    icon: STICK
  leather:
    display-name: "Soggy Leather"
    base-cost: 1.0
    icon: LEATHER
  bowl:
    display-name: "Old Bowl"
    base-cost: 0.8
    icon: BOWL
  bone:
    display-name: "Fish Bone"
    base-cost: 0.3
    icon: BONE
  lily_pad:
    display-name: "Lily Pad"
    base-cost: 0.2
    icon: LILY_PAD

treasures:
  name_tag:
    display-name: "Engraved Name Tag"
    base-cost: 50.0
    icon: NAME_TAG
  saddle:
    display-name: "Ancient Saddle"
    base-cost: 65.0
    icon: SADDLE
  nautilus_shell:
    display-name: "Pristine Nautilus Shell"
    base-cost: 90.0
    icon: NAUTILUS_SHELL
  heart_of_the_sea:
    display-name: "Heart of the Deep"
    base-cost: 250.0
    icon: HEART_OF_THE_SEA
  enchanted_book:
    display-name: "Waterlogged Tome"
    base-cost: 120.0
    icon: ENCHANTED_BOOK

sell:
  global-multiplier: 1.0
  weight-factor-enabled: true
  weight-factor-exponent: 1.15
  length-factor-enabled: true
  length-factor-exponent: 1.1
  round-decimals: 2
  min-price: 0.01

display:
  lore:
    - "{color}{bold}{rarity} {name}"
    - "{dark_gray}-------------------"
    - "{gray}Weight: {white}{weight} kg"
    - "{gray}Length: {white}{length} cm"
    - "{gray}Rarity: {color}{rarity}"
    - "{gray}Value: {gold}{price}"
    - "{dark_gray}-------------------"
    - "{yellow}Sell with /lotn sellfish"
```
:::

:::spoiler mobs.yml
```yaml
#####################################################################
# Note: Plugin is in Early Access - its very experimental right now #
#####################################################################

schema-version: 10

scaling:
  enabled: true
  health-per-level: 0.028
  damage-per-level: 0.018
  armor-per-level: 0.025

player-selection:
  detection-radius: 48.0
  default-level: 1
  ignore-creative: true
  ignore-spectator: true

levels:
  minimum: 1
  maximum: 80
  roll-within-player-bracket: true

tiers:
  1:
    purpose: COMMON
    stats:
      health-multiplier: 0.90
      damage-multiplier: 0.90
      armor-bonus: 0.0
      speed-multiplier: 1.0
      experience-multiplier: 0.85
      knockback-resistance: 0.0
  2:
    purpose: UNCOMMON
    stats:
      health-multiplier: 1.05
      damage-multiplier: 1.0
      armor-bonus: 1.0
      speed-multiplier: 1.10
      experience-multiplier: 1.1
      knockback-resistance: 0.02
  3:
    purpose: STRONG
    stats:
      health-multiplier: 1.30
      damage-multiplier: 1.15
      armor-bonus: 2.5
      speed-multiplier: 1.04
      experience-multiplier: 1.45
      knockback-resistance: 0.06
  4:
    purpose: ELITE
    stats:
      health-multiplier: 1.75
      damage-multiplier: 1.30
      armor-bonus: 4.0
      speed-multiplier: 1.07
      experience-multiplier: 2.1
      knockback-resistance: 0.12
  5:
    purpose: CHAMPION
    stats:
      health-multiplier: 2.40
      damage-multiplier: 1.50
      armor-bonus: 6.0
      speed-multiplier: 1.10
      experience-multiplier: 3.2
      knockback-resistance: 0.20
  6:
    purpose: LEGENDARY
    stats:
      health-multiplier: 3.25
      damage-multiplier: 1.75
      armor-bonus: 8.0
      speed-multiplier: 1.12
      experience-multiplier: 5.0
      knockback-resistance: 0.30

families:
  zombie:
    group: zombie
    entities: [ZOMBIE, HUSK, ZOMBIE_VILLAGER]
    stats:
      health-multiplier: 1.0
      damage-multiplier: 1.0
      armor-bonus: 0.0
      speed-multiplier: 1.0
      experience-multiplier: 1.0
    variants:
      rotten_corpse:
        display-name: "Rotten Corpse"
        tier: 1
        weights: [120, 95, 70, 45, 28, 16, 8, 3]
      zombie:
        display-name: "Zombie"
        tier: 2
        weights: [75, 85, 82, 70, 55, 42, 30, 18]
      diseased_zombie:
        display-name: "Diseased Zombie"
        tier: 3
        weights: [20, 38, 55, 62, 65, 60, 50, 35]
      plague_walker:
        display-name: "Plague Walker"
        tier: 4
        weights: [3, 10, 20, 35, 48, 60, 65, 65]
      grave_champion:
        display-name: "Grave Champion"
        tier: 5
        weights: [1, 2, 6, 15, 28, 40, 55, 70]
      undying_lord:
        display-name: "Undying Lord"
        tier: 6
        weights: [0, 0, 1, 3, 6, 12, 25, 45]

  skeleton:
    group: skeleton
    entities: [SKELETON, STRAY, BOGGED, WITHER_SKELETON]
    stats:
      health-multiplier: 0.95
      damage-multiplier: 1.05
      armor-bonus: 0.0
      speed-multiplier: 1.0
      experience-multiplier: 1.0
    variants:
      skeleton:
        display-name: "Skeleton"
        tier: 1
        weights: [120, 95, 70, 48, 30, 18, 10, 4]
      archer_skeleton:
        display-name: "Archer Skeleton"
        tier: 2
        weights: [70, 82, 80, 68, 55, 45, 32, 20]
      bone_hunter:
        display-name: "Bone Hunter"
        tier: 3
        weights: [18, 35, 52, 60, 64, 60, 54, 40]
      bone_captain:
        display-name: "Bone Captain"
        tier: 4
        weights: [3, 10, 20, 35, 46, 58, 65, 68]
      bone_warden:
        display-name: "Bone Warden"
        tier: 5
        weights: [1, 3, 8, 16, 28, 40, 52, 65]
      bone_overlord:
        display-name: "Bone Overlord"
        tier: 6
        weights: [0, 0, 1, 2, 5, 10, 22, 42]

  spider:
    group: spider
    entities: [SPIDER, CAVE_SPIDER]
    stats:
      health-multiplier: 0.90
      damage-multiplier: 1.0
      armor-bonus: 0.0
      speed-multiplier: 1.06
      experience-multiplier: 1.0
    variants:
      spider:
        display-name: "Spider"
        tier: 1
        weights: [125, 100, 75, 50, 30, 20, 12, 6]
      venom_spider:
        display-name: "Venom Spider"
        tier: 2
        weights: [55, 70, 72, 68, 60, 50, 42, 30]
      frost_spider:
        display-name: "Frost Spider"
        tier: 3
        weights: [12, 22, 40, 52, 58, 62, 60, 54]
      widow_spider:
        display-name: "Widow Spider"
        tier: 4
        weights: [2, 5, 15, 28, 40, 50, 60, 68]
      broodmother:
        display-name: "Broodmother"
        tier: 5
        weights: [1, 2, 5, 10, 18, 30, 42, 55]
      ancient_broodmother:
        display-name: "Ancient Broodmother"
        tier: 6
        weights: [0, 0, 1, 2, 4, 8, 18, 35]

  creeper:
    group: creeper
    entities: [CREEPER]
    stats:
      health-multiplier: 1.0
      damage-multiplier: 1.0
      armor-bonus: 0.0
      speed-multiplier: 1.0
      experience-multiplier: 1.0
    variants:
      creeper:
        display-name: "Creeper"
        tier: 1
        weights: [120, 95, 70, 50, 35, 22, 12, 6]
      swift_creeper:
        display-name: "Swift Creeper"
        tier: 2
        weights: [55, 68, 70, 68, 60, 52, 42, 32]
      armored_creeper:
        display-name: "Armored Creeper"
        tier: 3
        weights: [15, 28, 42, 52, 58, 60, 58, 50]
      toxic_creeper:
        display-name: "Toxic Creeper"
        tier: 4
        weights: [3, 8, 18, 30, 42, 55, 62, 68]
      infernal_creeper:
        display-name: "Infernal Creeper"
        tier: 5
        weights: [1, 2, 6, 12, 22, 35, 48, 60]
      ancient_creeper:
        display-name: "Ancient Creeper"
        tier: 6
        weights: [0, 0, 1, 2, 5, 10, 20, 40]

  drowned:
    group: drowned
    entities: [DROWNED]
    stats:
      health-multiplier: 1.05
      damage-multiplier: 1.0
      armor-bonus: 0.0
      speed-multiplier: 1.0
      experience-multiplier: 1.05
    variants:
      drowned:
        display-name: "Drowned"
        tier: 1
        weights: [120, 95, 70, 45, 28, 16, 8, 3]
      sea_walker:
        display-name: "Sea Walker"
        tier: 2
        weights: [75, 85, 82, 70, 55, 42, 30, 18]
      deep_stalker:
        display-name: "Deep Stalker"
        tier: 3
        weights: [20, 38, 55, 62, 65, 60, 50, 35]
      abyss_hunter:
        display-name: "Abyss Hunter"
        tier: 4
        weights: [3, 10, 20, 35, 48, 60, 65, 65]
      abyss_guardian:
        display-name: "Abyss Guardian"
        tier: 5
        weights: [1, 2, 6, 15, 28, 40, 55, 70]
      leviathans_servant:
        display-name: "Leviathan's Servant"
        tier: 6
        weights: [0, 0, 1, 3, 6, 12, 25, 45]

  phantom:
    group: phantom
    entities: [PHANTOM]
    stats:
      health-multiplier: 0.95
      damage-multiplier: 1.05
      armor-bonus: 0.0
      speed-multiplier: 1.08
      experience-multiplier: 1.1
    variants:
      phantom:
        display-name: "Phantom"
        tier: 1
        weights: [125, 100, 75, 50, 30, 20, 12, 6]
      night_phantom:
        display-name: "Night Phantom"
        tier: 2
        weights: [55, 70, 72, 68, 60, 50, 42, 30]
      shadow_phantom:
        display-name: "Shadow Phantom"
        tier: 3
        weights: [12, 22, 40, 52, 58, 62, 60, 54]
      soul_phantom:
        display-name: "Soul Phantom"
        tier: 4
        weights: [2, 5, 15, 28, 40, 50, 60, 68]
      nightmare:
        display-name: "Nightmare"
        tier: 5
        weights: [1, 2, 5, 10, 18, 30, 42, 55]
      ancient_nightmare:
        display-name: "Ancient Nightmare"
        tier: 6
        weights: [0, 0, 1, 2, 4, 8, 18, 35]

  piglin:
    group: piglin
    entities: [PIGLIN, PIGLIN_BRUTE, ZOMBIFIED_PIGLIN]
    stats:
      health-multiplier: 1.05
      damage-multiplier: 1.08
      armor-bonus: 1.0
      speed-multiplier: 1.0
      experience-multiplier: 1.1
    variants:
      piglin:
        display-name: "Piglin"
        tier: 1
        weights: [120, 95, 70, 48, 30, 18, 10, 4]
      piglin_raider:
        display-name: "Piglin Raider"
        tier: 2
        weights: [70, 82, 80, 68, 55, 45, 32, 20]
      piglin_warrior:
        display-name: "Piglin Warrior"
        tier: 3
        weights: [18, 35, 52, 60, 64, 60, 54, 40]
      piglin_champion:
        display-name: "Piglin Champion"
        tier: 4
        weights: [3, 10, 20, 35, 46, 58, 65, 68]
      piglin_warlord:
        display-name: "Piglin Warlord"
        tier: 5
        weights: [1, 3, 8, 16, 28, 40, 52, 65]
      piglin_king:
        display-name: "Piglin King"
        tier: 6
        weights: [0, 0, 1, 2, 5, 10, 22, 42]

  blaze:
    group: nether
    entities: [BLAZE]
    bracket-shift: -1
    stats:
      health-multiplier: 1.1
      damage-multiplier: 1.1
      armor-bonus: 1.0
      speed-multiplier: 1.0
      experience-multiplier: 1.2
    variants:
      blaze:
        display-name: "Blaze"
        tier: 1
        weights: [120, 95, 70, 48, 30, 18, 10, 4]
      infernal_blaze:
        display-name: "Infernal Blaze"
        tier: 2
        weights: [70, 82, 80, 68, 55, 45, 32, 20]
      ember_mage:
        display-name: "Ember Mage"
        tier: 3
        weights: [18, 35, 52, 60, 64, 60, 54, 40]
      hellfire_sentinel:
        display-name: "Hellfire Sentinel"
        tier: 4
        weights: [3, 10, 20, 35, 46, 58, 65, 68]
      flame_tyrant:
        display-name: "Flame Tyrant"
        tier: 5
        weights: [1, 3, 8, 16, 28, 40, 52, 65]
      phoenix_herald:
        display-name: "Phoenix Herald"
        tier: 6
        weights: [0, 0, 1, 2, 5, 10, 22, 42]

  pillager:
    group: pillager
    entities: [PILLAGER]
    variants:
      pillager:
        display-name: "Pillager"
        tier: 1
        weights: [100, 100, 100, 100, 100, 100, 100, 100]
  vindicator:
    group: vindicator
    entities: [VINDICATOR]
    variants:
      vindicator:
        display-name: "Vindicator"
        tier: 1
        weights: [100, 100, 100, 100, 100, 100, 100, 100]
  evoker:
    group: evoker
    entities: [EVOKER]
    variants:
      evoker:
        display-name: "Evoker"
        tier: 1
        weights: [100, 100, 100, 100, 100, 100, 100, 100]
  magma_cube:
    group: nether
    entities: [MAGMA_CUBE]
    stats:
      health-multiplier: 1.1
      damage-multiplier: 1.05
      experience-multiplier: 1.1
    variants:
      magma_cube:
        display-name: "Magma Cube"
        tier: 1
        weights: [100, 100, 100, 100, 100, 100, 100, 100]
  enderman:
    group: end
    entities: [ENDERMAN]
    stats:
      health-multiplier: 1.15
      damage-multiplier: 1.1
      experience-multiplier: 1.15
    variants:
      enderman:
        display-name: "Enderman"
        tier: 1
        weights: [100, 100, 100, 100, 100, 100, 100, 100]
  shulker:
    group: end
    entities: [SHULKER]
    variants:
      shulker:
        display-name: "Shulker"
        tier: 1
        weights: [100, 100, 100, 100, 100, 100, 100, 100]
  endermite:
    group: end
    entities: [ENDERMITE]
    variants:
      endermite:
        display-name: "Endermite"
        tier: 1
        weights: [100, 100, 100, 100, 100, 100, 100, 100]

  witch:
    group: witch
    entities: [WITCH]
    variants:
      witch:
        display-name: "Witch"
        tier: 1
        weights: [100, 100, 100, 100, 100, 100, 100, 100]
  slime:
    group: slime
    entities: [SLIME]
    variants:
      slime:
        display-name: "Slime"
        tier: 1
        weights: [100, 100, 100, 100, 100, 100, 100, 100]
  silverfish:
    group: silverfish
    entities: [SILVERFISH]
    variants:
      silverfish:
        display-name: "Silverfish"
        tier: 1
        weights: [100, 100, 100, 100, 100, 100, 100, 100]
  guardian:
    group: guardian
    entities: [GUARDIAN]
    variants:
      guardian:
        display-name: "Guardian"
        tier: 1
        weights: [100, 100, 100, 100, 100, 100, 100, 100]
  ghast:
    group: nether
    entities: [GHAST]
    variants:
      ghast:
        display-name: "Ghast"
        tier: 1
        weights: [100, 100, 100, 100, 100, 100, 100, 100]
  hoglin:
    group: nether
    entities: [HOGLIN]
    variants:
      hoglin:
        display-name: "Hoglin"
        tier: 1
        weights: [100, 100, 100, 100, 100, 100, 100, 100]
  zoglin:
    group: nether
    entities: [ZOGLIN]
    variants:
      zoglin:
        display-name: "Zoglin"
        tier: 1
        weights: [100, 100, 100, 100, 100, 100, 100, 100]
  ravager:
    group: pillager
    entities: [RAVAGER]
    variants:
      ravager:
        display-name: "Ravager"
        tier: 1
        weights: [100, 100, 100, 100, 100, 100, 100, 100]
  vex:
    group: evoker
    entities: [VEX]
    variants:
      vex:
        display-name: "Vex"
        tier: 1
        weights: [100, 100, 100, 100, 100, 100, 100, 100]
  breeze:
    group: trial
    entities: [BREEZE]
    variants:
      breeze:
        display-name: "Breeze"
        tier: 1
        weights: [100, 100, 100, 100, 100, 100, 100, 100]
  creaking:
    group: woodland
    entities: [CREAKING]
    variants:
      creaking:
        display-name: "Creaking"
        tier: 1
        weights: [100, 100, 100, 100, 100, 100, 100, 100]

hologram:
  enabled: true
  show-on-hostile-mobs: true
  show-on-passive-mobs: true
  show-on-neutral-mobs: true
  show-on-bosses: true
  suppress-native-nameplate: true
  visibility-range: 32.0
  visibility:
    poll-interval-ticks: 1
    look-enabled: true
    look-range: 8.0
    ray-size: 0.15
    look-retain-ms: 2000
    combat-enabled: true
    combat-retain-ms: 8000
    minimum-view-distance: 0.75
    hide-when-camera-inside: true
  show-level: true
  show-health: true
  level-generation:
    minimum: 1
    maximum: 80
    default-level: 1
    nearest-player-enabled: true
    player-level-influence: 0.35
    random-spread: 2
    world-environment-base:
      normal: 1
      nether: 20
      the_end: 35
      custom: 1
  format:
    name-line: "&c{name} &8• &7Lv. &f{level}"
    name-only-line: "&c{name}"
  health-bar:
    segments: 10
    left: ""
    filled: "&a&m "
    missing: "&c&m "
    right: ""
  style:
    billboard: VERTICAL
    vertical-offset: 0.35
    scale: 0.8
    see-through: false
    shadowed: true
    line-width: 160
    display-width: 2.5
    display-height: 1.0
    view-range: 1.0
    shadow-radius: 0.0
    shadow-strength: 0.0
    background:
      alpha: 0
      red: 15
      green: 15
      blue: 18

armor:
  enabled: true
  minimum-tier: 4
  default:
    helmet: CHAINMAIL_HELMET
    chestplate: CHAINMAIL_CHESTPLATE
    leggings: CHAINMAIL_LEGGINGS
    boots: CHAINMAIL_BOOTS

equipment-profiles:
  tier-1: {}
  tier-2: {}
  tier-3: {}
  tier-4:
    helmet: CHAINMAIL_HELMET
    chestplate: CHAINMAIL_CHESTPLATE
    leggings: CHAINMAIL_LEGGINGS
    boots: CHAINMAIL_BOOTS
  tier-5:
    helmet: IRON_HELMET
    chestplate: IRON_CHESTPLATE
    leggings: IRON_LEGGINGS
    boots: IRON_BOOTS
  tier-6:
    helmet: DIAMOND_HELMET
    chestplate: DIAMOND_CHESTPLATE
    leggings: DIAMOND_LEGGINGS
    boots: DIAMOND_BOOTS

display:
  show-mob-level: true
  always-visible: false

rewards:
  base-kill-experience: 8.0
  experience-per-mob-level: 1.2
  farmed-spawn-multiplier: 0.15
  farmed-spawns-count-for-quests: false
  rank-multipliers:
    normal: 1.0
    common: 1.0
    uncommon: 1.1
    strong: 1.35
    elite: 2.25
    champion: 4.0
    legendary: 6.0
    boss: 8.0
```
:::

:::spoiler quests.yml
```yaml
#####################################################################
# Note: Plugin is in Early Access - its very experimental right now #
#####################################################################

schema-version: 4

quests:
  main_ender_dragon:
    enabled: true
    display-name: "Main Quest: Kill the Ender Dragon"
    icon: DRAGON_HEAD
    category: main
    description:
      - "Find the End portal and kill the Ender Dragon."
    objectives:
      defeat_dragon:
        type: KILL
        target: ENDER_DRAGON
        amount: 1
        description: "Kill the Ender Dragon"
    rewards:
      experience: 5000
      skill-xp:
        one_handed: 100
        two_handed: 100
        archery: 100
      reputation:
        wardens: 150
        northfolk: 150

  radiant_hostile_hunt:
    enabled: true
    display-name: "Monster Hunt"
    icon: IRON_SWORD
    category: repeatable
    repeatable: true
    cooldown-seconds: 0
    description:
      - "Kill hostile mobs."
    objectives:
      hunt:
        type: KILL
        target: HOSTILE
        amount: 12
        description: "Kill hostile mobs"
    rewards:
      experience: 70
      skill-xp:
        one_handed: 12

  radiant_zombie_hunt:
    enabled: true
    display-name: "Zombie Hunt"
    icon: ROTTEN_FLESH
    category: repeatable
    repeatable: true
    cooldown-seconds: 0
    description:
      - "Kill zombies."
    objectives:
      zombies:
        type: KILL
        target: ZOMBIE
        amount: 10
        description: "Kill zombies"
    rewards:
      experience: 65
      skill-xp:
        one_handed: 10

  radiant_skeleton_hunt:
    enabled: true
    display-name: "Skeleton Hunt"
    icon: BONE
    category: repeatable
    repeatable: true
    cooldown-seconds: 0
    description:
      - "Kill skeletons."
    objectives:
      skeletons:
        type: KILL
        target: SKELETON
        amount: 10
        description: "Kill skeletons"
    rewards:
      experience: 65
      skill-xp:
        archery: 10

  radiant_creeper_hunt:
    enabled: true
    display-name: "Creeper Hunt"
    icon: GUNPOWDER
    category: repeatable
    repeatable: true
    cooldown-seconds: 0
    description:
      - "Kill creepers."
    objectives:
      creepers:
        type: KILL
        target: CREEPER
        amount: 6
        description: "Kill creepers"
    rewards:
      experience: 75
      skill-xp:
        archery: 12

  radiant_spider_hunt:
    enabled: true
    display-name: "Spider Hunt"
    icon: SPIDER_EYE
    category: repeatable
    repeatable: true
    cooldown-seconds: 0
    description:
      - "Kill spiders and cave spiders."
    objectives:
      spiders:
        type: KILL
        target: "SPIDER|CAVE_SPIDER"
        amount: 10
        description: "Kill spiders"
    rewards:
      experience: 65
      skill-xp:
        two_handed: 10

  radiant_blaze_hunt:
    enabled: true
    display-name: "Blaze Hunt"
    icon: BLAZE_ROD
    category: repeatable
    repeatable: true
    cooldown-seconds: 0
    description:
      - "Kill blazes in the Nether."
    objectives:
      blazes:
        type: KILL
        target: BLAZE
        amount: 6
        description: "Kill blazes"
    rewards:
      experience: 110
      skill-xp:
        two_handed: 15

  radiant_iron_mining:
    enabled: true
    display-name: "Mine Iron"
    icon: RAW_IRON
    category: repeatable
    repeatable: true
    cooldown-seconds: 0
    description:
      - "Mine iron ore."
    objectives:
      iron:
        type: MINE
        target: "IRON_ORE|DEEPSLATE_IRON_ORE"
        amount: 16
        description: "Mine iron ore"
    rewards:
      experience: 65
      skill-xp:
        mining: 18

  radiant_coal_mining:
    enabled: true
    display-name: "Mine Coal"
    icon: COAL
    category: repeatable
    repeatable: true
    cooldown-seconds: 0
    description:
      - "Mine coal ore."
    objectives:
      coal:
        type: MINE
        target: "COAL_ORE|DEEPSLATE_COAL_ORE"
        amount: 20
        description: "Mine coal ore"
    rewards:
      experience: 55
      skill-xp:
        mining: 15

  radiant_redstone_mining:
    enabled: true
    display-name: "Mine Redstone"
    icon: REDSTONE
    category: repeatable
    repeatable: true
    cooldown-seconds: 0
    description:
      - "Mine redstone ore."
    objectives:
      redstone:
        type: MINE
        target: "REDSTONE_ORE|DEEPSLATE_REDSTONE_ORE"
        amount: 14
        description: "Mine redstone ore"
    rewards:
      experience: 80
      skill-xp:
        mining: 20

  radiant_lumber:
    enabled: true
    display-name: "Chop Wood"
    icon: IRON_AXE
    category: repeatable
    repeatable: true
    cooldown-seconds: 0
    description:
      - "Chop logs."
    objectives:
      logs:
        type: BREAK
        target: LOGS
        amount: 24
        description: "Chop logs"
    rewards:
      experience: 55
      skill-xp:
        woodcutting: 18

  radiant_harvest:
    enabled: true
    display-name: "Harvest Crops"
    icon: WHEAT
    category: repeatable
    repeatable: true
    cooldown-seconds: 0
    description:
      - "Harvest crops."
    objectives:
      crops:
        type: HARVEST
        target: FARM_PRODUCE
        amount: 24
        description: "Harvest crops"
    rewards:
      experience: 55
      skill-xp:
        farming: 18

  radiant_planting:
    enabled: true
    display-name: "Plant Crops"
    icon: WHEAT_SEEDS
    category: repeatable
    repeatable: true
    cooldown-seconds: 0
    description:
      - "Plant crops."
    objectives:
      crops:
        type: PLANT
        target: CROPS
        amount: 24
        description: "Plant crops"
    rewards:
      experience: 45
      skill-xp:
        farming: 15

  radiant_fishing:
    enabled: true
    display-name: "Catch Fish"
    icon: FISHING_ROD
    category: repeatable
    repeatable: true
    cooldown-seconds: 0
    description:
      - "Catch fish."
    objectives:
      catches:
        type: FISH
        target: ANY
        amount: 6
        description: "Catch fish"
    rewards:
      experience: 65
      skill-xp:
        fishing: 18

  radiant_smelting:
    enabled: true
    display-name: "Smelt Iron"
    icon: FURNACE
    category: repeatable
    repeatable: true
    cooldown-seconds: 0
    description:
      - "Smelt iron ingots."
    objectives:
      ingots:
        type: SMELT
        target: IRON_INGOT
        amount: 16
        description: "Smelt iron ingots"
    rewards:
      experience: 60
      skill-xp:
        smithing: 18

  radiant_weapon_crafting:
    enabled: true
    display-name: "Craft Weapons"
    icon: ANVIL
    category: repeatable
    repeatable: true
    cooldown-seconds: 0
    description:
      - "Craft weapons."
    objectives:
      weapons:
        type: CRAFT
        target: WEAPON
        amount: 3
        description: "Craft weapons"
    rewards:
      experience: 65
      skill-xp:
        smithing: 20
```
:::

:::spoiler scoreboard.yml
```yaml
#####################################################################
# Note: Plugin is in Early Access - its very experimental right now #
#####################################################################

schema-version: 11
enabled: true
update-interval-ticks: 20
title: "&m         &l&cLOTN&r&m         "

quest-bar:
  enabled: true
  color: YELLOW
  style: SEGMENTED_10
  update-interval-ticks: 10
  title-format: "&f{quest} &8• &7{objective}"

# Character: {level}, {level_progress}, {health}, {max_health},
# {stamina}, {max_stamina}, {magicka}, {max_magicka}
# Equipment: {armor_rating}
# World: {biome}, {location}, {month}, {day}, {time}
# Survival: {temperature}, {temp_c}, {temp_f}, {weight},
# {carry_weight}, {max_weight}
lines:
  - "&7&l[ Character ]"
  - "&f{character_name}"
  - "&8Lv. &6{level}"
  - "&7Armor: &f{armor_rating}"
  - ""
  - "&7&l[ World ]"
  - "&b{month} {day}"
  - "&a{temperature}"
  - ""
  - "&7&l[ Inventory ]"
  - "&e{balance} Gold"
  - "&f{weight}"
  - "&m                        "
```
:::

:::spoiler skills.yml
```yaml
#####################################################################
# Note: Plugin is in Early Access - its very experimental right now #
#####################################################################

schema-version: 7
debug: false
progression:
  default-level: 15
  max-level: 100
  xp-curve:
    base-xp: 75.0
    exponent: 1.65
  maximum-single-xp-gain: 10000.0
  show-xp-gains: false

messages:
  skill-level-up: "&aLotN: &6{skill} &areached level {level}."
  skill-xp-gain: "&7LotN: +{amount} {skill} XP ({source})."
  mastered: "Mastered"
  perk-purchased: "&aLotN: Upgraded &6{perk}&a."
  perk-max-rank: "&eLotN: {perk} is already fully upgraded."
  perk-skill-required: "&cLotN: Your skill level is too low for the next rank."
  perk-prerequisite-required: "&cLotN: Unlock the prerequisite perk first."
  perk-not-enough-points: "&cLotN: You do not have enough perk points."
  perk-unknown: "&cLotN: That perk is no longer configured."
  perk-disabled: "&cLotN: {perk} is currently disabled."
  perk-mutually-exclusive: "&cLotN: A mutually exclusive perk is already purchased."
  perk-cancelled: "&eLotN: That perk purchase was cancelled."
  perks-skill-unlocked: "&eNew skill-unlocked perks: &6{perks}&e.{points_note}"

anti-exploit:
  allow-pvp-xp: false
  allow-friendly-targets: false
  allow-plugin-spawned-targets: false
  allow-environmental-armor-xp: false
  allow-dispenser-block-xp: false
  diminishing:
    enabled: true
    window-millis: 30000
    same-entity-full-xp-hits: 6
    same-type-full-xp-hits: 30
    same-entity-reduction-per-hit: 0.12
    same-type-reduction-per-hit: 0.015
    minimum-multiplier: 0.15

xp-multipliers:
  one_handed: 1.0
  archery: 1.0
  block: 1.0
  light_armor: 1.0
  heavy_armor: 1.0
  sneak: 1.0
  smithing: 1.0

progress-feedback:
  enabled: true
  threshold-percent: 25
  hold-millis: 2500

activity:
  tick-interval-ticks: 100
  afk-after-seconds: 120
  minimum-movement-distance: 0.20

armor-familiarity:
  enabled: true
  xp-per-block: 0.01
  maximum-per-tick: 0.25
  session-cap: 25.0

skill-definitions:
  one_handed:
    display-name: "One-Handed"
    icon: IRON_SWORD
    description: "Deal real damage with swords and other configured one-handed weapons."
    category: combat
    max-level: 100
    player-level-weight: 1.0
  two_handed:
    display-name: "Two-Handed"
    icon: IRON_AXE
    description: "Deal real damage with axes, maces, tridents, and configured heavy weapons."
    category: combat
    max-level: 100
    player-level-weight: 1.0
  archery:
    display-name: "Archery"
    icon: BOW
    description: "Damage valid enemies with bows and crossbows."
    category: combat
    max-level: 100
    player-level-weight: 1.0
  block:
    display-name: "Block"
    icon: SHIELD
    description: "Prevent incoming combat damage with a raised shield."
    category: combat
    max-level: 100
    player-level-weight: 1.0
  heavy_armor:
    display-name: "Heavy Armor"
    icon: IRON_CHESTPLATE
    description: "Survive combat while wearing heavy armor."
    category: protection
    max-level: 100
    player-level-weight: 0.95
  light_armor:
    display-name: "Light Armor"
    icon: LEATHER_CHESTPLATE
    description: "Survive combat while wearing light armor."
    category: protection
    max-level: 100
    player-level-weight: 0.95
  sneak:
    display-name: "Sneak"
    icon: LEATHER_BOOTS
    description: "Land valid attacks while sneaking."
    category: protection
    max-level: 100
    player-level-weight: 0.75
  mining:
    display-name: "Mining"
    icon: IRON_PICKAXE
    description: "Extract naturally generated ores."
    category: professions
    max-level: 100
    player-level-weight: 0.85
  woodcutting:
    display-name: "Woodcutting"
    icon: IRON_AXE
    description: "Harvest naturally generated logs."
    category: professions
    max-level: 100
    player-level-weight: 0.75
  fishing:
    display-name: "Fishing"
    icon: FISHING_ROD
    description: "Catch fish, treasure, and legendary northern creatures."
    category: professions
    max-level: 100
    player-level-weight: 0.9
  alchemy:
    display-name: "Alchemy"
    icon: BREWING_STAND
    description: "Study ingredients and brew legitimate LOTN mixtures."
    category: crafting
    max-level: 100
    player-level-weight: 0.85
  enchanting:
    display-name: "Enchanting"
    icon: ENCHANTED_BOOK
    description: "Learn and apply LOTN enchantments."
    category: crafting
    max-level: 100
    player-level-weight: 0.9
  smithing:
    display-name: "Smithing"
    icon: ANVIL
    description: "Craft equipment and extract smelted materials."
    category: crafting
    max-level: 100
    player-level-weight: 0.85
  farming:
    display-name: "Farming"
    icon: WHEAT
    description: "Harvest mature crops."
    category: professions
    max-level: 100
    player-level-weight: 0.7

perk-trees:
  archery:
    steady_aim:
      display-name: "Steady Aim"
      icon: BOW
      gui-slot: 13
      legacy-ids: [arch_steady_aim]
      description:
        - "Increases bow and crossbow damage."
      ranks:
        1: {required-skill-level: 20, cost: 1, effects: {damage-percent: 5.0}}
        2: {required-skill-level: 40, cost: 1, effects: {damage-percent: 10.0}}
        3: {required-skill-level: 60, cost: 1, effects: {damage-percent: 15.0}}
        4: {required-skill-level: 80, cost: 1, effects: {damage-percent: 20.0}}
        5: {required-skill-level: 100, cost: 1, effects: {damage-percent: 25.0}}
    eagle_eye:
      display-name: "Eagle Eye"
      icon: SPYGLASS
      gui-slot: 20
      prerequisite: steady_aim
      legacy-ids: [arch_eagle_eye]
      description:
        - "Reduces projectile spread by aligning shots more closely"
        - "with the direction of the player's aim."
      ranks:
        1: {required-skill-level: 30, cost: 1, effects: {accuracy-percent: 20.0}}
        2: {required-skill-level: 60, cost: 1, effects: {accuracy-percent: 35.0}}
        3: {required-skill-level: 90, cost: 1, effects: {accuracy-percent: 50.0}}
    hunters_draw:
      display-name: "Hunter's Draw"
      icon: ARROW
      gui-slot: 24
      prerequisite: steady_aim
      legacy-ids: [arch_quick_nock]
      description:
        - "Increases projectile velocity as a reliable alternative"
        - "to client-side bow draw-time modification. (EA: INFO)"
      ranks:
        1: {required-skill-level: 35, cost: 1, effects: {projectile-velocity-percent: 5.0}}
        2: {required-skill-level: 70, cost: 1, effects: {projectile-velocity-percent: 10.0}}
    piercing_shot:
      display-name: "Piercing Shot"
      icon: POINTED_DRIPSTONE
      gui-slot: 29
      prerequisite: eagle_eye
      legacy-ids: [arch_piercing_shot]
      description:
        - "Grants a chance for ranged attacks to ignore part"
        - "of the target's armor."
      ranks:
        1: {required-skill-level: 50, cost: 1, effects: {chance: 8.0, armor-ignore-percent: 15.0}}
        2: {required-skill-level: 75, cost: 1, effects: {chance: 12.0, armor-ignore-percent: 22.0}}
        3: {required-skill-level: 100, cost: 1, effects: {chance: 18.0, armor-ignore-percent: 30.0}}

  block:
    deflection:
      display-name: "Deflection"
      icon: SHIELD
      gui-slot: 13
      legacy-ids: [blk_shield_wall]
      description:
        - "Increases damage prevented while actively blocking."
      ranks:
        1: {required-skill-level: 20, cost: 1, effects: {additional-block-percent: 5.0}}
        2: {required-skill-level: 40, cost: 1, effects: {additional-block-percent: 10.0}}
        3: {required-skill-level: 60, cost: 1, effects: {additional-block-percent: 15.0}}
        4: {required-skill-level: 80, cost: 1, effects: {additional-block-percent: 20.0}}
        5: {required-skill-level: 100, cost: 1, effects: {additional-block-percent: 25.0}}
    steadfast:
      display-name: "Steadfast"
      icon: IRON_INGOT
      gui-slot: 20
      prerequisite: deflection
      legacy-ids: [blk_deflection]
      description:
        - "Reduces shield-disable duration after a successful block."
      ranks:
        1: {required-skill-level: 35, cost: 1, effects: {shield-disable-reduction-percent: 20.0}}
        2: {required-skill-level: 70, cost: 1, effects: {shield-disable-reduction-percent: 40.0}}
    counterguard:
      display-name: "Counterguard"
      icon: IRON_SWORD
      gui-slot: 24
      prerequisite: deflection
      legacy-ids: [blk_counter_strike]
      description:
        - "Successful blocks may briefly stagger the attacker."
      ranks:
        1: {required-skill-level: 45, cost: 1, effects: {chance: 8.0, duration-ticks: 12, cooldown-ticks: 80}}
        2: {required-skill-level: 75, cost: 1, effects: {chance: 13.0, duration-ticks: 16, cooldown-ticks: 70}}
        3: {required-skill-level: 100, cost: 1, effects: {chance: 18.0, duration-ticks: 20, cooldown-ticks: 60}}
    last_bastion:
      display-name: "Last Bastion"
      icon: OBSIDIAN
      gui-slot: 31
      prerequisite: steadfast
      legacy-ids: [blk_fortress, blk_unbreakable]
      description:
        - "At low health, blocking becomes more effective."
      ranks:
        1: {required-skill-level: 65, cost: 1, effects: {health-threshold-percent: 30.0, additional-block-percent: 10.0, cooldown-ticks: 200}}
        2: {required-skill-level: 100, cost: 1, effects: {health-threshold-percent: 35.0, additional-block-percent: 18.0, cooldown-ticks: 160}}

  one_handed:
    armsman:
      display-name: "Armsman"
      icon: IRON_SWORD
      gui-slot: 13
      legacy-ids: [oh_blade_training]
      description: ["Increases damage with eligible one-handed weapons."]
      ranks:
        1: {required-skill-level: 20, cost: 1, effects: {damage-percent: 4.0}}
        2: {required-skill-level: 40, cost: 1, effects: {damage-percent: 8.0}}
        3: {required-skill-level: 60, cost: 1, effects: {damage-percent: 12.0}}
        4: {required-skill-level: 80, cost: 1, effects: {damage-percent: 16.0}}
        5: {required-skill-level: 100, cost: 1, effects: {damage-percent: 20.0}}
    quick_strikes:
      display-name: "Quick Strikes"
      icon: GOLDEN_SWORD
      gui-slot: 20
      prerequisite: armsman
      legacy-ids: [oh_quick_reflexes]
      description: ["Improves attack-speed handling (EA: server API needs to support it)"]
      ranks:
        1: {required-skill-level: 35, cost: 1, effects: {attack-speed-percent: 4.0}}
        2: {required-skill-level: 70, cost: 1, effects: {attack-speed-percent: 8.0}}
    bleeding_edge:
      display-name: "Bleeding Edge"
      icon: REDSTONE
      gui-slot: 24
      prerequisite: armsman
      legacy-ids: [oh_iron_grip]
      description: ["Sword attacks may apply a short bleeding effect."]
      ranks:
        1: {required-skill-level: 45, cost: 1, effects: {chance: 6.0, duration-ticks: 40, damage-per-tick: 0.75}}
        2: {required-skill-level: 75, cost: 1, effects: {chance: 10.0, duration-ticks: 60, damage-per-tick: 1.0}}
        3: {required-skill-level: 100, cost: 1, effects: {chance: 14.0, duration-ticks: 80, damage-per-tick: 1.25}}
    crushing_blows:
      display-name: "Crushing Blows"
      icon: IRON_AXE
      gui-slot: 31
      prerequisite: bleeding_edge
      legacy-ids: [oh_flurry, oh_bladestorm]
      description: ["Configured one-handed axes may partially ignore armor."]
      ranks:
        1: {required-skill-level: 65, cost: 1, effects: {chance: 8.0, armor-ignore-percent: 12.0}}
        2: {required-skill-level: 100, cost: 1, effects: {chance: 14.0, armor-ignore-percent: 20.0}}

  two_handed:
    barbarian:
      display-name: "Barbarian"
      icon: IRON_AXE
      gui-slot: 13
      legacy-ids: [th_power_strike]
      description: ["Increases damage with eligible two-handed weapons."]
      ranks:
        1: {required-skill-level: 20, cost: 1, effects: {damage-percent: 5.0}}
        2: {required-skill-level: 40, cost: 1, effects: {damage-percent: 10.0}}
        3: {required-skill-level: 60, cost: 1, effects: {damage-percent: 15.0}}
        4: {required-skill-level: 80, cost: 1, effects: {damage-percent: 20.0}}
        5: {required-skill-level: 100, cost: 1, effects: {damage-percent: 25.0}}
    heavy_impact:
      display-name: "Heavy Impact"
      icon: MACE
      gui-slot: 20
      prerequisite: barbarian
      legacy-ids: [th_crushing_blow]
      description: ["Fully charged heavy attacks may stagger enemies."]
      ranks:
        1: {required-skill-level: 40, cost: 1, effects: {chance: 8.0, duration-ticks: 10}}
        2: {required-skill-level: 70, cost: 1, effects: {chance: 14.0, duration-ticks: 15}}
        3: {required-skill-level: 100, cost: 1, effects: {chance: 20.0, duration-ticks: 20}}
    sweeping_force:
      display-name: "Sweeping Force"
      icon: NETHERITE_AXE
      gui-slot: 29
      prerequisite: heavy_impact
      legacy-ids: [th_sweep_attack]
      description: ["Fully charged attacks deal limited nearby damage on a cooldown."]
      ranks:
        1: {required-skill-level: 60, cost: 1, effects: {radius: 2.5, damage-percent: 20.0, cooldown-ticks: 100}}
        2: {required-skill-level: 100, cost: 1, effects: {radius: 3.0, damage-percent: 30.0, cooldown-ticks: 80}}

  heavy_armor:
    iron_skin:
      display-name: "Iron Skin"
      icon: IRON_CHESTPLATE
      gui-slot: 13
      legacy-ids: [ha_iron_skin]
      description:
        - "Improves heavy armor effectiveness and carry capacity."
      ranks:
        1: {required-skill-level: 20, cost: 1, effects: {armor-percent: 2.2, carry-capacity: 10.0}}
        2: {required-skill-level: 40, cost: 1, effects: {armor-percent: 4.4, carry-capacity: 20.0}}
        3: {required-skill-level: 60, cost: 1, effects: {armor-percent: 6.6, carry-capacity: 30.0}}
        4: {required-skill-level: 80, cost: 1, effects: {armor-percent: 8.8, carry-capacity: 40.0}}
        5: {required-skill-level: 100, cost: 1, effects: {armor-percent: 11.0, carry-capacity: 50.0}}
    unshaken:
      display-name: "Unshaken"
      icon: NETHERITE_INGOT
      gui-slot: 20
      prerequisite: iron_skin
      legacy-ids: [ha_immovable]
      description: ["Reduces knockback while wearing sufficient heavy armor."]
      ranks:
        1: {required-skill-level: 45, cost: 1, effects: {knockback-resistance: 0.10, required-pieces: 3}}
        2: {required-skill-level: 75, cost: 1, effects: {knockback-resistance: 0.20, required-pieces: 3}}
        3: {required-skill-level: 100, cost: 1, effects: {knockback-resistance: 0.30, required-pieces: 2}}
    juggernaut:
      display-name: "Juggernaut"
      icon: NETHERITE_CHESTPLATE
      gui-slot: 29
      prerequisite: unshaken
      legacy-ids: [ha_juggernaut, ha_colossus]
      description: ["Grants additional protection in a complete heavy armor set."]
      ranks:
        1: {required-skill-level: 65, cost: 1, effects: {damage-reduction-percent: 5.0}}
        2: {required-skill-level: 100, cost: 1, effects: {damage-reduction-percent: 9.0}}

  light_armor:
    agile_defense:
      display-name: "Agile Defense"
      icon: LEATHER_CHESTPLATE
      gui-slot: 13
      legacy-ids: [la_agile_defense]
      description:
        - "Improves light armor effectiveness and carry capacity."
      ranks:
        1: {required-skill-level: 20, cost: 1, effects: {armor-percent: 1.3, carry-capacity: 6.0}}
        2: {required-skill-level: 40, cost: 1, effects: {armor-percent: 2.6, carry-capacity: 12.0}}
        3: {required-skill-level: 60, cost: 1, effects: {armor-percent: 3.9, carry-capacity: 18.0}}
        4: {required-skill-level: 80, cost: 1, effects: {armor-percent: 5.2, carry-capacity: 24.0}}
        5: {required-skill-level: 100, cost: 1, effects: {armor-percent: 6.5, carry-capacity: 30.0}}
    windstep:
      display-name: "Windstep"
      icon: FEATHER
      gui-slot: 20
      prerequisite: agile_defense
      legacy-ids: [la_swift_movement]
      description: ["Improves movement while wearing a complete light armor set."]
      ranks:
        1: {required-skill-level: 40, cost: 1, effects: {movement-speed-percent: 2.0}}
        2: {required-skill-level: 70, cost: 1, effects: {movement-speed-percent: 4.0}}
        3: {required-skill-level: 100, cost: 1, effects: {movement-speed-percent: 6.0}}
    evasion:
      display-name: "Evasion"
      icon: PHANTOM_MEMBRANE
      gui-slot: 29
      prerequisite: windstep
      legacy-ids: [la_evasion, la_wind_dancer]
      description: ["May reduce incoming combat damage with a visible cooldown."]
      ranks:
        1: {required-skill-level: 60, cost: 1, effects: {chance: 5.0, damage-reduction-percent: 25.0, cooldown-ticks: 100}}
        2: {required-skill-level: 100, cost: 1, effects: {chance: 8.0, damage-reduction-percent: 35.0, cooldown-ticks: 80}}

  fishing:
    experienced_angler:
      display-name: "Experienced Angler"
      icon: FISHING_ROD
      gui-slot: 13
      legacy-ids: [fish_patient_fisher]
      description: ["Improves Fishing XP and reduces hook waiting time."]
      ranks:
        1: {required-skill-level: 20, cost: 1, effects: {skill-xp-percent: 8.0, hook-wait-multiplier: 0.90}}
        2: {required-skill-level: 50, cost: 1, effects: {skill-xp-percent: 15.0, hook-wait-multiplier: 0.82}}
        3: {required-skill-level: 80, cost: 1, effects: {skill-xp-percent: 22.0, hook-wait-multiplier: 0.75}}
    strong_line:
      display-name: "Strong Line"
      icon: STRING
      gui-slot: 20
      prerequisite: experienced_angler
      legacy-ids: [fish_lucky_line]
      description: ["Improves the weight and length of successful fish catches."]
      ranks:
        1: {required-skill-level: 40, cost: 1, effects: {size-percent: 4.0}}
        2: {required-skill-level: 70, cost: 1, effects: {size-percent: 8.0}}
        3: {required-skill-level: 100, cost: 1, effects: {size-percent: 12.0}}
    treasure_hunter:
      display-name: "Treasure Hunter"
      icon: NAUTILUS_SHELL
      gui-slot: 24
      prerequisite: experienced_angler
      legacy-ids: [fish_treasure_hunter, fish_keen_eye]
      description: ["Improves rare treasure chances."]
      ranks:
        1: {required-skill-level: 50, cost: 1, effects: {treasure-chance-percent: 15.0}}
        2: {required-skill-level: 80, cost: 1, effects: {treasure-chance-percent: 30.0}}
    northern_fisherman:
      display-name: "Northern Fisherman"
      icon: HEART_OF_THE_SEA
      gui-slot: 31
      prerequisite: strong_line
      legacy-ids: [fish_master_angler, fish_legendary_fisher]
      description: ["Unlocks and improves legendary catches at Fishing level 100."]
      ranks:
        1: {required-skill-level: 100, cost: 1, effects: {legendary-chance-percent: 25.0}}

  smithing:
    eye_glass:
      display-name: "Eye Glass"
      icon: SPYGLASS
      gui-slot: 13
      legacy-ids: [sm_eye_glass]
      description: ["Allows qualifying mobs to drop enchanted LOTN gear."]
      ranks:
        1: {required-skill-level: 20, cost: 1, effects: {}}
    enchanter:
      display-name: "Enchanter"
      icon: ENCHANTED_BOOK
      gui-slot: 22
      prerequisite: eye_glass
      legacy-ids: [sm_enchanter]
      description: ["Allows enchanting and disenchanting through LOTN systems."]
      ranks:
        1: {required-skill-level: 40, cost: 1, effects: {}}
    temper:
      display-name: "Temper"
      icon: ANVIL
      gui-slot: 31
      prerequisite: eye_glass
      legacy-ids: [sm_temper]
      description:
        - "Improves leveled weapons and armor at an anvil."
        - "Rank I unlocks Fine gear; Rank II unlocks Superior gear."
      ranks:
        1: {required-skill-level: 20, cost: 1, effects: {maximum-upgrade-rank: 1}}
        2: {required-skill-level: 40, cost: 1, effects: {maximum-upgrade-rank: 2}}
    # Stage 2 identifiers and requirement hooks. Disabled until its perk graph/effects ship.
    leatherworking:
      enabled: false
      display-name: "Leatherworking"
      icon: LEATHER
      gui-slot: 10
      description: ["Stage 2 material-specialization hook for leather armor."]
      ranks: {1: {required-skill-level: 0, cost: 1, effects: {material-family: leather}}}
    chain_smithing:
      enabled: false
      display-name: "Chain Smithing"
      icon: CHAIN
      gui-slot: 11
      description: ["Stage 2 material-specialization hook for chainmail armor."]
      ranks: {1: {required-skill-level: 20, cost: 1, effects: {material-family: chainmail}}}
    golden_smithing:
      enabled: false
      display-name: "Golden Smithing"
      icon: GOLD_INGOT
      gui-slot: 12
      description: ["Stage 2 material-specialization hook for gold equipment."]
      ranks: {1: {required-skill-level: 30, cost: 1, effects: {material-family: gold}}}
    iron_smithing:
      enabled: false
      display-name: "Iron Smithing"
      icon: IRON_INGOT
      gui-slot: 14
      description: ["Stage 2 material-specialization hook for iron equipment."]
      ranks: {1: {required-skill-level: 30, cost: 1, effects: {material-family: iron}}}
    toolsmith:
      enabled: false
      display-name: "Toolsmith"
      icon: IRON_PICKAXE
      gui-slot: 15
      description: ["Stage 2 hook for axes, pickaxes, and hoes."]
      ranks: {1: {required-skill-level: 40, cost: 1, effects: {category: tools}}}
    advanced_smithing:
      enabled: false
      display-name: "Advanced Smithing"
      icon: SMITHING_TABLE
      gui-slot: 16
      description: ["Stage 2 hook for improved tempering effectiveness."]
      ranks: {1: {required-skill-level: 50, cost: 1, effects: {advanced-tempering: true}}}
    arcane_blacksmith:
      enabled: false
      display-name: "Arcane Blacksmith"
      icon: ENCHANTED_BOOK
      gui-slot: 19
      description: ["Stage 2 hook for tempering enchanted equipment."]
      ranks: {1: {required-skill-level: 60, cost: 1, effects: {temper-enchanted: true}}}
    diamond_smithing:
      enabled: false
      display-name: "Diamond Smithing"
      icon: DIAMOND
      gui-slot: 20
      description: ["Stage 2 material-specialization hook for diamond equipment."]
      ranks: {1: {required-skill-level: 70, cost: 1, effects: {material-family: diamond}}}
    netherite_smithing:
      enabled: false
      display-name: "Netherite Smithing"
      icon: NETHERITE_INGOT
      gui-slot: 21
      description: ["Stage 2 material-specialization hook for netherite equipment."]
      ranks: {1: {required-skill-level: 90, cost: 1, effects: {material-family: netherite}}}
    master_smithing:
      enabled: false
      display-name: "Master Smithing"
      icon: NETHERITE_BLOCK
      gui-slot: 23
      description: ["Stage 2 hook for maximum tempering mastery."]
      ranks: {1: {required-skill-level: 100, cost: 1, effects: {mastery: true}}}

item-progression:
  enabled: true
  max-level: 100
  weapon:
    experience-per-kill: 1.0
    experience-per-level: 1.0
  armor:
    experience-per-damage: 1.0
    experience-per-level: 10.0
xp-sources:
  combat:
    per-damage: 0.70
    max-per-hit: 12.0
    mob-tier-bonus: 0.08
    kill-bonus-per-max-health: 0.08
    maximum-kill-bonus: 6.0
  archery:
    distance-bonus-per-block: 0.01
    maximum-distance-bonus: 1.0
    critical-bonus: 0.10
  sneak:
    attack-multiplier: 0.75
  block:
    per-damage-prevented: 0.90
    max-per-hit: 12.0
  heavy-armor:
    per-damage: 0.45
    max-per-hit: 8.0
  light-armor:
    per-damage: 0.45
    max-per-hit: 8.0
  armor:
    valid-causes: [ENTITY_ATTACK, ENTITY_SWEEP_ATTACK, PROJECTILE, ENTITY_EXPLOSION]
  smithing:
    crafting-base: 1.0
    netherite-upgrade: 24.0
    tier-weights:
      0: 0.50
      1: 1.00
      2: 2.00
      3: 5.00
      4: 9.00

one_handed:
  enabled: true
  max-level: 100
  damage-per-level: 0.0025
two_handed:
  enabled: false
  max-level: 100
  damage-per-level: 0.0035
archery:
  enabled: true
  max-level: 100
  damage-per-level: 0.0025
block:
  enabled: true
  max-level: 100
  damage-reduction-per-level: 0.0015
heavy_armor:
  enabled: true
  max-level: 100
  armor-per-level: 0.0015
  attacker-damage-bonus: 0.03
  hardened-reduction: 0.05
light_armor:
  enabled: true
  max-level: 100
  armor-per-level: 0.001
  swift-movement-speed: 0.03
sneak:
  enabled: true
  max-level: 100
mining:
  enabled: false
  max-level: 100
woodcutting:
  enabled: false
  max-level: 100
fishing:
  enabled: false
  max-level: 100
alchemy:
  enabled: false
  max-level: 100
enchanting:
  enabled: false
  max-level: 100
smithing:
  enabled: true
  max-level: 100
survival:
  enabled: false
  max-level: 100
restoration:
  enabled: false
  max-level: 100
destruction:
  enabled: false
  max-level: 100
farming:
  enabled: false
  max-level: 100
trading:
  enabled: false
  max-level: 100
```
:::

:::spoiler survival.yml
```yaml
#####################################################################
# Note: Plugin is in Early Access - its very experimental right now #
#####################################################################

schema-version: 3

injuries:
  broken-leg:
    enabled: true
    movement-speed-multiplier: 0.55
    disable-sprinting: true
    persist-through-death: true
    healing-potions:
      - cure
      - minor_health
      - health
      - greater_health
    natural-healing:
      enabled: false
      time-ticks: 48000
    minimum-fall-damage: 4.0
    base-chance: 0.08
    chance-per-extra-damage: 0.03
    maximum-chance: 0.80

messages:
  broken: "&c&lLotN: You broke your leg!\n&7Use an approved LOTN health potion to mend it."
  still-broken: "&cLotN: Your leg is still broken. Use an approved LOTN health potion."
  healed-by-potion: "&aLotN: The potion mended your broken leg!"
  healed-by-admin: "&aLotN: Your broken leg was healed."
  healed-on-death: "&aLotN: Your broken leg did not persist through death."
  healed-naturally: "&aLotN: Your broken leg healed over time."
  admin:
    no-permission: "&cYou do not have permission."
    player-not-found: "&cPlayer not found."
    console-player-required: "&cConsole must provide an online player: /lotnea {command} <player>"
    already-broken: "&e{player} already has a broken leg."
    broken: "&aBroke {player}'s leg."
    not-broken: "&e{player} does not have a broken leg."
    healed: "&aHealed {player}'s broken leg."
```
:::