# Better Derma Grid
Replacement for Gmod's DIconLayout that isn't buggy and hard to use

# Installation
Put it in clientside autorun

# Usage

Initialize the panel, and set its columns - the amount of columns will dictate how many items are on each row.
```lua
local grid = vgui.Create("ThreesGrid")
grid:SetColumns(3)
```

Add cells to the grid, all you need to do is set the panel's height, every panel in a row will take the height of its tallest child 
```lua
local pnl = vgui.Create("DPanel")
pnl:SetTall(100)
grid:AddCell(pnl)
```

# Spacing
Want spacing between your grid cells?
```lua
grid:SetHorizontalMargin(5) //5 pixels of space between each item on a row, horizontally
grid:SetVerticalMargin(10) //10 pixels of space between each row, vertically
```

# Clearing
You can get rid of everything in a grid by using:
```lua
grid:Clear()
```

# Misc
Normally, adding cells to the table goes on a left to right, top to down basis, so if you want to add a completely empty cell for spacing reasons or whatever, you can use:
```lua
grid:Skip()
```
