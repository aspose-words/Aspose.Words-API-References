---
title: Document.RemovePersonalInformation
linktitle: RemovePersonalInformation
articleTitle: RemovePersonalInformation
second_title: Aspose.Words для .NET
description: Обеспечьте конфиденциальность с помощью функции Document RemovePersonalInformation в Word, которая автоматически удаляет данные пользователя из комментариев и свойств при сохранении.
type: docs
weight: 360
url: /ru/net/aspose.words/document/removepersonalinformation/
---
## Document.RemovePersonalInformation property

Возвращает или задает флаг, указывающий, что Microsoft Word удалит всю пользовательскую информацию из комментариев, редакций и свойств документа при сохранении документа.

```csharp
public bool RemovePersonalInformation { get; set; }
```

## Примеры

Показывает, как включить удаление личной информации при ручном сохранении.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставьте контент с личной информацией.
doc.BuiltInDocumentProperties.Author = "John Doe";
doc.BuiltInDocumentProperties.Company = "Placeholder Inc.";

doc.StartTrackRevisions(doc.BuiltInDocumentProperties.Author, DateTime.Now);
builder.Write("Hello world!");
doc.StopTrackRevisions();

// Этот флаг эквивалентен Файл -> Параметры -> Центр управления безопасностью -> Настройки центра управления безопасностью... ->
// Параметры конфиденциальности -> «Удалять личную информацию из свойств файла при сохранении» в Microsoft Word.
doc.RemovePersonalInformation = saveWithoutPersonalInfo;

// Эта опция не вступит в силу во время операции сохранения, выполненной с помощью Aspose.Words.
// Персональные данные будут удалены из нашего документа с установленным флагом, если мы сохраним его вручную с помощью Microsoft Word.
doc.Save(ArtifactsDir + "Document.RemovePersonalInformation.docx");
doc = new Document(ArtifactsDir + "Document.RemovePersonalInformation.docx");

Assert.AreEqual(saveWithoutPersonalInfo, doc.RemovePersonalInformation);
Assert.AreEqual("John Doe", doc.BuiltInDocumentProperties.Author);
Assert.AreEqual("Placeholder Inc.", doc.BuiltInDocumentProperties.Company);
Assert.AreEqual("John Doe", doc.Revisions[0].Author);
```

### Смотрите также

* class [Document](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
