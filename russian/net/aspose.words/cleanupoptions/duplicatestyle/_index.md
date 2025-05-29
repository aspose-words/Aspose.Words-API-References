---
title: CleanupOptions.DuplicateStyle
linktitle: DuplicateStyle
articleTitle: DuplicateStyle
second_title: Aspose.Words для .NET
description: Оптимизируйте свои документы с помощью свойства CleanupOptions DuplicateStyle — легко удаляйте дублирующиеся стили для более чистого и эффективного форматирования. Значение по умолчанию — false.
type: docs
weight: 20
url: /ru/net/aspose.words/cleanupoptions/duplicatestyle/
---
## CleanupOptions.DuplicateStyle property

Возвращает/устанавливает флаг, указывающий, следует ли удалять дублирующиеся стили из документа. Значение по умолчанию:`ЛОЖЬ` .

```csharp
public bool DuplicateStyle { get; set; }
```

## Примеры

Показывает, как удалить дублирующиеся стили из документа.

```csharp
Document doc = new Document();

// Добавляем в документ два стиля с идентичными свойствами,
// но разные имена. Второй стиль считается дубликатом первого.
Style myStyle = doc.Styles.Add(StyleType.Paragraph, "MyStyle1");
myStyle.Font.Size = 14;
myStyle.Font.Name = "Courier New";
myStyle.Font.Color = Color.Blue;

Style duplicateStyle = doc.Styles.Add(StyleType.Paragraph, "MyStyle2");
duplicateStyle.Font.Size = 14;
duplicateStyle.Font.Name = "Courier New";
duplicateStyle.Font.Color = Color.Blue;

Assert.AreEqual(6, doc.Styles.Count);

// Применить оба стиля к разным абзацам документа.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.ParagraphFormat.StyleName = myStyle.Name;
builder.Writeln("Hello world!");

builder.ParagraphFormat.StyleName = duplicateStyle.Name;
builder.Writeln("Hello again!");

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

Assert.AreEqual(myStyle, paragraphs[0].ParagraphFormat.Style);
Assert.AreEqual(duplicateStyle, paragraphs[1].ParagraphFormat.Style);

// Настройте объект CleanOptions, затем вызовите метод Cleanup для замены всех дублирующихся стилей
// с оригиналом и удалить дубликаты из документа.
CleanupOptions cleanupOptions = new CleanupOptions { DuplicateStyle = true };

doc.Cleanup(cleanupOptions);

Assert.AreEqual(5, doc.Styles.Count);
Assert.AreEqual(myStyle, paragraphs[0].ParagraphFormat.Style);
Assert.AreEqual(myStyle, paragraphs[1].ParagraphFormat.Style);
```

### Смотрите также

* class [CleanupOptions](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
