---
title: ParagraphFormat.Style
second_title: Справочник по API Aspose.Words для .NET
description: ParagraphFormat свойство. Получает или задает стиль абзаца применяемый к этому форматированию.
type: docs
weight: 330
url: /ru/net/aspose.words/paragraphformat/style/
---
## ParagraphFormat.Style property

Получает или задает стиль абзаца, применяемый к этому форматированию.

```csharp
public Style Style { get; set; }
```

### Примеры

Показывает, как создать и использовать стиль абзаца с форматированием списка.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Создать собственный стиль абзаца.
Style style = doc.Styles.Add(StyleType.Paragraph, "MyStyle1");
style.Font.Size = 24;
style.Font.Name = "Verdana";
style.ParagraphFormat.SpaceAfter = 12;

// Создайте список и убедитесь, что абзацы, использующие этот стиль, будут использовать этот список.
style.ListFormat.List = doc.Lists.Add(ListTemplate.BulletDefault);
style.ListFormat.ListLevelNumber = 0;

// Применяем стиль абзаца к текущему абзацу конструктора документов, а затем добавляем текст.
builder.ParagraphFormat.Style = style;
builder.Writeln("Hello World: MyStyle1, bulleted list.");

// Измените стиль построителя документа на стиль без форматирования списка и напишите еще один абзац.
builder.ParagraphFormat.Style = doc.Styles["Normal"];
builder.Writeln("Hello World: Normal.");

builder.Document.Save(ArtifactsDir + "Styles.ParagraphStyleBulletedList.docx");
```

### Смотрите также

* class [Style](../../style/)
* class [ParagraphFormat](../)
* пространство имен [Aspose.Words](../../paragraphformat/)
* сборка [Aspose.Words](../../../)


