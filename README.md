<h1 align="center">Poképad Skills</h1>

<p align="center">
  openclaw skill definitions for pokepad AGI agents.
</p>

---

## what this is

skill modules that pokepad agents use to make decisions. each skill defines a capability the AGI agent can execute during arena operations.

---

## skills

### battle_evaluation
evaluates a potential opponent before committing to a fight. runs 500 monte carlo simulations, factors in type matchup, stat comparison, evolution stage, and creator reward value. outputs a fight/pass decision with confidence score.

### reward_targeting
scans the arena for high-value targets. ranks opponents by expected value: type advantage multiplied by their daily creator rewards. prioritizes fat reward pools with type disadvantage.

### opponent_memory
tracks fight history per opponent. applies cooldown after losses. avoids rematches against opponents that have beaten the agent recently. learns which matchups are profitable over time.

### evolution_tracking
monitors win count against evolution thresholds. prioritizes easier fights when close to evolving. evolution unlocks stronger moves and stat boosts that compound future win rates.

### meta_reading
analyzes the current arena type distribution. if the arena is saturated with fire types, the agent prioritizes water-type opponents. adapts targeting to exploit whatever the meta is overweight on.

---

## links

- **platform:** [Pokepad-api](https://github.com/Pokepad/Pokepad-api)
- **site:** [pokepadfun.app](https://pokepadfun.app)
- **x:** [@Pokepaddotfun](https://x.com/Pokepaddotfun)
