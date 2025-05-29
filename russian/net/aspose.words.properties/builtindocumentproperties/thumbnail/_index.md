---
title: BuiltInDocumentProperties.Thumbnail
linktitle: Thumbnail
articleTitle: Thumbnail
second_title: Aspose.Words для .NET
description: Управляйте визуальной привлекательностью вашего документа с помощью BuiltInDocumentProperties. Легко получайте или устанавливайте миниатюры изображений для улучшения представления и организации.
type: docs
weight: 310
url: /ru/net/aspose.words.properties/builtindocumentproperties/thumbnail/
---
## BuiltInDocumentProperties.Thumbnail property

Получает или задает миниатюру документа.

```csharp
public byte[] Thumbnail { get; set; }
```

### Исключения

| исключение | условие |
| --- | --- |
| InvalidOperationException | Вызывается, если изображение недопустимо или его формат не поддерживается определенным форматом документа. |

## Примечания

На данный момент это свойство используется только при экспорте документа в ePub, оно не считывается и не записывается в другие форматы документов.

Этому свойству можно задать изображение произвольного формата, но формат проверяется при экспорте.

Для публикации в формате ePub можно использовать только изображения в форматах gif, jpeg и png.

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

* class [BuiltInDocumentProperties](../)
* пространство имен [Aspose.Words.Properties](../../../aspose.words.properties/)
* сборка [Aspose.Words](../../../)
