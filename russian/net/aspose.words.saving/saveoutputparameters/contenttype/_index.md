---
title: SaveOutputParameters.ContentType
linktitle: ContentType
articleTitle: ContentType
second_title: Aspose.Words для .NET
description: Откройте для себя свойство SaveOutputParameters ContentType, которое предоставляет тип интернет-носителя для ваших сохраненных документов, обеспечивая точную идентификацию файлов.
type: docs
weight: 10
url: /ru/net/aspose.words.saving/saveoutputparameters/contenttype/
---
## SaveOutputParameters.ContentType property

Возвращает строку Content-Type (тип интернет-носителя), которая идентифицирует тип сохраненного документа.

```csharp
public string ContentType { get; }
```

## Примеры

Показывает, как получить доступ к выходным параметрам операции сохранения документа.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// После сохранения документа мы можем получить доступ к типу интернет-носителя (MIME-типу) вновь созданного выходного документа.
SaveOutputParameters parameters = doc.Save(ArtifactsDir + "Document.SaveOutputParameters.doc");

Assert.AreEqual("application/msword", parameters.ContentType);

// Это свойство изменяется в зависимости от формата сохранения.
parameters = doc.Save(ArtifactsDir + "Document.SaveOutputParameters.pdf");

Assert.AreEqual("application/pdf", parameters.ContentType);
```

### Смотрите также

* class [SaveOutputParameters](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
