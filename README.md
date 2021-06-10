# Infinite.js API



<a name="-1"></a>

|Contents|
|--------|
|[Menu](#0)|

---

## <a name="0"></a>Menu
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

