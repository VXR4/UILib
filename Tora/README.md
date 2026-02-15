# 🧊 Tora UI Library Example (Roblox)

[![Preview](Screenshot%202026-02-15%20155628.png)](Screenshot%202026-02-15%20155628.png)

Simple example script using Tora Library

---

## 📦 Library Source

```lua
local library = loadstring(game:HttpGet(
    "https://raw.githubusercontent.com/liebertsx/Tora-Library/main/src/librarynew",
    true
))()
```

This loads the Tora UI Library dynamically using HttpGet.

---

## 🪟 Creating a Window

```lua
local window = library:CreateWindow("Main Window")
```

Creates a new window with the title "Main Window".

---

## 📂 Creating a Folder

```lua
local folder = window:AddFolder("Main Section")
```

Adds a folder (section container) inside the window.

---

## 🧩 UI Elements

### 🔘 Button

```lua
folder:AddButton({
    text = "Click Me",
    flag = "button_flag",
    callback = function()
        print("Button clicked")
    end
})
```

---

### ✅ Toggle

```lua
folder:AddToggle({
    text = "Auto Mode",
    flag = "toggle_flag",
    callback = function(value)
        print(value)
    end
})
```

---

### 🏷 Label

```lua
folder:AddLabel({
    text = "This is a label",
    type = "label"
})
```

---

### 🎚 Slider

```lua
folder:AddSlider({
    text = "FOV",
    min = 70,
    max = 170,
    dual = false,
    type = "slider",
    callback = function(value)
        print(value)
    end
})
```

---

### 🎨 Color Picker

```lua
folder:AddColor({
    text = "Color Picker",
    flag = "color_flag",
    type = "color",
    callback = function(value)
        print(value)
    end
})
```

---

### 📋 Dropdown

```lua
folder:AddList({
    text = "Select Option",
    values = {"Red", "Green", "Blue"},
    flag = "dropdown_flag",
    open = false,
    callback = function(value)
        print(value)
    end
})
```

---

### ⌨ Bind

```lua
folder:AddBind({
    text = "Toggle UI",
    key = "RightControl",
    hold = false,
    callback = function()
        print("Key pressed")
    end
})
```

---

## 🚀 Final (Required)

```lua
library:Init()
```

UI will not appear without calling Init().

---

## ❌ Close Library

```lua
library:Close()
```

Closes the UI window.
