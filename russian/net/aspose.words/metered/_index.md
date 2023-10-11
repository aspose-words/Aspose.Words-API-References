---
title: Class Metered
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Metered сорт. Предоставляет методы для установки дозированного ключа.
type: docs
weight: 4160
url: /ru/net/aspose.words/metered/
---
## Metered class

Предоставляет методы для установки дозированного ключа.

Чтобы узнать больше, посетите[Лицензирование и подписка](https://docs.aspose.com/words/net/licensing/) статья документации.

```csharp
public class Metered
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [Metered](metered/)() | Инициализирует новый экземпляр этого класса. |

## Методы

| Имя | Описание |
| --- | --- |
| [SetMeteredKey](../../aspose.words/metered/setmeteredkey/)(string, string) | Устанавливает лимитированный открытый и закрытый ключ. Если вы приобретаете лимитированную лицензию, при запуске приложения этот API должен вызываться, обычно этого достаточно. Однако, если всегда не удается загрузить данные о потреблении и превышает 24 часа, лицензия будет переведена в оценочный статус, , чтобы избежать такого случая, вам следует регулярно проверять статус лицензии. Если это оценочный статус, вызовите этот API еще раз. |
| static [GetConsumptionCredit](../../aspose.words/metered/getconsumptioncredit/)() | Получает потребительский кредит |
| static [GetConsumptionQuantity](../../aspose.words/metered/getconsumptionquantity/)() | Получает файл потребления size |

### Примеры

В этом примере будет предпринята попытка установить дозированный открытый и закрытый ключ

```csharp
[C#]

Metered matered = new Metered();
matered.SetMeteredKey("PublicKey", "PrivateKey");


[Visual Basic]

Dim matered As Metered = New Metered
matered.SetMeteredKey("PublicKey", "PrivateKey")
```

Показывает, как активировать дозированную лицензию и отслеживать кредит/потребление.

```csharp
// Создайте новую дозированную лицензию и распечатайте статистику ее использования.
Metered metered = new Metered();
metered.SetMeteredKey("MyPublicKey", "MyPrivateKey");

Console.WriteLine($"Credit before operation: {Metered.GetConsumptionCredit()}");
Console.WriteLine($"Consumption quantity before operation: {Metered.GetConsumptionQuantity()}");

// Работаем с помощью Aspose.Words, а затем снова распечатываем измеренную статистику, чтобы увидеть, сколько мы потратили.
Document doc = new Document(MyDir + "Document.docx");
doc.Save(ArtifactsDir + "Metered.Usage.pdf");

// Поскольку механизм дозированного лицензирования не отправляет данные об использовании на сервер покупки каждый раз,
// вам нужно использовать ожидание.
System.Threading.Thread.Sleep(10000);

Console.WriteLine($"Credit after operation: {Metered.GetConsumptionCredit()}");
Console.WriteLine($"Consumption quantity after operation: {Metered.GetConsumptionQuantity()}");
```

### Смотрите также

* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)


