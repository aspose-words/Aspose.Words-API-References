---
title: Metered Class
linktitle: Metered
articleTitle: Metered
second_title: Aspose.Words для .NET
description: Откройте для себя мощь класса Aspose.Words.Metered! Легко управляйте своим лимитированным ключом с помощью эффективных методов для бесперебойной обработки документов.
type: docs
weight: 4850
url: /ru/net/aspose.words/metered/
---
## Metered class

Предоставляет методы для установки измеренного ключа.

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
| [GetProductName](../../aspose.words/metered/getproductname/)() | Возврат Название продукта |
| [SetMeteredKey](../../aspose.words/metered/setmeteredkey/)(*string, string*) | Устанавливает измеренный открытый и закрытый ключ. Если вы приобрели измеренную лицензию, при запуске приложения следует вызвать этот API, обычно этого достаточно. Однако, если постоянно не удается загрузить данные о потреблении и истекает 24 часа, лицензия будет переведена в статус оценки, Чтобы избежать этого, следует регулярно проверять статус лицензии, если это статус оценки, снова вызвать этот API. |
| static [GetConsumptionCredit](../../aspose.words/metered/getconsumptioncredit/)() | Получает потребительский кредит |
| static [GetConsumptionQuantity](../../aspose.words/metered/getconsumptionquantity/)() | Получает файл потребления size |
| static [IsMeteredLicensed](../../aspose.words/metered/ismeteredlicensed/)() | Проверьте, лицензирован ли счетчик |

## Примеры

В этом примере будет сделана попытка установить измеренный открытый и закрытый ключ

```csharp
[C#]

Metered matered = new Metered();
matered.SetMeteredKey("PublicKey", "PrivateKey");


[Visual Basic]

Dim matered As Metered = New Metered
matered.SetMeteredKey("PublicKey", "PrivateKey")
```

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

* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)
