---
title: ParagraphFormat.Style
linktitle: Style
articleTitle: Style
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ParagraphFormat Style, чтобы легко настраивать и улучшать стиль абзацев вашего документа для улучшения читаемости и представления.
type: docs
weight: 350
url: /ru/net/aspose.words/paragraphformat/style/
---
## ParagraphFormat.Style property

Возвращает или задает стиль абзаца, примененный к данному форматированию.

```csharp
public Style Style { get; set; }
```

## Примеры

Показывает, как создать и использовать стиль абзаца с форматированием списка.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Создать пользовательский стиль абзаца.
Style style = doc.Styles.Add(StyleType.Paragraph, "MyStyle1");
style.Font.Size = 24;
style.Font.Name = "Verdana";
style.ParagraphFormat.SpaceAfter = 12;

// Создайте список и убедитесь, что абзацы, использующие этот стиль, будут использовать этот список.
style.ListFormat.List = doc.Lists.Add(ListTemplate.BulletDefault);
style.ListFormat.ListLevelNumber = 0;

// Применяем стиль абзаца к текущему абзацу конструктора документа, а затем добавляем текст.
builder.ParagraphFormat.Style = style;
builder.Writeln("Hello World: MyStyle1, bulleted list.");

// Измените стиль конструктора документов на такой, который не имеет форматирования списка, и напишите еще один абзац.
builder.ParagraphFormat.Style = doc.Styles["Normal"];
builder.Writeln("Hello World: Normal.");

builder.Document.Save(ArtifactsDir + "Styles.ParagraphStyleBulletedList.docx");
```

### Смотрите также

* class [Style](../../style/)
* class [ParagraphFormat](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
