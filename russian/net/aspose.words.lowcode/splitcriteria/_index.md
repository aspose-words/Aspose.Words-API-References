---
title: SplitCriteria Enum
linktitle: SplitCriteria
articleTitle: SplitCriteria
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.LowCode.SplitCriteria для эффективного разделения документов. Оптимизируйте свой рабочий процесс с помощью универсальных опций для бесшовного управления частями.
type: docs
weight: 4400
url: /ru/net/aspose.words.lowcode/splitcriteria/
---
## SplitCriteria enumeration

Указывает, как документ делится на части.

```csharp
public enum SplitCriteria
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Page | `0` | Указывает, что документ разделен на страницы. |
| SectionBreak | `1` | Указывает, что документ разделен на части по разрыву раздела любого типа. |
| Style | `2` | Указывает, что документ разделен на части по абзацу, отформатированные с использованием стиля, указанного в[`SplitStyle`](../splitoptions/splitstyle/) . |

## Примеры

Показывает, как разделить документ по страницам.

```csharp
string doc = MyDir + "Big document.docx";

SplitOptions options = new SplitOptions();
options.SplitCriteria = SplitCriteria.Page;
Splitter.Split(doc, ArtifactsDir + "LowCode.SplitDocument.1.docx", options);
Splitter.Split(doc, ArtifactsDir + "LowCode.SplitDocument.2.docx", SaveFormat.Docx, options);
```

### Смотрите также

* пространство имен [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../)
