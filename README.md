## 🔥 Heating Control - Window/Door Detection v1.1

### ✨ New Features

- **🔄 Inverted Sensor Logic Support**: New `sensor_logic` parameter to handle sensors where `on=closed` and `off=open` (common with some door/window sensors)
- **⚙️ Configurable sensor behavior**: Choose between "Normal" and "Inverted" logic directly in the blueprint configuration

### 🐛 Bug Fixes

- **Fixed inverted behavior**: Resolves issue where heating would turn ON when opening sensors and OFF when closing them
- **Improved trigger reliability**: Enhanced template triggers for optional door sensors to prevent errors with empty lists

### 🎯 Features Summary

- **Immediate window detection**: Instant heating control when windows open/close
- **Delayed door detection**: Configurable delay (default 4 minutes) before reacting to door sensors
- **Flexible heating modes**: Support for comfort, comfort-1, comfort-2, eco, and off presets
- **Activation toggle**: Easy enable/disable without deleting the automation
- **Optional door sensors**: Works with windows only or windows + doors

### 📦 Compatibility

- ✅ Compatible with climate entities supporting standard presets (`comfort`, `eco`, etc.)
- ✅ Works with both normal and inverted binary sensors
- ✅ Supports French wire pilot heating controllers (fil pilote)

### 🔧 Installation

1. Download `heating_window_door_control.yaml`
2. Place in `/config/blueprints/automation/jcspenle/`
3. Reload blueprints in Home Assistant
4. Create automation from blueprint

---

**⚠️ Breaking Change**: Users with inverted sensors must now select "Inverted" in the `Sensor Logic` parameter
