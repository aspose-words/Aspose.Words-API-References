---
title: Style.BaseStyleName
linktitle: BaseStyleName
articleTitle: BaseStyleName
second_title: Aspose.Words для .NET
description: Узнайте, как настроить свойство BaseStyleName для улучшения вашего дизайна. Легко получите или задайте имя стиля для улучшения визуальной привлекательности!
type: docs
weight: 30
url: /ru/net/aspose.words/style/basestylename/
---
## Style.BaseStyleName property

Получает/задает имя стиля, на котором основан этот стиль.

```csharp
public string BaseStyleName { get; set; }
```

## Примечания

Это будет пустая строка, если стиль не основан ни на каком другом стиле, и его можно установить в пустую строку.

## Примеры

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
