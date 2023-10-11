---
title: Metered.GetConsumptionQuantity
second_title: Справочник по API Aspose.Words для .NET
description: Metered метод. Получает файл потребления size
type: docs
weight: 40
url: /ru/net/aspose.words/metered/getconsumptionquantity/
---
## Metered.GetConsumptionQuantity method

Получает файл потребления size

```csharp
public static decimal GetConsumptionQuantity()
```

### Возвращаемое значение

объем потребления

### Примеры

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

* class [Metered](../)
* пространство имен [Aspose.Words](../../metered/)
* сборка [Aspose.Words](../../../)


