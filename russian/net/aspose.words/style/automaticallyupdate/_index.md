---
title: Style.AutomaticallyUpdate
linktitle: AutomaticallyUpdate
articleTitle: AutomaticallyUpdate
second_title: Aspose.Words для .NET
description: Узнайте, как свойство AutomaticallyUpdate улучшает ваши стили, автоматически переопределяя их для оптимальной ценности и производительности в ваших проектах.
type: docs
weight: 20
url: /ru/net/aspose.words/style/automaticallyupdate/
---
## Style.AutomaticallyUpdate property

Указывает, будет ли этот стиль автоматически переопределяться на основе соответствующего значения.

```csharp
public bool AutomaticallyUpdate { get; set; }
```

## Примечания

Если значение свойства установлено равным true, MS Word автоматически переопределяет текущий стиль, когда изменяется соответствующее форматирование абзаца.

Свойство AutomaticallyUpdate применимо только к стилям абзацев.

Значение по умолчанию:`ЛОЖЬ`.

## Примеры

Показывает, как создать и применить пользовательский стиль.

```csharp
Document doc = new Document();

Style style = doc.Styles.Add(StyleType.Paragraph, "MyStyle");
style.Font.Name = "Times New Roman";
style.Font.Size = 16;
style.Font.Color = Color.Navy;
// Автоматически переопределить стиль.
style.AutomaticallyUpdate = true;

DocumentBuilder builder = new DocumentBuilder(doc);

// Применить один из стилей документа к абзацу, создаваемому конструктором документа.
builder.ParagraphFormat.Style = doc.Styles["MyStyle"];
builder.Writeln("Hello world!");

Style firstParagraphStyle = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Style;

Assert.AreEqual(style, firstParagraphStyle);

// Удаляем наш пользовательский стиль из коллекции стилей документа.
doc.Styles["MyStyle"].Remove();

firstParagraphStyle = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Style;

// Любой текст, в котором использовался удаленный стиль, возвращается к форматированию по умолчанию.
Assert.False(doc.Styles.Any(s => s.Name == "MyStyle"));
Assert.AreEqual("Times New Roman", firstParagraphStyle.Font.Name);
Assert.AreEqual(12.0d, firstParagraphStyle.Font.Size);
Assert.AreEqual(Color.Empty.ToArgb(), firstParagraphStyle.Font.Color.ToArgb());
```

### Смотрите также

* class [Style](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
