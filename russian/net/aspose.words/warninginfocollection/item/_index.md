---
title: WarningInfoCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words для .NET
description: Получите доступ к определенным элементам WarningInfoCollection без усилий по индексу. Оптимизируйте управление данными с помощью нашей интуитивной функции свойств!
type: docs
weight: 30
url: /ru/net/aspose.words/warninginfocollection/item/
---
## WarningInfoCollection indexer

Получает элемент по указанному индексу.

```csharp
public WarningInfo this[int index] { get; }
```

| Параметр | Описание |
| --- | --- |
| index | Индекс элемента, отсчитываемый от нуля. |

## Примеры

Показывает, как получать предупреждения о неподдерживаемых форматах.

```csharp
WarningInfoCollection warnings = new WarningInfoCollection();
Document doc = new Document(MyDir + "FB2 document.fb2", new LoadOptions { WarningCallback = warnings });

Assert.AreEqual("The original file load format is FB2, which is not supported by Aspose.Words. The file is loaded as an XML document.", warnings[0].Description);
Assert.AreEqual(1, warnings.Count);
```

### Смотрите также

* class [WarningInfo](../../warninginfo/)
* class [WarningInfoCollection](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
