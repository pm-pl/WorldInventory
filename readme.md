# 🌍 WorldInventory v1.0.2

<p align="center">
  <img src="https://github.com/xBeastMode/WorldInventory/raw/master/icon.png" alt="WorldInventory Icon">
</p>

<p align="center">
  <a href="https://poggit.pmmp.io/p/WorldInventory">
    <img src="https://poggit.pmmp.io/shield.api/WorldInventory" alt="API">
  </a>
  <a href="https://poggit.pmmp.io/p/WorldInventory">
    <img src="https://poggit.pmmp.io/shield.dl/WorldInventory" alt="Downloads">
  </a>
</p>

A powerful PocketMine-MP plugin that allows servers to **manage player inventories per world** with flexible rules and database support.

---

## ✨ Features

- 🔄 Clear inventories between worlds  
- 🔗 Link inventories across multiple worlds  
- 💾 Save unique inventories per world  
- 🎒 Define custom inventories for specific worlds  
- 🗄️ MySQL and SQLite support  
- 🧩 Full API for developers  
- 🚧 Planned: Command support  

> 💡 Have an idea? Open an issue!

---

## 🧠 Overview

WorldInventory gives server owners full control over how player inventories behave when switching worlds.

You can:

- Share inventories between worlds  
- Isolate inventories per world  
- Reset inventories completely  
- Provide predefined loadouts  

---

## 📦 Inventory Types

| Type     | Description |
|----------|------------|
| `clear`  | Inventory is wiped every time the player enters the world |
| `linked` | Worlds share the same inventory |
| `saved`  | Each world has its own persistent inventory |
| `custom` | Players receive predefined items |

---

## ⚙️ Configuration

### 🗄️ Database

Supports both **SQLite** and **MySQL**:

```yaml
database:
  type: sqlite

  sqlite:
    file: data.sqlite

  mysql:
    host: 127.0.0.1
    username: root
    password: ""
    schema: your_schema

  worker-limit: 1
```

---

### 🌍 World Settings

```yaml
worlds:
  world: "linked"
  foo: "linked"
  bar: "saved"
  baz: "clear"
  qux: "custom"
```

---

### 🎒 Custom Inventories

Define items for worlds using the `custom` type:

```yaml
items:
  qux:
    armor:
      - "diamond_helmet:1:custom armor:custom lore:protection:1"
    inventory:
      - "diamond_sword:1:custom sword:custom lore:protection:1"
```

---

### 🧩 Item Format

```
item_name:count:custom_name:lore:enchantments
```

Example:

```
diamond_sword:1:Epic Sword:Sharp blade:sharpness:5:unbreaking:3
```

---

## 🧪 Learning Outcomes

This project demonstrates:

- Event-driven plugin design in PHP  
- Persistent data handling (SQLite/MySQL)  
- Inventory state management  
- Designing flexible configuration systems  
- API design for extensibility  

---

## 🔌 API

WorldInventory includes a full API, allowing developers to:

- Hook into inventory changes  
- Extend behavior  
- Integrate with other plugins  

Explore the source code for usage examples.

---

## 🚀 Use Cases

- PvP servers (separate kits per world)  
- Minigames (isolated inventories)  
- Hub servers (shared inventories)  
- Custom gamemodes  

---

## 🤝 Contributing

Contributions are welcome:

1. Fork the repository  
2. Create a feature branch  
3. Commit your changes  
4. Open a pull request  
