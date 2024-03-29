---
title: Document.StopTrackRevisions
linktitle: StopTrackRevisions
articleTitle: StopTrackRevisions
second_title: Aspose.Words для .NET
description: Document StopTrackRevisions метод. Останавливает автоматическую маркировку изменений документа как редакций на С#.
type: docs
weight: 720
url: /ru/net/aspose.words/document/stoptrackrevisions/
---
## Document.StopTrackRevisions method

Останавливает автоматическую маркировку изменений документа как редакций.

```csharp
public void StopTrackRevisions()
```

## Примеры

Показывает, как отслеживать изменения при редактировании документа.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Редактирование документа обычно не считается редакцией, пока мы не начнем его отслеживать.
builder.Write("Hello world! ");

Assert.AreEqual(0, doc.Revisions.Count);
Assert.False(doc.FirstSection.Body.Paragraphs[0].Runs[0].IsInsertRevision);

doc.StartTrackRevisions("John Doe");

builder.Write("Hello again! ");

Assert.AreEqual(1, doc.Revisions.Count);
Assert.True(doc.FirstSection.Body.Paragraphs[0].Runs[1].IsInsertRevision);
Assert.AreEqual("John Doe", doc.Revisions[0].Author);
Assert.That(doc.Revisions[0].DateTime, Is.EqualTo(DateTime.Now).Within(10).Milliseconds);

// Прекратить отслеживание редакций, чтобы будущие изменения не считались редакциями.
doc.StopTrackRevisions();
builder.Write("Hello again! ");

Assert.AreEqual(1, doc.Revisions.Count);
Assert.False(doc.FirstSection.Body.Paragraphs[0].Runs[2].IsInsertRevision);

// Создание ревизий дает им дату и время операции.
// Мы можем отключить это, передав DateTime.MinValue, когда начинаем отслеживать версии.
doc.StartTrackRevisions("John Doe", DateTime.MinValue);
builder.Write("Hello again! ");

Assert.AreEqual(2, doc.Revisions.Count);
Assert.AreEqual("John Doe", doc.Revisions[1].Author);
Assert.AreEqual(DateTime.MinValue, doc.Revisions[1].DateTime);

// Мы можем принять/отклонить эти изменения программно
// путем вызова таких методов, как Document.AcceptAllRevisions, или метода Accept каждой ревизии.
// В Microsoft Word мы можем обработать их вручную через «Просмотр» ->> "Изменения".
doc.Save(ArtifactsDir + "Document.StartTrackRevisions.docx");
```

### Смотрите также

* method [StartTrackRevisions](../starttrackrevisions/)
* class [Document](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
