---
title: FieldIndexFormat Enum
linktitle: FieldIndexFormat
articleTitle: FieldIndexFormat
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.FieldIndexFormat для настраиваемого форматирования FieldIndex в ваших документах. Улучшите структуру вашего документа без усилий!
type: docs
weight: 2480
url: /ru/net/aspose.words.fields/fieldindexformat/
---
## FieldIndexFormat enumeration

Задает форматирование для[`FieldIndex`](../fieldindex/) поля в документе.

```csharp
public enum FieldIndexFormat
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Template | `0` | Из шаблона. |
| Classic | `1` | Классика. |
| Fancy | `2` | Изысканный. |
| Modern | `3` | Современный. |
| Bulleted | `4` | Маркированный. |
| Formal | `5` | Официально. |
| Simple | `6` | Простой. |

## Примеры

Показывает, как форматировать поля FieldIndex.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("A");
builder.InsertBreak(BreakType.LineBreak);
builder.InsertField("XE \"A\"");
builder.Write("B");

builder.InsertField(" INDEX \\e \" · \" \\h \"A\" \\c \"2\" \\z \"1033\"", null);

doc.FieldOptions.FieldIndexFormat = FieldIndexFormat.Fancy;
doc.UpdateFields();

doc.Save(ArtifactsDir + "Field.SetFieldIndexFormat.docx");
```

### Смотрите также

* пространство имен [Aspose.Words.Fields](../../aspose.words.fields/)
* сборка [Aspose.Words](../../)
