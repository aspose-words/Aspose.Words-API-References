---
title: StartTrackRevisions
second_title: Справочник по API Aspose.Words для .NET
description: Начинает автоматически отмечать все дальнейшие изменения которые вы вносите в документ программно как изменения редакции.
type: docs
weight: 690
url: /ru/net/aspose.words/document/starttrackrevisions/
---
## StartTrackRevisions(string, DateTime) {#starttrackrevisions_1}

Начинает автоматически отмечать все дальнейшие изменения, которые вы вносите в документ программно, как изменения редакции.

```csharp
public void StartTrackRevisions(string author, DateTime dateTime)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| author | String | Инициалы автора, используемые для редакций. |
| dateTime | DateTime | Дата и время, используемые для ревизий. |

### Примечания

Если вызвать этот метод, а затем программно внести некоторые изменения в документ, сохраните документ, а затем откройте документ в MS Word, вы увидите эти изменения как ревизии.

В настоящее время Aspose.Words поддерживает только отслеживание вставок и удалений узлов. Изменения форматирования не записываются как ревизии.

Поддерживается автоматическое отслеживание изменений как при модификации этого документа посредством манипуляций с узлами , так и при использовании[`DocumentBuilder`](../../documentbuilder)

Этот метод не изменяет параметр[`TrackRevisions`](../trackrevisions)и не используйте его значение для отслеживания изменений.

### Примеры

Показывает, как отслеживать изменения при редактировании документа.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Редактирование документа обычно не считается редакцией, пока мы не начнем их отслеживать.
builder.Write("Hello world! ");

Assert.AreEqual(0, doc.Revisions.Count);
Assert.False(doc.FirstSection.Body.Paragraphs[0].Runs[0].IsInsertRevision);

doc.StartTrackRevisions("John Doe");

builder.Write("Hello again! ");

Assert.AreEqual(1, doc.Revisions.Count);
Assert.True(doc.FirstSection.Body.Paragraphs[0].Runs[1].IsInsertRevision);
Assert.AreEqual("John Doe", doc.Revisions[0].Author);
Assert.That(doc.Revisions[0].DateTime, Is.EqualTo(DateTime.Now).Within(10).Milliseconds);

// Остановить отслеживание ревизий, чтобы не считать будущие правки ревизиями.
doc.StopTrackRevisions();
builder.Write("Hello again! ");

Assert.AreEqual(1, doc.Revisions.Count);
Assert.False(doc.FirstSection.Body.Paragraphs[0].Runs[2].IsInsertRevision);

// Создание ревизий дает им дату и время операции.
// Мы можем отключить это, передав DateTime.MinValue, когда начинаем отслеживать ревизии.
doc.StartTrackRevisions("John Doe", DateTime.MinValue);
builder.Write("Hello again! ");

Assert.AreEqual(2, doc.Revisions.Count);
Assert.AreEqual("John Doe", doc.Revisions[1].Author);
Assert.AreEqual(DateTime.MinValue, doc.Revisions[1].DateTime);

// Мы можем принять/отклонить эти изменения программно
// путем вызова таких методов, как Document.AcceptAllRevisions, или метода Accept каждой ревизии.
// В Microsoft Word мы можем обработать их вручную через "Рецензирование" -> "Изменения".
doc.Save(ArtifactsDir + "Document.StartTrackRevisions.docx");
```

### Смотрите также

* method [StopTrackRevisions](../stoptrackrevisions)
* class [Document](../../document)
* namespace [Aspose.Words](../../document)
* assembly [Aspose.Words](../../../)

---

## StartTrackRevisions(string) {#starttrackrevisions}

Начинает автоматически отмечать все дальнейшие изменения, которые вы вносите в документ программно, как изменения редакции.

```csharp
public void StartTrackRevisions(string author)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| author | String | Инициалы автора, используемые для редакций. |

### Примечания

Если вызвать этот метод, а затем программно внести некоторые изменения в документ, сохраните документ, а затем откройте документ в MS Word, вы увидите эти изменения как ревизии.

В настоящее время Aspose.Words поддерживает только отслеживание вставок и удалений узлов. Изменения форматирования не записываются как ревизии.

Поддерживается автоматическое отслеживание изменений как при модификации этого документа посредством манипуляций с узлами , так и при использовании[`DocumentBuilder`](../../documentbuilder)

Этот метод не изменяет параметр[`TrackRevisions`](../trackrevisions)и не используйте его значение для отслеживания изменений.

### Примеры

Показывает, как отслеживать изменения при редактировании документа.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Редактирование документа обычно не считается редакцией, пока мы не начнем их отслеживать.
builder.Write("Hello world! ");

Assert.AreEqual(0, doc.Revisions.Count);
Assert.False(doc.FirstSection.Body.Paragraphs[0].Runs[0].IsInsertRevision);

doc.StartTrackRevisions("John Doe");

builder.Write("Hello again! ");

Assert.AreEqual(1, doc.Revisions.Count);
Assert.True(doc.FirstSection.Body.Paragraphs[0].Runs[1].IsInsertRevision);
Assert.AreEqual("John Doe", doc.Revisions[0].Author);
Assert.That(doc.Revisions[0].DateTime, Is.EqualTo(DateTime.Now).Within(10).Milliseconds);

// Остановить отслеживание ревизий, чтобы не считать будущие правки ревизиями.
doc.StopTrackRevisions();
builder.Write("Hello again! ");

Assert.AreEqual(1, doc.Revisions.Count);
Assert.False(doc.FirstSection.Body.Paragraphs[0].Runs[2].IsInsertRevision);

// Создание ревизий дает им дату и время операции.
// Мы можем отключить это, передав DateTime.MinValue, когда начинаем отслеживать ревизии.
doc.StartTrackRevisions("John Doe", DateTime.MinValue);
builder.Write("Hello again! ");

Assert.AreEqual(2, doc.Revisions.Count);
Assert.AreEqual("John Doe", doc.Revisions[1].Author);
Assert.AreEqual(DateTime.MinValue, doc.Revisions[1].DateTime);

// Мы можем принять/отклонить эти изменения программно
// путем вызова таких методов, как Document.AcceptAllRevisions, или метода Accept каждой ревизии.
// В Microsoft Word мы можем обработать их вручную через "Рецензирование" -> "Изменения".
doc.Save(ArtifactsDir + "Document.StartTrackRevisions.docx");
```

### Смотрите также

* method [StopTrackRevisions](../stoptrackrevisions)
* class [Document](../../document)
* namespace [Aspose.Words](../../document)
* assembly [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
