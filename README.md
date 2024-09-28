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

**Как найти мои токены?** —
Вам нужно зайти в Services — Home — API

В коде вы найдете ваши токены

## Другие переменные
Тут будет ваш ключ, ключ следует вводить перед проверкой

```lua
local key = ""
```

## Функци проверки
Эти функци только осуществляют функцию проверки, а не саму проверку.
Для этого нужно использовать конструкцию **if**, про нее будет ниже

Проверка обычного ключа
```lua
KeyGuardLibrary.validateDefaultKey(key)
```

Проверка премиум ключа
```lua
KeyGuardLibrary.validatePremiumKey(key)
```

Эти проверки лучше использовать таким образом:
```lua
local response = KeyGuardLibrary.validateDefaultKey(key)
```
## Другие функции
Получение информации о сервисе
```lua
KeyGuardLibrary.validateDefaultKey(key)
```

Получение ссылки с указанием hwid
```lua
KeyGuardLibrary.getLink()
```
Например, можно использовать **setclipboard(KeyGuardLibrary.getLink())** — будет копировать ссылку в буфер обмена

## Проверка ключа
```lua
if response == trueData then
  print("Key is valid")
else
  print("Key is invalid")
end
```

Система будет проверять переменную **key**, и если такого ключа нет, или **hwid** ключа не будет совпадать с hwid игрока,
то система будет выдавать **Key is invalid**

В других случаях система будет выдавать **Key is valid**
