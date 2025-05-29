---
title: Metered.IsMeteredLicensed
linktitle: IsMeteredLicensed
articleTitle: IsMeteredLicensed
second_title: Aspose.Words для .NET
description: Узнайте, лицензирован ли ваш метод измерения с помощью IsMetered. Обеспечьте соответствие и откройте для себя преимущества лицензированных услуг сегодня!
type: docs
weight: 60
url: /ru/net/aspose.words/metered/ismeteredlicensed/
---
## Metered.IsMeteredLicensed method

Проверьте, лицензирован ли счетчик

```csharp
public static bool IsMeteredLicensed()
```

### Возвращаемое значение

Правда или ложь

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
