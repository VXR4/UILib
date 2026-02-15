# 🧙 [Wizard UI Library](https://github.com/bloodball/UI-Librarys/blob/main/wizard) Example (Roblox)

[![Preview](Screenshot%202026-02-15%20154734.png)](Screenshot%202026-02-15%20154734.png)

Simple example script

---

## 📦 Library Source

```lua
local Library = loadstring(Game:HttpGet("https://raw.githubusercontent.com/bloodball/-back-ups-for-libs/main/wizard"))()
```

This loads the Wizard UI Library dynamically using HttpGet.

---

## 🪟 Creating a Window

```lua
local PhantomForcesWindow = Library:NewWindow("Combat")
```

Creates a new window titled "Combat".

---

## 📂 Creating a Section

```lua
local KillingCheats = PhantomForcesWindow:NewSection("Kill Options")
```

Adds a section named "Kill Options" inside the window.

---

## 🧩 UI Elements

### 🔘 Button

```lua
KillingCheats:CreateButton("Button", function()
    print("HI")
    -- ...
end)
```

Executes a function when clicked.

---

### 📝 Textbox

```lua
KillingCheats:CreateTextbox("TextBox", function(text)
    print(text)
end)
```

Returns user input as `text`.

---

### ✅ Toggle

```lua
KillingCheats:CreateToggle("Auto Ez", function(value)
    print(value)
end)
```

Returns true or false depending on toggle state.

---

### 📋 Dropdown

```lua
KillingCheats:CreateDropdown("DropDown", {"Hello", "World", "Hello World"}, 2, function(text)
    print(text)
end)
```

- Options list
- Default selected index: 2
- Returns selected option text

---

### 🎚 Slider

```lua
KillingCheats:CreateSlider("Slider", 0, 100, 15, false, function(value)
    print(value)
end)
```

Parameters:
- Minimum: 0
- Maximum: 100
- Default: 15
- Precise value: false
- Returns current slider value

---

### 🎨 Color Picker

```lua
KillingCheats:CreateColorPicker("Picker", Color3.new(255, 255, 255), function(value)
    print(value)
end)
```

Returns selected Color3 value.

---

## 🛠 Features Demonstrated

- Window creation  
- Section creation  
- Button  
- Textbox  
- Toggle  
- Dropdown  
- Slider  
- Color Picker  

---

