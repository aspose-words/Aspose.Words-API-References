---
title: Document.AcceptAllRevisions
linktitle: AcceptAllRevisions
articleTitle: AcceptAllRevisions
second_title: Aspose.Words для .NET
description: Оптимизируйте процесс редактирования с помощью метода AcceptAllRevisions, который без труда принимает все отслеженные изменения в документе для получения безупречной финальной версии.
type: docs
weight: 540
url: /ru/net/aspose.words/document/acceptallrevisions/
---
## Document.AcceptAllRevisions method

Принимает все отслеженные изменения в документе.

```csharp
public void AcceptAllRevisions()
```

## Примечания

Этот метод является сокращенным для[`AcceptAll`](../../revisioncollection/acceptall/).

## Примеры

Показывает, как принять все отслеживаемые изменения в документе.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Редактируйте документ, отслеживая изменения, чтобы создать несколько редакций.
doc.StartTrackRevisions("John Doe");
builder.Write("Hello world! ");
builder.Write("Hello again! ");
builder.Write("This is another revision.");
doc.StopTrackRevisions();

Assert.AreEqual(3, doc.Revisions.Count);

// Мы можем перебрать каждую редакцию и принять/отклонить ее как часть нашего документа.
// Если мы знаем, что хотим принять каждую ревизию, мы можем сделать это более прямолинейно, вызвав этот метод.
doc.AcceptAllRevisions();

Assert.AreEqual(0, doc.Revisions.Count);
Assert.AreEqual("Hello world! Hello again! This is another revision.", doc.GetText().Trim());
```

### Смотрите также

* class [Document](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
