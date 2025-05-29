---
title: Document.StopTrackRevisions
linktitle: StopTrackRevisions
articleTitle: StopTrackRevisions
second_title: Aspose.Words для .NET
description: Узнайте, как использовать метод StopTrackRevisions для предотвращения автоматической маркировки изменений документа, что повысит эффективность редактирования и ясность документа.
type: docs
weight: 770
url: /ru/net/aspose.words/document/stoptrackrevisions/
---
## Document.StopTrackRevisions method

Останавливает автоматическую маркировку изменений документа как ревизий.

```csharp
public void StopTrackRevisions()
```

## Примеры

Показывает, как отслеживать изменения при редактировании документа.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Редактирование документа обычно не считается правкой, пока мы не начнем отслеживать его.
builder.Write("Hello world! ");

Assert.AreEqual(0, doc.Revisions.Count);
Assert.False(doc.FirstSection.Body.Paragraphs[0].Runs[0].IsInsertRevision);

doc.StartTrackRevisions("John Doe");

builder.Write("Hello again! ");

Assert.AreEqual(1, doc.Revisions.Count);
Assert.True(doc.FirstSection.Body.Paragraphs[0].Runs[1].IsInsertRevision);
Assert.AreEqual("John Doe", doc.Revisions[0].Author);
Assert.IsTrue((DateTime.Now - doc.Revisions[0].DateTime).Milliseconds <= 10);

// Прекратить отслеживать изменения, чтобы не учитывать будущие правки как изменения.
doc.StopTrackRevisions();
builder.Write("Hello again! ");

Assert.AreEqual(1, doc.Revisions.Count);
Assert.False(doc.FirstSection.Body.Paragraphs[0].Runs[2].IsInsertRevision);

// Создание ревизий дает им дату и время операции.
// Мы можем отключить это, передав DateTime.MinValue, когда начинаем отслеживать изменения.
doc.StartTrackRevisions("John Doe", DateTime.MinValue);
builder.Write("Hello again! ");

Assert.AreEqual(2, doc.Revisions.Count);
Assert.AreEqual("John Doe", doc.Revisions[1].Author);
Assert.AreEqual(DateTime.MinValue, doc.Revisions[1].DateTime);

// Мы можем принять/отклонить эти изменения программно
// вызывая такие методы, как Document.AcceptAllRevisions, или метод Accept каждой ревизии.
// В Microsoft Word мы можем обработать их вручную через «Рецензирование» -> «Изменения».
doc.Save(ArtifactsDir + "Revision.StartTrackRevisions.docx");
```

### Смотрите также

* method [StartTrackRevisions](../starttrackrevisions/)
* class [Document](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
