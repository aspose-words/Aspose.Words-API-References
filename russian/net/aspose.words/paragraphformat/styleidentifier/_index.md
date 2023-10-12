---
title: ParagraphFormat.StyleIdentifier
second_title: Справочник по API Aspose.Words для .NET
description: ParagraphFormat свойство. Получает или задает независимый от локали идентификатор стиля абзаца примененного к этому форматированию.
type: docs
weight: 350
url: /ru/net/aspose.words/paragraphformat/styleidentifier/
---
## ParagraphFormat.StyleIdentifier property

Получает или задает независимый от локали идентификатор стиля абзаца, примененного к этому форматированию.

```csharp
public StyleIdentifier StyleIdentifier { get; set; }
```

### Примеры

Показывает, как вставить оглавление (TOC) в документ, используя стили заголовков в качестве записей.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставляем оглавление первой страницы документа.
// Настройте таблицу так, чтобы она подбирала абзацы с заголовками уровней от 1 до 3.
// Также сделайте его записи гиперссылками, которые приведут нас
// к местоположению заголовка при щелчке левой кнопкой мыши в Microsoft Word.
builder.InsertTableOfContents("\\o \"1-3\" \\h \\z \\u");
builder.InsertBreak(BreakType.PageBreak);

// Заполняем оглавление, добавляя абзацы со стилями заголовков.
// Каждый такой заголовок уровня от 1 до 3 создаст запись в таблице.
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

// Оглавление — это поле типа, которое необходимо обновить, чтобы отобразить актуальный результат.
doc.UpdateFields();
doc.Save(ArtifactsDir + "DocumentBuilder.InsertToc.docx");
```

### Смотрите также

* enum [StyleIdentifier](../../styleidentifier/)
* class [ParagraphFormat](../)
* пространство имен [Aspose.Words](../../paragraphformat/)
* сборка [Aspose.Words](../../../)


