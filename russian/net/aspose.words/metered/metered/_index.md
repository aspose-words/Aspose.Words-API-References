---
title: Metered
linktitle: Metered
articleTitle: Metered
second_title: Aspose.Words для .NET
description: Metered строитель. Инициализирует новый экземпляр этого класса на С#.
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
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
