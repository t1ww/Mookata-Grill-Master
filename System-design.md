# 🏗️ Mookata Tycoon – Building & Placement System (v1)

## 1. Overview
This system handles **grid-based placement** of furniture, decorations, and props inside the player’s shop.  
It separates **main objects** (tables, counters, desks) from **sub-items** (pans, plates, small props) using a **main grid + subgrid** approach.

---

## 2. Main Grid
- **Purpose:** Controls placement of large objects (tables, counters, walls).  
- **Size:** Configurable; e.g., 2×2 or 4×4 studs per tile.  
- **Rules:**
  - Objects snap to nearest available grid tile.  
  - Prevents overlapping main furniture.  
  - Used for adjacency detection (table next to grill, chairs around table).  
- **Data:**
  - Store each placed object with:
    - `gridPosition` (Vector2 or Vector3)  
    - `FurnitureType` (Table, Counter, Chair, Grill, etc.)  
    - `FurnitureGroupId` (for connected sets)

---

## 3. Subgrid (Props on Furniture)
- **Purpose:** Allows placing small items **on top of main furniture**.  
- **Example:** Pan on table, plates on counter.  
- **Rules:**
  - Each main furniture object can have its own subgrid layout.  
  - Subgrid snaps small props independently of main grid.  
  - Subgrid spots are validated for collisions with other props only.  
- **Data:**
  - Each furniture object stores a table of subgrid slots:
    - `Occupied` boolean  
    - `PropReference` (Instance of the prop placed)  

---

## 4. Furniture Groups
- **Purpose:** Identify objects that are “connected” (table + grill + chairs).  
- **Implementation:**
  - Assign `FurnitureGroupId` to objects when placed adjacent to each other.  
  - Adjacent objects automatically share the same group.  
  - Used for NPC seating, cooking logic, or upgrades.  

---

## 5. Placement Validation
- **Main grid:**  
  - Check if target tile is empty.  
  - Check for shop boundaries (cannot place outside walls).  
- **Subgrid:**  
  - Check if spot is free.  
  - Optional: check for physics collisions if props can fall.  

---

## 6. Walls / Shop Layout
- **Option 1 (Recommended for hobby project):** Pre-made shop shell.  
  - Walls, doors, and basic floor layout are static.  
  - Players can place furniture inside only.  
- **Option 2 (Optional advanced):** Fully player-built shop.  
  - Players can place/move walls and floors.  
  - Requires additional collision, snapping, and pathfinding logic.  

---

## 7. Example Placement Workflow
1. Player selects a furniture item (e.g., table).  
2. Object previews at mouse location (snapped to main grid).  
3. Validate placement (tile empty, within shop bounds).  
4. Place object → assign `gridPosition` and optionally `FurnitureGroupId`.  
5. Player selects a prop (e.g., pan).  
6. Prop previews on table (snapped to subgrid).  
7. Validate subgrid spot (no collision with other props).  
8. Place prop → update subgrid slot as occupied.

---

## 8. Future Expansion Ideas
- Upgrade furniture (e.g., grill upgrade swaps model).  
- Dynamic furniture adjacency effects (e.g., table + grill combo gives bonus).  
- NPC seating detection using `FurnitureGroupId`.  
- Props with physics (can slide or fall off, visual only).  

---