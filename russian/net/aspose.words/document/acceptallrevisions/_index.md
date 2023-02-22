---
title: Document.AcceptAllRevisions
second_title: Справочник по API Aspose.Words для .NET
description: Document метод. Принимает все отслеживаемые изменения в документе.
type: docs
weight: 500
url: /ru/net/aspose.words/document/acceptallrevisions/
---
## Document.AcceptAllRevisions method

Принимает все отслеживаемые изменения в документе.

```csharp
public void AcceptAllRevisions()
```

### Примечания

Этот метод является кратчайшим путем[`AcceptAll`](../../revisioncollection/acceptall/).

### Примеры

Показывает, как принять все отслеживаемые изменения в документе.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Отредактируйте документ, отслеживая изменения, чтобы создать несколько редакций.
doc.StartTrackRevisions("John Doe");
builder.Write("Hello world! ");
builder.Write("Hello again! "); 
builder.Write("This is another revision.");
doc.StopTrackRevisions();

Assert.AreEqual(3, doc.Revisions.Count);

// Мы можем пройтись по каждой ревизии и принять/отклонить ее как часть нашего документа.
// Если мы знаем, что хотим принять каждую ревизию, мы можем сделать это проще, вызвав этот метод.
doc.AcceptAllRevisions();

Assert.AreEqual(0, doc.Revisions.Count);
Assert.AreEqual("Hello world! Hello again! This is another revision.", doc.GetText().Trim());
```

### Смотрите также

* class [Document](../)
* пространство имен [Aspose.Words](../../document/)
* сборка [Aspose.Words](../../../)


