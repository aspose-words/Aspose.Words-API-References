---
title: ParagraphCollection.ToArray
second_title: Справочник по API Aspose.Words для .NET
description: ParagraphCollection метод. Копирует все абзацы из коллекции в новый массив абзацев.
type: docs
weight: 20
url: /ru/net/aspose.words/paragraphcollection/toarray/
---
## ParagraphCollection.ToArray method

Копирует все абзацы из коллекции в новый массив абзацев.

```csharp
public Paragraph[] ToArray()
```

### Возвращаемое значение

Массив абзацев.

### Примеры

Показывает, как создать массив из NodeCollection.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");

Paragraph[] paras = doc.FirstSection.Body.Paragraphs.ToArray();

Assert.AreEqual(22, paras.Length);
```

Показывает, как использовать «горячее удаление» для удаления узла во время перечисления.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("The first paragraph");
builder.Writeln("The second paragraph");
builder.Writeln("The third paragraph");
builder.Writeln("The fourth paragraph");

// Удалить узел из коллекции в середине перечисления.
foreach (Paragraph para in doc.FirstSection.Body.Paragraphs.ToArray())
    if (para.Range.Text.Contains("third"))
        para.Remove();

Assert.False(doc.GetText().Contains("The third paragraph"));
```

### Смотрите также

* class [Paragraph](../../paragraph/)
* class [ParagraphCollection](../)
* пространство имен [Aspose.Words](../../paragraphcollection/)
* сборка [Aspose.Words](../../../)


