---
title: FieldOptions.FieldIndexFormat
linktitle: FieldIndexFormat
articleTitle: FieldIndexFormat
second_title: Aspose.Words для .NET
description: Узнайте, как использовать свойство FieldIndexFormat в FieldOptions для настройки форматирования FieldIndex с целью повышения ясности и организации документа.
type: docs
weight: 90
url: /ru/net/aspose.words.fields/fieldoptions/fieldindexformat/
---
## FieldOptions.FieldIndexFormat property

Получает или задает`FieldIndexFormat` что представляет форматирование для[`FieldIndex`](../../fieldindex/) поля в документе.

```csharp
public FieldIndexFormat FieldIndexFormat { get; set; }
```

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

* enum [FieldIndexFormat](../../fieldindexformat/)
* class [FieldOptions](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
