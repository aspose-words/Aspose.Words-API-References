---
title: Style.Font
linktitle: Font
articleTitle: Font
second_title: Aspose.Words для .NET
description: Style Font свойство. Получает форматирование символов стиля на С#.
type: docs
weight: 60
url: /ru/net/aspose.words/style/font/
---
## Style.Font property

Получает форматирование символов стиля.

```csharp
public Font Font { get; }
```

## Примечания

Для стилей списков это свойство возвращает`нулевой`.

## Примеры

Показывает, как создать и использовать стиль абзаца с форматированием списка.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Создаем собственный стиль абзаца.
Style style = doc.Styles.Add(StyleType.Paragraph, "MyStyle1");
style.Font.Size = 24;
style.Font.Name = "Verdana";
style.ParagraphFormat.SpaceAfter = 12;

// Создайте список и убедитесь, что абзацы, использующие этот стиль, будут использовать этот список.
style.ListFormat.List = doc.Lists.Add(ListTemplate.BulletDefault);
style.ListFormat.ListLevelNumber = 0;

// Примените стиль абзаца к текущему абзацу конструктора документов, а затем добавьте текст.
builder.ParagraphFormat.Style = style;
builder.Writeln("Hello World: MyStyle1, bulleted list.");

// Измените стиль компоновщика документов на стиль без форматирования списка и напишите еще один абзац.
builder.ParagraphFormat.Style = doc.Styles["Normal"];
builder.Writeln("Hello World: Normal.");

builder.Document.Save(ArtifactsDir + "Styles.ParagraphStyleBulletedList.docx");
```

Показывает, как создать и применить собственный стиль.

```csharp
Document doc = new Document();

Style style = doc.Styles.Add(StyleType.Paragraph, "MyStyle");
style.Font.Name = "Times New Roman";
style.Font.Size = 16;
style.Font.Color = Color.Navy;
// Автоматически переопределить стиль.
style.AutomaticallyUpdate = true;

DocumentBuilder builder = new DocumentBuilder(doc);

// Применяем один из стилей документа к абзацу, который создает конструктор документов.
builder.ParagraphFormat.Style = doc.Styles["MyStyle"];
builder.Writeln("Hello world!");

Style firstParagraphStyle = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Style;

Assert.AreEqual(style, firstParagraphStyle);

// Удаляем наш собственный стиль из коллекции стилей документа.
doc.Styles["MyStyle"].Remove();

firstParagraphStyle = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Style;

// Любой текст, в котором использовался удаленный стиль, возвращается к форматированию по умолчанию.
Assert.False(doc.Styles.Any(s => s.Name == "MyStyle"));
Assert.AreEqual("Times New Roman", firstParagraphStyle.Font.Name);
Assert.AreEqual(12.0d, firstParagraphStyle.Font.Size);
Assert.AreEqual(Color.Empty.ToArgb(), firstParagraphStyle.Font.Color.ToArgb());
```

### Смотрите также

* class [Font](../../font/)
* class [Style](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
