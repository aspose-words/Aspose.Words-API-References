---
title: Style.Remove
linktitle: Remove
articleTitle: Remove
second_title: Aspose.Words для .NET
description: Без усилий удалите нежелательные стили из вашего документа с помощью метода Style Remove. Улучшите внешний вид вашего контента и поддерживайте его согласованность!
type: docs
weight: 230
url: /ru/net/aspose.words/style/remove/
---
## Style.Remove method

Удаляет указанный стиль из документа.

```csharp
public void Remove()
```

## Примечания

Удаление стиля оказывает следующее влияние на модель документа:

* Все ссылки на стиль удаляются из соответствующих абзацев, разделов и таблиц.
* Если базовый стиль удален, его форматирование переносится в дочерние стили.
* Если удаляемый стиль имеет связанный стиль, то удаляются оба стиля.

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
