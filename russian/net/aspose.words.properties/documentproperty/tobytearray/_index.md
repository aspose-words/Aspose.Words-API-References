---
title: DocumentProperty.ToByteArray
linktitle: ToByteArray
articleTitle: ToByteArray
second_title: Aspose.Words для .NET
description: DocumentProperty ToByteArray метод. Возвращает значение свойства в виде массива байтов на С#.
type: docs
weight: 70
url: /ru/net/aspose.words.properties/documentproperty/tobytearray/
---
## DocumentProperty.ToByteArray method

Возвращает значение свойства в виде массива байтов.

```csharp
public byte[] ToByteArray()
```

## Примечания

Выдает исключение, если тип свойства неByteArray.

## Примеры

Показывает, как добавить миниатюру к документу, который мы сохраняем как Epub.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Если мы сохраним документ, свойство «Миниатюра» которого содержит добавленные нами данные изображения, как Epub,
// читатель, открывший этот документ, может отобразить изображение перед первой страницей.
BuiltInDocumentProperties properties = doc.BuiltInDocumentProperties;

byte[] thumbnailBytes = File.ReadAllBytes(ImageDir + "Logo.jpg");
properties.Thumbnail = thumbnailBytes;

doc.Save(ArtifactsDir + "DocumentProperties.Thumbnail.epub");

// Мы можем извлечь миниатюру изображения документа и сохранить его в локальной файловой системе.
DocumentProperty thumbnail = doc.BuiltInDocumentProperties["Thumbnail"];
File.WriteAllBytes(ArtifactsDir + "DocumentProperties.Thumbnail.gif", thumbnail.ToByteArray());
```

### Смотрите также

* class [DocumentProperty](../)
* пространство имен [Aspose.Words.Properties](../../../aspose.words.properties/)
* сборка [Aspose.Words](../../../)
