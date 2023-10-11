---
title: Document.StartTrackRevisions
second_title: Справочник по API Aspose.Words для .NET
description: Document метод. Начинает автоматически отмечать все дальнейшие изменения которые вы вносите в документ программно как изменения версии.
type: docs
weight: 730
url: /ru/net/aspose.words/document/starttrackrevisions/
---
## StartTrackRevisions(string, DateTime) {#starttrackrevisions_1}

Начинает автоматически отмечать все дальнейшие изменения, которые вы вносите в документ программно, как изменения версии.

```csharp
public void StartTrackRevisions(string author, DateTime dateTime)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| author | String | Инициалы автора для исправлений. |
| dateTime | DateTime | Дата и время, используемые для изменений. |

### Примечания

Если вы вызовете этот метод, а затем внесете некоторые изменения в документ программно, сохраните документ и позже откроете его в MS Word, вы увидите эти изменения как исправления.

В настоящее время Aspose.Words поддерживает только отслеживание вставок и удалений узлов. Изменения форматирования не записываются как версии.

Автоматическое отслеживание изменений поддерживается как при изменении этого документа посредством манипуляций с узлами , так и при использовании[`DocumentBuilder`](../../documentbuilder/)

Этот метод не меняет[`TrackRevisions`](../trackrevisions/) и не использует его значение value для отслеживания версий.

### Примеры

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

* method [StopTrackRevisions](../stoptrackrevisions/)
* class [Document](../)
* пространство имен [Aspose.Words](../../document/)
* сборка [Aspose.Words](../../../)

---

## StartTrackRevisions(string) {#starttrackrevisions}

Начинает автоматически отмечать все дальнейшие изменения, которые вы вносите в документ программно, как изменения версии.

```csharp
public void StartTrackRevisions(string author)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| author | String | Инициалы автора для исправлений. |

### Примечания

Если вы вызовете этот метод, а затем внесете некоторые изменения в документ программно, сохраните документ и позже откроете его в MS Word, вы увидите эти изменения как исправления.

В настоящее время Aspose.Words поддерживает только отслеживание вставок и удалений узлов. Изменения форматирования не записываются как версии.

Автоматическое отслеживание изменений поддерживается как при изменении этого документа посредством манипуляций с узлами , так и при использовании[`DocumentBuilder`](../../documentbuilder/)

Этот метод не меняет[`TrackRevisions`](../trackrevisions/) и не использует его значение value для отслеживания версий.

### Примеры

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

* method [StopTrackRevisions](../stoptrackrevisions/)
* class [Document](../)
* пространство имен [Aspose.Words](../../document/)
* сборка [Aspose.Words](../../../)


