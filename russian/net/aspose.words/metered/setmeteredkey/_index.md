---
title: Metered.SetMeteredKey
second_title: Справочник по API Aspose.Words для .NET
description: Metered метод. Устанавливает лимитированный открытый и закрытый ключ. Если вы приобретаете лимитированную лицензию при запуске приложения этот API должен вызываться обычно этого достаточно. Однако если всегда не удается загрузить данные о потреблении и превышает 24 часа лицензия будет переведена в оценочный статус  чтобы избежать такого случая вам следует регулярно проверять статус лицензии. Если это оценочный статус вызовите этот API еще раз.
type: docs
weight: 20
url: /ru/net/aspose.words/metered/setmeteredkey/
---
## Metered.SetMeteredKey method

Устанавливает лимитированный открытый и закрытый ключ. Если вы приобретаете лимитированную лицензию, при запуске приложения этот API должен вызываться, обычно этого достаточно. Однако, если всегда не удается загрузить данные о потреблении и превышает 24 часа, лицензия будет переведена в оценочный статус, , чтобы избежать такого случая, вам следует регулярно проверять статус лицензии. Если это оценочный статус, вызовите этот API еще раз.

```csharp
public void SetMeteredKey(string publicKey, string privateKey)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| publicKey | String | открытый ключ |
| privateKey | String | закрытый ключ |

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


