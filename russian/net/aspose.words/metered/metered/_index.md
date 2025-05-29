---
title: Metered
linktitle: Metered
articleTitle: Metered
second_title: Aspose.Words для .NET
description: Откройте для себя наш конструктор с измерением для эффективной инициализации экземпляра. Оптимизируйте процесс кодирования с оптимизированной производительностью и улучшенной функциональностью.
type: docs
weight: 10
url: /ru/net/aspose.words/metered/metered/
---
## Metered constructor

Инициализирует новый экземпляр этого класса.

```csharp
public Metered()
```

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
