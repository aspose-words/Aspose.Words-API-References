---
title: StyleCollection.DefaultParagraphFormat
linktitle: DefaultParagraphFormat
articleTitle: DefaultParagraphFormat
second_title: Aspose.Words для .NET
description: Откройте для себя свойство StyleCollection DefaultParagraphFormat, чтобы легко получить доступ к форматированию абзацев по умолчанию в вашем документе и настроить его для повышения удобства чтения.
type: docs
weight: 30
url: /ru/net/aspose.words/stylecollection/defaultparagraphformat/
---
## StyleCollection.DefaultParagraphFormat property

Получает форматирование абзаца документа по умолчанию.

```csharp
public ParagraphFormat DefaultParagraphFormat { get; }
```

## Примечания

Обратите внимание, что значения по умолчанию для всего документа были введены в Microsoft Word 2007 и полностью поддерживаются в форматах OOXML (Docx) только. Более ранние форматы документов не поддерживают форматирование абзацев документа по умолчанию.

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

* class [ParagraphFormat](../../paragraphformat/)
* class [StyleCollection](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
