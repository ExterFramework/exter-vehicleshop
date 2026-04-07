<div align="center">

# 🚗 Exter Vehicle Shop

### A Modern, Feature-Rich Vehicle Dealership System for FiveM

[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![FiveM](https://img.shields.io/badge/FiveM-Ready-brightgreen.svg)](https://fivem.net/)
[![Exter Framework](https://img.shields.io/badge/Exter-Framework-orange.svg)](https://github.com/ExterFramework)

*A fully configurable vehicle shop resource built on the Exter Framework, providing players with an immersive car-buying experience through a sleek NUI interface.*

</div>

---

## 📋 Table of Contents

- [Features](#-features)
- [Preview](#-preview)
- [Dependencies](#-dependencies)
- [Installation](#-installation)
- [Configuration](#-configuration)
- [Project Structure](#-project-structure)
- [Localization](#-localization)
- [Contributing](#-contributing)
- [License](#-license)

---

## ✨ Features

- **Modern NUI Interface** — Clean, responsive HTML/CSS/JS dealership UI for seamless player interaction
- **Multi-Framework Support** — Built on Exter Framework with native compatibility for ESX and QBCore
- **Vehicle Categories** — Organize inventory by class (Sports, SUVs, Sedans, Compacts, etc.)
- **Test Drive System** — Let players test vehicles before committing to a purchase
- **Configurable Dealerships** — Set up multiple dealership locations with custom vehicle inventories
- **Localization Ready** — Full i18n support with easily extendable locale files
- **Optimized Performance** — Lightweight resource with minimal impact on server performance

---

## 📸 Preview

> *Screenshots coming soon — contributions welcome!*

---

## 📦 Dependencies

| Dependency | Description |
|---|---|
| [Exter Framework](https://github.com/ExterFramework) | Core framework providing multi-framework bridge and utilities |

> **Note:** Exter Framework handles compatibility with ESX, QBCore, and other supported frameworks automatically.

---

## 🚀 Installation

1. **Download** the latest release or clone the repository:

   ```bash
   git clone https://github.com/ExterFramework/exter-vehicleshop.git
   ```

2. **Place** the `exter-vehicleshop` folder into your server's `resources` directory:

   ```
   resources/
   └── [exter]/
       └── exter-vehicleshop/
   ```

3. **Ensure** the resource in your `server.cfg`:

   ```cfg
   ensure exter-vehicleshop
   ```

4. **Configure** the resource by editing `shared/config.lua` to match your server's needs (see [Configuration](#-configuration)).

5. **Restart** your server or start the resource:

   ```
   refresh
   ensure exter-vehicleshop
   ```

---

## ⚙️ Configuration

All configuration is managed through `shared/config.lua`. Below are the key configurable options:

| Option | Type | Description |
|---|---|---|
| `Dealerships` | `table` | Define dealership locations, blips, NPC positions, and available vehicle categories |
| `Vehicles` | `table` | Configure available vehicles with model names, display labels, and pricing |
| `Categories` | `table` | Organize vehicles into browsable categories |
| `TestDrive` | `table` | Set test drive duration, spawn points, and restrictions |

<details>
<summary><strong>Example Configuration Snippet</strong></summary>

```lua
Config = {}

-- Dealership location configuration
Config.Dealerships = {
    ["pdm"] = {
        label = "Premium Deluxe Motorsport",
        blip = { sprite = 326, color = 2, scale = 0.8 },
        categories = { "sports", "sedans", "suvs", "compacts" },
        -- Additional options...
    }
}

-- Test drive settings
Config.TestDrive = {
    duration = 60,  -- seconds
    -- Additional options...
}
```

</details>

> For a complete list of options, refer to the comments within [`shared/config.lua`](shared/config.lua).

---

## 📁 Project Structure

```
exter-vehicleshop/
├── client/
│   └── core.lua            # Client-side logic (NUI callbacks, vehicle spawning, UI interactions)
├── server/
│   └── core.lua            # Server-side logic (purchase validation, database operations)
├── shared/
│   └── config.lua          # Shared configuration (dealerships, vehicles, categories)
├── html/
│   ├── index.html          # NUI interface markup
│   ├── style.css           # NUI styling
│   └── script.js           # NUI client-side JavaScript
├── locales/
│   └── en.lua              # English locale strings
├── fxmanifest.lua          # Resource manifest
├── LICENSE                 # GPL-3.0 License
└── README.md               # This file
```

---

## 🌐 Localization

Exter Vehicle Shop supports multiple languages through locale files located in the `locales/` directory.

**Adding a new language:**

1. Copy `locales/en.lua` and rename it to your language code (e.g., `fr.lua`, `de.lua`, `es.lua`).
2. Translate all string values while keeping the keys unchanged.
3. The framework will automatically detect and load the appropriate locale based on server configuration.

**Currently available:**
- 🇬🇧 English (`en`)

> Community translations are welcome! See [Contributing](#-contributing).

---

## 🤝 Contributing

Contributions are what make the open-source community an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

1. **Fork** the repository
2. **Create** your feature branch (`git checkout -b feature/amazing-feature`)
3. **Commit** your changes (`git commit -m 'feat: add amazing feature'`)
4. **Push** to the branch (`git push origin feature/amazing-feature`)
5. **Open** a Pull Request

### Contribution Ideas

- 🌍 Add locale translations
- 🎨 UI/UX improvements to the NUI interface
- 🐛 Bug fixes and performance optimizations
- 📖 Documentation improvements
- ✨ New features (finance system, vehicle history, etc.)

---

## 📄 License

This project is licensed under the **GNU General Public License v3.0** — see the [LICENSE](LICENSE) file for details.

```
Copyright (C) 2024 ExterFramework

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.
```

---

<div align="center">

**Made with ❤️ by [Exter Framework](https://github.com/ExterFramework)**

⭐ Star this repository if you find it useful!

</div>
