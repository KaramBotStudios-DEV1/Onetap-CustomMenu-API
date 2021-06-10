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

