# Infinite.js API

**In Progress** - Feel free to open an Issue if you need Clarrification or have a suggestion 

<a name="-1"></a>

|Contents|
|--------|
|[Menu](#0)|
|[Configs](#1)|
|[Callbacks](#2)|

---

## <a name="0"></a>Menu

**All menu Element must be called after the API**

[ **Checkbox** ]
Syntax: CreateCheckbox(label, defaultvalue, row)

**Creates** a Checkbox with the specified Label, Default Value, and Row 

```java
CreateCheckbox("Infinite API", false, 0);
function Checkbox()
{
    if(GetMenuValue("Infinite API"))
    {
        Cheat.Print("Checkbox Enabled");
    }
}

Global.RegisterCallback("Draw", "Checkbox");
```

[ **Get Value** ]
Syntax: GetMenuValue(label)

**Returns** the Value of a Menu Element

```java
CreateCheckbox("Menu Element", false, 0);
function Checkbox()
{
    Cheat.Print("The value of the element is: " + GetMenuValue("Menu Element"));
  
}

Global.RegisterCallback("Draw", "Checkbox");
```

[ **Set Value** ]
Syntax: SetMenuValue(label, value)

**Sets** the Value of a Menu Element

```java
CreateCheckbox("Menu Element", false, 0);
function Checkbox()
{
    SetMenuValue("Menu Element", true);
}

Global.RegisterCallback("Draw", "Checkbox");
```
---

## <a name="1"></a>Configs
[ **Load Script from Config** ]
Syntax: LoadFromConfig() [ ** must be called at the end of a script** ]

**Loads and Updates** all menu elements from the loaded config

```java
CreateCheckbox("Infinite API", false, 0);

function onDraw()
{



}

Global.RegisterCallback("Draw", "onDraw");


//at end of script
LoadFromConfig()
```

---

## <a name="2"></a>Callbacks

[ **Optimized Callbacks** ]
Syntax: Callback(type, function); [ ** Function to be Invoked not as a string** ]

**Callbacks** the selected function


```java
CreateCheckbox("Draw Rectangle", false, 0);

function onDraw()
{
    if(!GetMenuValue("Draw Rectangle")) { return; }

    Render.Rect(100, 100, 150, 150, [255, 0, 0, 255]);
}

Callback(0, onDraw)

```

[ **Callback Types** ]
```java

0 - Draw
1 - CreateMove

```


