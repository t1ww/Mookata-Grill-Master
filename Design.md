# 🐷 Mookata Tycoon – Updated Design Spec (v2)

---

## 1. 🔥 Core Gameplay Loop
1. Buy pork  
2. Feed pigs (once unlocked)  
3. Influence texture  
4. Process meat  
5. Marinate for flavor  
6. Cook & serve to customers  
7. Earn based on satisfaction, volume, and mutation effects  

---

## 2. 🧍 Customer System

### 2.1 Customer Stats
Procedurally generated with:

| Stat | Description |
|------|------------|
| Wallet | Max budget per meal or total |
| Flavor Preference | Desired range per flavor type |
| Texture Preference | Desired texture range |
| Standard | Minimum quality threshold |
| Eating Speed Multiplier | Affected by satisfaction |

### 2.2 Satisfaction Score
**Factors:**
- Flavor match %  
- Texture match %  
- Mutation bonus  

**Effects:**
- Faster eating  
- More food consumed  
- Higher tips  

**Example:**
- 90–100% Salty preference → gets 1000% salty pork  
- Satisfaction 110% → Chaos mode triggered  

---

## 3. 🍢 Marination System
- Flavor types: Spicy, Salty, Sweet, Sour, Tangy, Bitter  
- Ingredients contribute %  
- Fully player-customizable  

---

## 4. 🧸 Texture System
**Affected by feeding stage:**

| Texture | Feed Type |
|---------|-----------|
| Tenderness | Acidic feeds (lime, vinegar) |
| Crispiness | Solid/hard feeds (sugar, glass) |
| Meatyness | Organic (grass, soy, natural) |

### 4.1 Unified Marination & Feed Table (Dual Effects)
| Name | Type | Spicy | Salty | Sweet | Sour | Tangy | Bitter | Tenderness | Crispiness | Meatyness | Notes |
|------|------|-------|-------|-------|------|-------|--------|------------|------------|-----------|-------|
| Chili Paste | Marinade | +30% | | +10% | | +5% | | | | | Spicy burn + mild tender |
| Fish Sauce | Marinade | | +40% | | | | +5% | | | | Salty, rich umami |
| Honey | Marinade | | | +50% | | | | +10% | +20% | | Sugary = slight tender & crisp |
| Lime Juice | Both | | | | +30% | +10% | | +30% | | | Strong acid, great for soft texture |
| Tamarind Extract | Marinade | | | | | +20% | +25% | +5% | +15% | | Mild acid = moderate tenderness |
| Bitter Gourd Juice | Marinade | | | | | | +40% | +5% | | | Adds bitterness, lightly softens |
| Garlic Soy Sauce | Marinade | | +25% | +10% | | | +5% | | | | Balanced seasoning |
| Vinegar Slurry | Feed | | | | | | | +50% | | | Strong acid feed |
| Sugar Cubes | Feed | | | | | | | | +40% | | High crispiness |
| Crushed Glass | Feed | | | | | | | | | +60% | Dangerous but crisp |
| Grass Clippings | Feed | | | | | | | | | +30% | Base meatyness source |
| Soy Meal | Feed | | | | | | | | | +50% | High protein |
| Spoiled Milk | Feed | | | | | | | +20% | +10% | | Soft, mixed feed |
| Junk Food | Feed | | | | | | | +10% | +20% | +10% | Unstable, multi-texture |
| Fermented Shrimp | Marinade | +10% | +30% | | +10% | | +5% | | | | Flavor bomb + light softening |
| Syrup Mix | Marinade | | | +40% | | +10% | | +5% | | +25% | Sugary, good for sweet-crisp |
| Pickled Chili | Both | +35% | +10% | | +15% | +10% | | +25% | | | Acidic-spicy with softening |
| Coconut Cream | Marinade | | | +20% | | | | +15% | | +10% | Adds richness and body |
| Miso Paste | Marinade | | +20% | +10% | | | +10% | | | +15% | Umami boost + softening |

---

## 5. ⚡ Mutation System (Simplified)

| Mutation | Trigger | Visual | Price Multiplier |
|----------|--------|--------|----------------|
| Charged Pig | Storm | Electric sparks | x1.5 |
| Burnt Pig | Heatwave | Charred look | x1.2 |
| Frozen Pig | Cold Front | Ice crystals | x1.3 |
| Gold Pig | Festival | Glowing gold | x2.0 |

- Triggered by environmental events  
- Purely bonuses (no flavor/texture changes)  
- Players can target mutations via timing  

---

## 6. 💡 Chaos Mechanics (Optional)
- **Overfeeding:** High satisfaction → overeating → table breaking, machine overload  
- **Emergency Cooldown:** Pork reserves empty → triggers mini-game or wait cooldown  

---

## 7. 🧪 Progression System
- Unlock automation: Cookbots, auto-feed, marinade arms  
- Discover secret recipes via combinations  
- Upgrade tools and kitchen systems  

---

## 8. 🐖 Early Game Pig Sourcing (NEW)
Before owning pigs, players must buy pork from stores:

| Pork Tier | Source | Price | Description |
|-----------|--------|-------|------------|
| Frozen Pork | Cheap Market | $ | Low freshness, low satisfaction potential |
| Standard Pork | Butcher Shop | $$ | Average quality |
| High-Quality Pork | Specialty Store | $$$ | Better texture baseline |
| Premium Pork | Luxury Vendor | $$$$ | Max satisfaction baseline, good mutations |

- Pig farming unlocked later as an upgrade milestone  
- Once pigs are unlocked, player can raise/feed them directly for custom texture feature  

---

## 9. 🍳 Cooking Pan System (NEW)

| Pan Tier | Speed Multiplier | Bonus Effects |
|----------|----------------|---------------|
| Rusty Pan | x1.0 | Basic |
| Iron Pan | x1.1 | Slightly faster cook/eat |
| Non-stick Pan | x1.25 | Faster cooking + small satisfaction boost |
| Electric Grill | x1.5 | High speed, bonus to spicy/salty flavors |
| Titanium Pan | x2.0 | Max speed, doubles satisfaction bonus |
