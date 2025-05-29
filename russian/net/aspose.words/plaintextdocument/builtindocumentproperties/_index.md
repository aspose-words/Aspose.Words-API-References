---
title: PlainTextDocument.BuiltInDocumentProperties
linktitle: BuiltInDocumentProperties
articleTitle: BuiltInDocumentProperties
second_title: Aspose.Words для .NET
description: Откройте для себя свойство BuiltInDocumentProperties класса PlainTextDocument, чтобы легко получать доступ к основным метаданным документа и управлять ими для улучшенной организации документа.
type: docs
weight: 20
url: /ru/net/aspose.words/plaintextdocument/builtindocumentproperties/
---
## PlainTextDocument.BuiltInDocumentProperties property

Получает`BuiltInDocumentProperties` документа.

```csharp
public BuiltInDocumentProperties BuiltInDocumentProperties { get; }
```

## Примеры

Показывает, как загрузить содержимое документа Microsoft Word в виде обычного текста, а затем получить доступ к встроенным свойствам исходного документа.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
doc.BuiltInDocumentProperties.Author = "John Doe";

doc.Save(ArtifactsDir + "PlainTextDocument.BuiltInProperties.docx");

PlainTextDocument plaintext = new PlainTextDocument(ArtifactsDir + "PlainTextDocument.BuiltInProperties.docx");

Assert.AreEqual("Hello world!", plaintext.Text.Trim());
Assert.AreEqual("John Doe", plaintext.BuiltInDocumentProperties.Author);
```

### Смотрите также

* class [BuiltInDocumentProperties](../../../aspose.words.properties/builtindocumentproperties/)
* class [PlainTextDocument](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
