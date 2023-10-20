---
title: JustificationMode Enum
linktitle: JustificationMode
articleTitle: JustificationMode
second_title: Aspose.Words для .NET
description: Aspose.Words.Settings.JustificationMode перечисление. Указывает настройку межсимвольного интервала для документа. Значение по умолчаниюРасширять  на С#.
type: docs
weight: 5800
url: /ru/net/aspose.words.settings/justificationmode/
---
## JustificationMode enumeration

Указывает настройку межсимвольного интервала для документа. Значение по умолчанию:`Расширять` .

```csharp
public enum JustificationMode
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Expand | `0` |  |
| Compress | `1` |  |
| CompressKana | `2` |  |

## Примеры

Показывает, как управлять интервалом между символами.

```csharp
Document doc = new Document(MyDir + "Document.docx");

JustificationMode justificationMode = doc.JustificationMode;
if (justificationMode == JustificationMode.Expand)                
    doc.JustificationMode = JustificationMode.Compress;

doc.Save(ArtifactsDir + "Document.SetJustificationMode.docx");
```

### Смотрите также

* пространство имен [Aspose.Words.Settings](../../aspose.words.settings/)
* сборка [Aspose.Words](../../)
