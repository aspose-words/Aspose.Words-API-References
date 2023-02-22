---
title: Document.RemovePersonalInformation
second_title: Справочник по API Aspose.Words для .NET
description: Document свойство. Получает или устанавливает флаг указывающий что Microsoft Word удалит всю информацию о пользователе из комментариев редакций и свойств документа при сохранении документа.
type: docs
weight: 320
url: /ru/net/aspose.words/document/removepersonalinformation/
---
## Document.RemovePersonalInformation property

Получает или устанавливает флаг, указывающий, что Microsoft Word удалит всю информацию о пользователе из комментариев, редакций и свойств документа при сохранении документа.

```csharp
public bool RemovePersonalInformation { get; set; }
```

### Примеры

Показывает, как включить удаление личной информации во время ручного сохранения.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставьте некоторый контент с личной информацией.
doc.BuiltInDocumentProperties.Author = "John Doe";
doc.BuiltInDocumentProperties.Company = "Placeholder Inc.";

doc.StartTrackRevisions(doc.BuiltInDocumentProperties.Author, DateTime.Now);
builder.Write("Hello world!");
doc.StopTrackRevisions();

// Этот флаг эквивалентен File -> Опции -> Центр управления безопасностью –> Настройки центра управления безопасностью... ->
// Параметры конфиденциальности -> «Удалить личную информацию из свойств файла при сохранении» в Microsoft Word.
doc.RemovePersonalInformation = saveWithoutPersonalInfo;

// Эта опция не будет действовать во время операции сохранения, выполненной с использованием Aspose.Words.
// Персональные данные будут удалены из нашего документа с установленным флагом, когда мы сохраним их вручную с помощью Microsoft Word.
doc.Save(ArtifactsDir + "Document.RemovePersonalInformation.docx");
doc = new Document(ArtifactsDir + "Document.RemovePersonalInformation.docx");

Assert.AreEqual(saveWithoutPersonalInfo, doc.RemovePersonalInformation);
Assert.AreEqual("John Doe", doc.BuiltInDocumentProperties.Author);
Assert.AreEqual("Placeholder Inc.", doc.BuiltInDocumentProperties.Company);
Assert.AreEqual("John Doe", doc.Revisions[0].Author);
```

### Смотрите также

* class [Document](../)
* пространство имен [Aspose.Words](../../document/)
* сборка [Aspose.Words](../../../)


