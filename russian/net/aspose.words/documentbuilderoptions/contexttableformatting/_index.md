---
title: DocumentBuilderOptions.ContextTableFormatting
linktitle: ContextTableFormatting
articleTitle: ContextTableFormatting
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ContextTableFormatting в DocumentBuilderOptions. Убедитесь, что форматирование таблиц остается независимым, что повышает ясность и стиль вашего документа.
type: docs
weight: 20
url: /ru/net/aspose.words/documentbuilderoptions/contexttableformatting/
---
## DocumentBuilderOptions.ContextTableFormatting property

Истина, если форматирование, примененное к содержимому таблицы, не влияет на форматирование содержимого, которое следует за ней. Значение по умолчанию:`истинный` .

```csharp
public bool ContextTableFormatting { get; set; }
```

## Примеры

Показывает, как игнорировать форматирование таблицы для содержимого после.

```csharp
Document doc = new Document();
DocumentBuilderOptions builderOptions = new DocumentBuilderOptions();
builderOptions.ContextTableFormatting = true;
DocumentBuilder builder = new DocumentBuilder(doc, builderOptions);

// Добавляет содержимое перед таблицей.
// Размер шрифта по умолчанию — 12.
builder.Writeln("Font size 12 here.");
builder.StartTable();
builder.InsertCell();
// Изменяет размер шрифта внутри таблицы.
builder.Font.Size = 5;
builder.Write("Font size 5 here");
builder.InsertCell();
builder.Write("Font size 5 here");
builder.EndRow();
builder.EndTable();

// Если ContextTableFormatting имеет значение true, то форматирование таблицы не применяется к содержимому после.
// Если ContextTableFormatting имеет значение false, то форматирование таблицы применяется к содержимому после.
builder.Writeln("Font size 12 here.");

doc.Save(ArtifactsDir + "Table.ContextTableFormatting.docx");
```

### Смотрите также

* class [DocumentBuilderOptions](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
