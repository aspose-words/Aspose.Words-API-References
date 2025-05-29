---
title: DocumentProperty.IsLinkToContent
linktitle: IsLinkToContent
articleTitle: IsLinkToContent
second_title: Aspose.Words для .NET
description: Узнайте, связано ли свойство IsLinkToContent DocumentProperty с контентом. Улучшите свой рабочий процесс с помощью бесшовных решений для управления документами.
type: docs
weight: 10
url: /ru/net/aspose.words.properties/documentproperty/islinktocontent/
---
## DocumentProperty.IsLinkToContent property

Показывает, связано ли это свойство с содержимым или нет.

```csharp
public bool IsLinkToContent { get; }
```

## Примеры

Показывает, как связать пользовательское свойство документа с закладкой.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartBookmark("MyBookmark");
builder.Write("Hello world!");
builder.EndBookmark("MyBookmark");

// Связать новое пользовательское свойство с закладкой. Значение этого свойства
// будет содержимым закладки, на которую она ссылается в элементе "LinkSource".
CustomDocumentProperties customProperties = doc.CustomDocumentProperties;
DocumentProperty customProperty = customProperties.AddLinkToContent("Bookmark", "MyBookmark");

Assert.AreEqual(true, customProperty.IsLinkToContent);
Assert.AreEqual("MyBookmark", customProperty.LinkSource);
Assert.AreEqual("Hello world!", customProperty.Value);

doc.Save(ArtifactsDir + "DocumentProperties.LinkCustomDocumentPropertiesToBookmark.docx");
```

### Смотрите также

* class [DocumentProperty](../)
* пространство имен [Aspose.Words.Properties](../../../aspose.words.properties/)
* сборка [Aspose.Words](../../../)
