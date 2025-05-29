---
title: Font.Style
linktitle: Style
articleTitle: Style
second_title: Aspose.Words для .NET
description: Узнайте, как использовать свойство «Стиль шрифта» для настройки стилей символов в форматировании, чтобы повысить привлекательность и читабельность текста.
type: docs
weight: 410
url: /ru/net/aspose.words/font/style/
---
## Font.Style property

Возвращает или задает стиль символов, применяемый к данному форматированию.

```csharp
public Style Style { get; set; }
```

## Примеры

Применяет двойное подчеркивание ко всем фрагментам документа, отформатированным с использованием пользовательских стилей символов.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставьте пользовательский стиль и примените его к тексту, созданному с помощью конструктора документов.
Style style = doc.Styles.Add(StyleType.Character, "MyStyle");
style.Font.Color = Color.Red;
style.Font.Name = "Courier New";

builder.Font.StyleName = "MyStyle";
builder.Write("This text is in a custom style.");

// Повторяем каждый запуск и добавляем двойное подчеркивание к каждому пользовательскому стилю.
foreach (Run run in doc.GetChildNodes(NodeType.Run, true))
{
    Style charStyle = run.Font.Style;

    if (!charStyle.BuiltIn)
        run.Font.Underline = Underline.Double;
}

doc.Save(ArtifactsDir + "Font.Style.docx");
```

### Смотрите также

* class [Style](../../style/)
* class [Font](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
