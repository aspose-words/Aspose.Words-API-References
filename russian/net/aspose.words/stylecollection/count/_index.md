---
title: StyleCollection.Count
second_title: Справочник по API Aspose.Words для .NET
description: StyleCollection свойство. Получает количество стилей в коллекции.
type: docs
weight: 10
url: /ru/net/aspose.words/stylecollection/count/
---
## StyleCollection.Count property

Получает количество стилей в коллекции.

```csharp
public int Count { get; }
```

### Примеры

Показывает, как добавить стиль в коллекцию стилей документа.

```csharp
Document doc = new Document();

StyleCollection styles = doc.Styles;
// Устанавливаем параметры по умолчанию для новых стилей, которые мы можем позже добавить в эту коллекцию.
styles.DefaultFont.Name = "Courier New";
// Если мы добавим стиль StyleType.Paragraph, коллекция применит значения
// его свойство "DefaultParagraphFormat" к свойству стиля "ParagraphFormat".
styles.DefaultParagraphFormat.FirstLineIndent = 15.0;
// Добавляем стиль и проверяем, что для него заданы настройки по умолчанию.
styles.Add(StyleType.Paragraph, "MyStyle");

Assert.AreEqual("Courier New", styles[4].Font.Name);
Assert.AreEqual(15.0, styles["MyStyle"].ParagraphFormat.FirstLineIndent);
```

### Смотрите также

* class [StyleCollection](../)
* пространство имен [Aspose.Words](../../stylecollection/)
* сборка [Aspose.Words](../../../)


