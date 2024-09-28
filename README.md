# KeyGuardian Api Documentation Ru

(Тут будет рассказ про api)

## Импортирование библиотеки

```lua
local KeyGuardLibrary = loadstring(game:HttpGet("https://cdn.keyguardian.org/library/v1.0.0.lua"))
```

## Базовые переменные

```lua
local TrueData = "e2f5d88ee72f444aa5952b3d3b19e015"
local FalseData = "158c11d003904547ae3cbff92a78407a"
```

## Настройка

```lua
KeyGuardLibrary.Set({
  publicToken = "ВашПубличныйТокен",
  privateToken = "ВашПриватныйТокен",
  trueData = TrueData,
  falseData = FalseData,
})
```

## Другие переменные
Тут будет ваш ключ, ключ следует вводить перед проверкой

```lua
local key = ""
```
