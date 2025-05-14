## Redz Library v5

 #### load
  
``` Lua
local redzlib = loadstring(game:HttpGet("https://raw.githubusercontent.com/tbao143/Library-ui/refs/heads/main/Redzhubui"))()
```
 #### window
    
``` Lua
local Window = redzlib:MakeWindow({
  Title = "Yor Hub",
  SubTitle = "by Jubileu",
  SaveFolder = "ConfigFolder"
})
```

#### minimize

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

 #### aba
    
``` Lua
local Tab = Window:MakeTab({"Aba", "icone name"})
```

 #### section

``` Lua
local Section = Tab:AddSection({"section"})
```

 #### paragraph
 
``` Lua
local Paragraph = Tab:AddParagraph({"Paragraph", ""})
```

 #### toggle

``` Lua
local Toggle = Tab:AddToggle({
  Name = "Toggle",
  Default = false,
  Flag = "MyToggleFlag",
  Callback = function(Value)
    if Value then
      print("Toggle ativado!")
    else
      print("Toggle desativado!")
    end
  end
})
```

 #### slider

``` Lua
Tab:AddSlider({
  Name = "Slider",
  Min = 1,
  Max = 10,
  Increase = 1,
  Default = 5,
  Flag = "MySliderFlag",
  Callback = function(Value)
    print("Valor do Slider: " .. Value)
  end
})
```

 #### Button

``` Lua
local Button = Tab:AddButton({"button"})
```

 #### dropdown

``` Lua
local Dropdown = Tab:AddDropdown({
  Name = "Dropdown",
  Description = "",
  Options = {"Um", "Dois", "Três"},
  Default = "Um",
  Flag = "MyDropdownFlag",
  Callback = function(Value)
    print("Dropdown selecionado: " .. Value)
  end
})
```

#### text box

``` Lua
Tab:AddTextBox({
  Name = "Name Item",
  Description = "1 Item on 1 Server",
  PlaceholderText = "Digite algo",
  Callback = function(Value)
    print("Texto digitado: " .. Value)
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
  Default = false,
  Flag = "MyToggleFlag",
  Callback = function(Value)
    if Value then
      print("Toggle ativado!")
    else
      print("Toggle desativado!")
    end
  end
})

MainTab:AddSlider({
  Name = "Slider",
  Min = 1,
  Max = 10,
  Increase = 1,
  Default = 5,
  Flag = "MySliderFlag",
  Callback = function(Value)
    print("Valor do Slider: " .. Value)
  end
})

local Button = MainTab:AddButton({"botão"})

local Dropdown = MainTab:AddDropdown({
  Name = "nome do seu dropdown",
  Description = "",
  Options = {"um", "dois", "três"},
  Default = "um",
  Flag = "dropdown",
  Callback = function(Value)
    
  end
})

MainTab:AddTextBox({
  Name = "Name Item",
  Description = "1 Item on 1 Server",
  PlaceholderText = "Digite algo",
  Callback = function(Value)
    print("Texto digitado: " .. Value)
  end
})

```
