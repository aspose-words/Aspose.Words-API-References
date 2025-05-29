---
title: MergeFormatMode Enum
linktitle: MergeFormatMode
articleTitle: MergeFormatMode
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.LowCode.MergeFormatMode для оптимизации слияния документов. Улучшите контроль форматирования при объединении нескольких файлов без усилий.
type: docs
weight: 4290
url: /ru/net/aspose.words.lowcode/mergeformatmode/
---
## MergeFormatMode enumeration

Указывает, как форматирование объединяется при объединении нескольких документов.

```csharp
public enum MergeFormatMode
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| MergeFormatting | `0` | Объединить форматирование объединенных документов. |
| KeepSourceFormatting | `1` | Означает, что исходный документ сохранит свое исходное форматирование, такое как стили шрифтов, размеры, цвета, отступы и любые другие элементы форматирования, примененные к его содержимому. |
| KeepSourceLayout | `2` | Сохраните макет исходных документов в конечном документе. |

## Примеры

Показывает, как объединить документы в один выходной документ.

```csharp
//Существует несколько способов объединения документов:
string inputDoc1 = MyDir + "Big document.docx";
string inputDoc2 = MyDir + "Tables.docx";

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.1.docx", new[] { inputDoc1, inputDoc2 });

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.2.docx", new[] { inputDoc1, inputDoc2 }, saveOptions, MergeFormatMode.KeepSourceFormatting);

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.3.pdf", new[] { inputDoc1, inputDoc2 }, SaveFormat.Pdf, MergeFormatMode.KeepSourceLayout);

LoadOptions firstLoadOptions = new LoadOptions() { IgnoreOleData = true };
LoadOptions secondLoadOptions = new LoadOptions() { IgnoreOleData = false };
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.4.docx", new[] { inputDoc1, inputDoc2 }, new[] { firstLoadOptions, secondLoadOptions }, saveOptions, MergeFormatMode.KeepSourceFormatting);

Document doc = Merger.Merge(new[] { inputDoc1, inputDoc2 }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.5.docx");

doc = Merger.Merge(new[] { inputDoc1, inputDoc2 }, new[] { firstLoadOptions, secondLoadOptions }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.6.docx");
```

### Смотрите также

* пространство имен [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../)
