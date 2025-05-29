---
title: Metered.GetConsumptionCredit
linktitle: GetConsumptionCredit
articleTitle: GetConsumptionCredit
second_title: Aspose.Words для .NET
description: Откройте для себя экономию с помощью метода Metered GetConsumptionCredit — эффективно извлекайте кредиты на потребление для более разумного управления энергопотреблением.
type: docs
weight: 40
url: /ru/net/aspose.words/metered/getconsumptioncredit/
---
## Metered.GetConsumptionCredit method

Получает потребительский кредит

```csharp
public static decimal GetConsumptionCredit()
```

### Возвращаемое значение

количество потребления

## Примеры

Показывает, как активировать измерительную лицензию и отслеживать кредит/потребление.

```csharp
// Создайте новую измеренную лицензию, а затем распечатайте статистику ее использования.
Metered metered = new Metered();
metered.SetMeteredKey("MyPublicKey", "MyPrivateKey");

Console.WriteLine($"Is metered license accepted: {Metered.IsMeteredLicensed()}");
Console.WriteLine($"Product name: {metered.GetProductName()}");
Console.WriteLine($"Credit before operation: {Metered.GetConsumptionCredit()}");
Console.WriteLine($"Consumption quantity before operation: {Metered.GetConsumptionQuantity()}");

// Работаем с Aspose.Words, а затем снова выводим нашу измеренную статистику, чтобы увидеть, сколько мы потратили.
Document doc = new Document(MyDir + "Document.docx");
doc.Save(ArtifactsDir + "Metered.Usage.pdf");

// Механизм лицензирования Aspose Metered не отправляет данные об использовании на сервер покупок каждый раз,
// вам нужно использовать ожидание.
System.Threading.Thread.Sleep(10000);

Console.WriteLine($"Credit after operation: {Metered.GetConsumptionCredit()}");
Console.WriteLine($"Consumption quantity after operation: {Metered.GetConsumptionQuantity()}");
```

### Смотрите также

* class [Metered](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
