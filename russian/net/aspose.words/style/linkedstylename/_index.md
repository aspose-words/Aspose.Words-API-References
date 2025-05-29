---
title: Style.LinkedStyleName
linktitle: LinkedStyleName
articleTitle: LinkedStyleName
second_title: Aspose.Words для .NET
description: Узнайте, как стилизовать свойство LinkedStyleName, легко управлять связанными стилями и улучшить рабочий процесс проектирования с помощью бесшовной интеграции.
type: docs
weight: 90
url: /ru/net/aspose.words/style/linkedstylename/
---
## Style.LinkedStyleName property

Получает/устанавливает имя[`Style`](../) связан с этим. Возвращает пустую строку, если ни один стиль не связан.

```csharp
public string LinkedStyleName { get; set; }
```

## Примечания

Разрешается только связывать стиль абзаца со стилем символа и наоборот.

Установка LinkedStyleName для текущего стиля автоматически приводит к установке LinkedStyleName для связанного стиля.

Назначение пустой строки эквивалентно отмене привязки ранее связанного стиля.

## Примеры

Показывает, как связывать стили между собой.

```csharp
Document doc = new Document();

Style styleHeading1 = doc.Styles[StyleIdentifier.Heading1];

Style styleHeading1Char = doc.Styles.Add(StyleType.Character, "Heading 1 Char");
styleHeading1Char.Font.Name = "Verdana";
styleHeading1Char.Font.Bold = true;
styleHeading1Char.Font.Border.LineStyle = LineStyle.Dot;
styleHeading1Char.Font.Border.LineWidth = 15;

styleHeading1.LinkedStyleName = "Heading 1 Char";

Assert.AreEqual("Heading 1 Char", styleHeading1.LinkedStyleName);
Assert.AreEqual("Heading 1", styleHeading1Char.LinkedStyleName);
```

Показывает, как использовать псевдонимы стилей.

```csharp
Document doc = new Document(MyDir + "Style with alias.docx");

// Этот документ содержит стиль с именем "MyStyle,MyStyle Alias 1,MyStyle Alias 2".
// Если имя стиля имеет несколько значений, разделенных запятыми, каждое предложение является отдельным псевдонимом.
Style style = doc.Styles["MyStyle"];
Assert.AreEqual(new [] { "MyStyle Alias 1", "MyStyle Alias 2" }, style.Aliases);
Assert.AreEqual("Title", style.BaseStyleName);
Assert.AreEqual("MyStyle Char", style.LinkedStyleName);

// Мы можем ссылаться на стиль, используя его псевдоним, а также его имя.
Assert.AreEqual(doc.Styles["MyStyle Alias 1"], doc.Styles["MyStyle Alias 2"]);

DocumentBuilder builder = new DocumentBuilder(doc);
builder.MoveToDocumentEnd();
builder.ParagraphFormat.Style = doc.Styles["MyStyle Alias 1"];
builder.Writeln("Hello world!");
builder.ParagraphFormat.Style = doc.Styles["MyStyle Alias 2"];
builder.Write("Hello again!");

Assert.AreEqual(doc.FirstSection.Body.Paragraphs[0].ParagraphFormat.Style, 
    doc.FirstSection.Body.Paragraphs[1].ParagraphFormat.Style);
```

### Смотрите также

* class [Style](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
