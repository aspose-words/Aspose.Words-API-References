---
title: Metered.SetMeteredKey
linktitle: SetMeteredKey
articleTitle: SetMeteredKey
second_title: Aspose.Words для .NET
description: Легко управляйте вашей измеренной лицензией с помощью метода SetMeteredKey. Обеспечьте бесперебойную загрузку данных и избегайте статуса оценки с помощью регулярных проверок.
type: docs
weight: 30
url: /ru/net/aspose.words/metered/setmeteredkey/
---
## Metered.SetMeteredKey method

Устанавливает измеренный открытый и закрытый ключ. Если вы приобрели измеренную лицензию, при запуске приложения следует вызвать этот API, обычно этого достаточно. Однако, если постоянно не удается загрузить данные о потреблении и истекает 24 часа, лицензия будет переведена в статус оценки, Чтобы избежать этого, следует регулярно проверять статус лицензии, если это статус оценки, снова вызвать этот API.

```csharp
public void SetMeteredKey(string publicKey, string privateKey)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| publicKey | String | открытый ключ |
| privateKey | String | закрытый ключ |

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
