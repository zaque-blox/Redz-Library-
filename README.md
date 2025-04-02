## Redz Library v5

 #### carregar gui
  
``` Lua
local redzlib = loadstring(game:HttpGet("https://raw.githubusercontent.com/tbao143/Library-ui/refs/heads/main/Redzhubui"))()
```
 #### criar janela
    
``` Lua
local Window = redzlib:MakeWindow({
  Title = "Yor Hub",
  SubTitle = "by Jubileu",
  SaveFolder = "ConfigFolder"
})
```

#### icone flutuante minimize

``` Lua
Window:AddMinimizeButton({
    Button = { Image = "rbxassetid://71014873973869", BackgroundTransparency = 0 },
    Corner = { CornerRadius = UDim.new(35, 1) },
})
```

 #### discord invite

``` Lua
Tab1:AddDiscordInvite({
    Name = "Name Hub",
    Description = "Join server",
    Logo = "rbxassetid://18751483361",
    Invite = "Link discord invite",
})
```

 #### set Theme

Dark
``` Lua
redzlib:SetTheme("Dark")
```

Darker

``` Lua
redzlib:SetTheme("Darker")
```

Purple
``` Lua
redzlib:SetTheme("Purple")
```

 #### criar aba
    
``` Lua
local Tab1 = Window:MakeTab({"nome da aba", "Icone da aba"})
```

 #### criar sessão

``` Lua
local Section = Tab:AddSection({"nome da sessão"})
```

 #### criar parágrafo
    
``` Lua
local Paragraph = Tab:AddParagraph({"nome do seu parágrafo", ""})
```

 #### criar toggle

``` Lua
local Toggle = Tab:AddToggle({
  Name = "nome do seu toggle",
  Default = false
})
```

 #### criar slider

``` Lua
Tab:AddSlider({
  Name = "nome do seu Slider",
  Min = 1,
  Max = 10,
  Increase = 1,
  Default = 5,
  Callback = function(Value)
    
  end
})
```

 #### criar botão

``` Lua
local Button = Tab:AddButton({"nome do seu botão"})
```

 #### criar dropdown

``` Lua
local Dropdown = Tab:AddDropdown({
  Name = "nome do seu dropdow ",
  Description = "",
  Options = {"um", "dois", "três"},
  Default = "two",
  Flag = "dropdown",
  Callback = function(Value)
    
  end
})
```

#### criar text box

``` Lua
Tab1:AddTextBox({
  Name = "Name item",
  Description = "1 Item on 1 Server", 
  PlaceholderText = "item only",
  Callback = function(Value)
    
  end
})
```

### Exemplo

``` Lua
-- Carregar elementos
local redzlib = loadstring(game:HttpGet("https://raw.githubusercontent.com/tbao143/Library-ui/refs/heads/main/Redzhubui"))()

-- Criar Janela
local Window = redzlib:MakeWindow({
  Title = "SEU HUB", -- Nome Do seu script
  SubTitle = "by", -- Criado por
  SaveFolder = "ConfigFolder" -- Pasta de configurações 
})

-- Botão minimize
Window:AddMinimizeButton({
    Button = { Image = "rbxassetid://71014873973869", BackgroundTransparency = 0 },
    Corner = { CornerRadius = UDim.new(35, 1) },
})

-- Criar Aba Main
local MainTab = Window:MakeTab({"Main", "Home"})

-- Sessão Main
local Section = MainTab:AddSection({"Main"})

local playerName = game.Players.LocalPlayer.Name

-- Criar parágrafo Com o nick do Local Player
local Paragraph = MainTab:AddParagraph({"Seja Bem vindo(a) " .. playerName .. "!", ""})

local Toggle = MainTab:AddToggle({
  Name = "Toggle",
  Default = false
})

MainTab:AddSlider({
  Name = "slider",
  Min = 1,
  Max = 10,
  Increase = 1,
  Default = 5,
  Callback = function(Value)
    
  end
})

local Button = MainTab:AddButton({"botão"})

local Dropdown = Tab:AddDropdown({
  Name = "nome do seu dropdow ",
  Description = "",
  Options = {"um", "dois", "três"},
  Default = "um",
  Flag = "dropdown",
  Callback = function(Value)
    
  end
})

```
