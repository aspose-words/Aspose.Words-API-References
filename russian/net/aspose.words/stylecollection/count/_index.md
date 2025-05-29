---
title: StyleCollection.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words для .NET
description: Откройте для себя свойство StyleCollection Count, чтобы легко получить общее количество стилей в вашей коллекции для улучшенной организации и управления.
type: docs
weight: 10
url: /ru/net/aspose.words/stylecollection/count/
---
## StyleCollection.Count property

Получает количество стилей в коллекции.

```csharp
public int Count { get; }
```

## Примеры

Показывает, как добавить стиль в коллекцию стилей документа.

```csharp
Document doc = new Document();

StyleCollection styles = doc.Styles;
// Устанавливаем параметры по умолчанию для новых стилей, которые мы позже можем добавить в эту коллекцию.
styles.DefaultFont.Name = "Courier New";
// Если мы добавим стиль "StyleType.Paragraph", коллекция применит значения
// его свойство "DefaultParagraphFormat" к свойству "ParagraphFormat" стиля.
styles.DefaultParagraphFormat.FirstLineIndent = 15.0;
// Добавьте стиль, а затем проверьте, что у него настройки по умолчанию.
styles.Add(StyleType.Paragraph, "MyStyle");

Assert.AreEqual("Courier New", styles[4].Font.Name);
Assert.AreEqual(15.0, styles["MyStyle"].ParagraphFormat.FirstLineIndent);
```

### Смотрите также

* class [StyleCollection](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
