---
title: DocumentProperty.ToByteArray
linktitle: ToByteArray
articleTitle: ToByteArray
second_title: Aspose.Words для .NET
description: Преобразуйте DocumentProperty в массив байтов без усилий с помощью метода ToByteArray. Оптимизируйте обработку данных и повысьте эффективность кодирования!
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

Выдает исключение, если тип свойства не являетсяByteArray.

## Примеры

Показывает, как добавить миниатюру к документу, сохраняемому в формате Epub.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Если мы сохраним документ, свойство «Миниатюра» которого содержит данные изображения, которые мы добавили, как Epub,
// читатель, открывающий этот документ, может отобразить изображение перед первой страницей.
BuiltInDocumentProperties properties = doc.BuiltInDocumentProperties;

byte[] thumbnailBytes = File.ReadAllBytes(ImageDir + "Logo.jpg");
properties.Thumbnail = thumbnailBytes;

doc.Save(ArtifactsDir + "DocumentProperties.Thumbnail.epub");

// Мы можем извлечь миниатюру изображения документа и сохранить ее в локальной файловой системе.
DocumentProperty thumbnail = doc.BuiltInDocumentProperties["Thumbnail"];
File.WriteAllBytes(ArtifactsDir + "DocumentProperties.Thumbnail.gif", thumbnail.ToByteArray());
```

### Смотрите также

* class [DocumentProperty](../)
* пространство имен [Aspose.Words.Properties](../../../aspose.words.properties/)
* сборка [Aspose.Words](../../../)
