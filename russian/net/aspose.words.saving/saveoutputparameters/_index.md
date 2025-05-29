---
title: SaveOutputParameters Class
linktitle: SaveOutputParameters
articleTitle: SaveOutputParameters
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Saving.SaveOutputParameters, который предоставляет важные сведения после сохранения документа, расширяя возможности управления документами.
type: docs
weight: 6390
url: /ru/net/aspose.words.saving/saveoutputparameters/
---
## SaveOutputParameters class

Этот объект возвращается вызывающей стороне после сохранения документа и содержит дополнительную информацию, которая была сгенерирована или вычислена во время операции сохранения. Вызывающая сторона может использовать или игнорировать этот объект.

Чтобы узнать больше, посетите[Сохранить документ](https://docs.aspose.com/words/net/save-a-document/) документальная статья.

```csharp
public class SaveOutputParameters
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [ContentType](../../aspose.words.saving/saveoutputparameters/contenttype/) { get; } | Возвращает строку Content-Type (тип интернет-носителя), которая идентифицирует тип сохраненного документа. |

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

* пространство имен [Aspose.Words.Saving](../../aspose.words.saving/)
* сборка [Aspose.Words](../../)
