---
title: DocumentBuilder.Italic
linktitle: Italic
articleTitle: Italic
second_title: Aspose.Words для .NET
description: Откройте для себя свойство DocumentBuilder Italic. Легко форматируйте текст курсивом для улучшения читаемости и стиля в ваших документах.
type: docs
weight: 140
url: /ru/net/aspose.words/documentbuilder/italic/
---
## DocumentBuilder.Italic property

True, если шрифт отформатирован как курсив.

```csharp
public bool Italic { get; set; }
```

## Примеры

Показывает, как заполнять поля MERGEFIELD данными с помощью конструктора документов вместо слияния почты.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставьте несколько MERGEFIELDS, которые принимают данные из столбцов с одинаковым именем в источнике данных во время слияния почты,
// а затем заполните их вручную.
builder.InsertField(" MERGEFIELD Chairman ");
builder.InsertField(" MERGEFIELD ChiefFinancialOfficer ");
builder.InsertField(" MERGEFIELD ChiefTechnologyOfficer ");

builder.MoveToMergeField("Chairman");
builder.Bold = true;
builder.Writeln("John Doe");

builder.MoveToMergeField("ChiefFinancialOfficer");
builder.Italic = true;
builder.Writeln("Jane Doe");

builder.MoveToMergeField("ChiefTechnologyOfficer");
builder.Italic = true;
builder.Writeln("John Bloggs");

doc.Save(ArtifactsDir + "DocumentBuilder.FillMergeFields.docx");
```

### Смотрите также

* class [DocumentBuilder](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
