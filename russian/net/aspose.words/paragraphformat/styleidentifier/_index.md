---
title: ParagraphFormat.StyleIdentifier
linktitle: StyleIdentifier
articleTitle: StyleIdentifier
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ParagraphFormat StyleIdentifier, которое позволяет легко управлять стилями абзацев и настраивать их, улучшая форматирование и удобочитаемость документа.
type: docs
weight: 360
url: /ru/net/aspose.words/paragraphformat/styleidentifier/
---
## ParagraphFormat.StyleIdentifier property

Возвращает или задает независимый от локали идентификатор стиля абзаца, примененного к данному форматированию.

```csharp
public StyleIdentifier StyleIdentifier { get; set; }
```

## Примеры

Показывает, как вставить оглавление (TOC) в документ, используя стили заголовков в качестве записей.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставьте оглавление для первой страницы документа.
// Настройте таблицу для выбора абзацев с заголовками уровней 1–3.
// Также задайте его записи как гиперссылки, которые перенесут нас
// в место расположения заголовка при щелчке левой кнопкой мыши в Microsoft Word.
builder.InsertTableOfContents("\\o \"1-3\" \\h \\z \\u");
builder.InsertBreak(BreakType.PageBreak);

// Заполните оглавление, добавив абзацы со стилями заголовков.
// Каждый такой заголовок с уровнем от 1 до 3 создаст запись в таблице.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;
builder.Writeln("Heading 1.1");
builder.Writeln("Heading 1.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Writeln("Heading 2");
builder.Writeln("Heading 3");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;
builder.Writeln("Heading 3.1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading3;
builder.Writeln("Heading 3.1.1");
builder.Writeln("Heading 3.1.2");
builder.Writeln("Heading 3.1.3");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading4;
builder.Writeln("Heading 3.1.3.1");
builder.Writeln("Heading 3.1.3.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;
builder.Writeln("Heading 3.2");
builder.Writeln("Heading 3.3");

// Оглавление — это поле типа, которое необходимо обновить для отображения актуального результата.
doc.UpdateFields();
doc.Save(ArtifactsDir + "DocumentBuilder.InsertToc.docx");
```

### Смотрите также

* enum [StyleIdentifier](../../styleidentifier/)
* class [ParagraphFormat](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
