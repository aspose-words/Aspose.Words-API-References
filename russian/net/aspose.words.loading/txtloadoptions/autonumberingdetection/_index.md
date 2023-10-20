---
title: TxtLoadOptions.AutoNumberingDetection
linktitle: AutoNumberingDetection
articleTitle: AutoNumberingDetection
second_title: Aspose.Words для .NET
description: TxtLoadOptions AutoNumberingDetection свойство. Получает или задает логическое значение указывающее что при загрузке документа будет выполняться автоматическое обнаружение нумерации . Значение по умолчаниюистинный  на С#.
type: docs
weight: 20
url: /ru/net/aspose.words.loading/txtloadoptions/autonumberingdetection/
---
## TxtLoadOptions.AutoNumberingDetection property

Получает или задает логическое значение, указывающее, что при загрузке документа будет выполняться автоматическое обнаружение нумерации . Значение по умолчанию:`истинный` .

```csharp
public bool AutoNumberingDetection { get; set; }
```

## Примеры

Показывает, как отключить автоматическое определение нумерации.

```csharp
TxtLoadOptions options = new TxtLoadOptions { AutoNumberingDetection = false };
Document doc = new Document(MyDir + "Number detection.txt", options);
```

### Смотрите также

* class [TxtLoadOptions](../)
* пространство имен [Aspose.Words.Loading](../../../aspose.words.loading/)
* сборка [Aspose.Words](../../../)
