---
title: TxtLoadOptions.AutoNumberingDetection
linktitle: AutoNumberingDetection
articleTitle: AutoNumberingDetection
second_title: Aspose.Words для .NET
description: Откройте для себя свойство AutoNumberingDetection TxtLoadOptions. Легко включайте и отключайте автоматическую нумерацию для бесперебойной загрузки документов. Значение по умолчанию — true.
type: docs
weight: 20
url: /ru/net/aspose.words.loading/txtloadoptions/autonumberingdetection/
---
## TxtLoadOptions.AutoNumberingDetection property

Возвращает или задает логическое значение, указывающее, будет ли выполняться автоматическое определение нумерации при загрузке документа. Значение по умолчанию:`истинный` .

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
