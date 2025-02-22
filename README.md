# Roblox_Lua_Line_chart_module
by:hahaxio7777(DC)
**(This file will have a display bug and will be fixed later)**

Used to create line charts

Usage:

1.Import

Example:
```
local ChartModule = loadstring(game:HttpGet("https://github.com/hisawg02/Roblox_Lua_Line_chart_module/raw/refs/heads/main/Main"))()
```

2.Initialization(ChartModule.CreateChart)

Parameters:

```ChartModule.CreateChart(<Frame>, <MaxInt>, <MinInt>, <Display range(-1 means infinite)>, <Text color(Color3.fromRGB)>, <Project table>)```

Project table Example:

```
{{"Item1",Color3.fromRGB(255, 0, 0),
{"Item2",Color3.fromRGB(0, 255, 0),
{"Item3",Color3.fromRGB(0, 0, 255) ,
}}
--Color3 = Line Color
--Can be expanded to unlimited}
```

Example:

```
local myChart = ChartModule.CreateChart(<Frame>, 100, 0, 10, Color3.fromRGB(0,255,0), 
{"Series1", Color3.fromRGB(255, 0, 0)},
	{"Series2", Color3.fromRGB(0, 255, 0)},
	{"Series3", Color3.fromRGB(0, 255, 255)},
	{"Series4", Color3.fromRGB(255, 255, 0)},
	{"Series5", Color3.fromRGB(255, 255, 255)})
```

3.Functions:

1.```updateChart(<table>)```:

table = Set the value of each item during initialization (latest)

Example:
```
  myChart:updateChart({
		{"Series1", 10},
		{"Series2", 20},
		{"Series3", 10 + 12},
		{"Series4", 10 - 2},
		{"Series5", 10 + 2 + math.random(1,10)},
	})
```

2.```changeChart(<MaxInt>,<MinInt>)```

You can set the vertical axis range

Example:

```
myChart:changeChart(120, -20)
```

3.```redrawChart()```:
Re-render a line chart

Example:
```
myChart:redrawChart()
```
