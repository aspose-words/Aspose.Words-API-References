---
title: Document.StartTrackRevisions
linktitle: StartTrackRevisions
articleTitle: StartTrackRevisions
second_title: Aspose.Words для .NET
description: Легко отслеживайте изменения документов с помощью метода StartTrackRevisions. Автоматически отмечайте все правки как ревизии для бесперебойной совместной работы и ясности.
type: docs
weight: 760
url: /ru/net/aspose.words/document/starttrackrevisions/
---
## StartTrackRevisions(*string, DateTime*) {#starttrackrevisions_1}

Начинает автоматически отмечать все дальнейшие изменения, вносимые вами в документ программным способом, как изменения редакции.

```csharp
public void StartTrackRevisions(string author, DateTime dateTime)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| author | String | Инициалы автора для использования при исправлениях. |
| dateTime | DateTime | Дата и время, которые следует использовать для внесения изменений. |

## Примечания

Если вы вызовете этот метод, а затем внесете некоторые изменения в документ программным путем, сохраните документ и позже откройте его в MS Word, вы увидите эти изменения как исправления.

В настоящее время Aspose.Words поддерживает только отслеживание вставок и удалений узлов. Изменения форматирования не регистрируются как ревизии.

Автоматическое отслеживание изменений поддерживается как при изменении этого документа посредством манипуляций с узлами , так и при использовании[`DocumentBuilder`](../../documentbuilder/)

Этот метод не изменяет[`TrackRevisions`](../trackrevisions/) параметр и не использует его значение для целей отслеживания изменений.

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

* method [StopTrackRevisions](../stoptrackrevisions/)
* class [Document](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)

---

## StartTrackRevisions(*string*) {#starttrackrevisions}

Начинает автоматически отмечать все дальнейшие изменения, вносимые вами в документ программным способом, как изменения редакции.

```csharp
public void StartTrackRevisions(string author)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| author | String | Инициалы автора для использования при исправлениях. |

## Примечания

Если вы вызовете этот метод, а затем внесете некоторые изменения в документ программным путем, сохраните документ и позже откройте его в MS Word, вы увидите эти изменения как исправления.

В настоящее время Aspose.Words поддерживает только отслеживание вставок и удалений узлов. Изменения форматирования не регистрируются как ревизии.

Автоматическое отслеживание изменений поддерживается как при изменении этого документа посредством манипуляций с узлами , так и при использовании[`DocumentBuilder`](../../documentbuilder/)

Этот метод не изменяет[`TrackRevisions`](../trackrevisions/) параметр и не использует его значение для целей отслеживания изменений.

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

* method [StopTrackRevisions](../stoptrackrevisions/)
* class [Document](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
