---
title: DocumentProperty.LinkSource
second_title: Справочник по API Aspose.Words для .NET
description: DocumentProperty свойство. Получает источник связанного свойства пользовательского документа.
type: docs
weight: 20
url: /ru/net/aspose.words.properties/documentproperty/linksource/
---
## DocumentProperty.LinkSource property

Получает источник связанного свойства пользовательского документа.

```csharp
public string LinkSource { get; }
```

### Примеры

Показывает, как связать настраиваемое свойство документа с закладкой.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartBookmark("MyBookmark");
builder.Write("Hello world!");
builder.EndBookmark("MyBookmark");

// Связываем новое пользовательское свойство с закладкой. Стоимость этого объекта недвижимости
// будет содержимым закладки, на которую он ссылается в элементе «LinkSource».
CustomDocumentProperties customProperties = doc.CustomDocumentProperties;
DocumentProperty customProperty = customProperties.AddLinkToContent("Bookmark", "MyBookmark");

Assert.AreEqual(true, customProperty.IsLinkToContent);
Assert.AreEqual("MyBookmark", customProperty.LinkSource);
Assert.AreEqual("Hello world!", customProperty.Value);

doc.Save(ArtifactsDir + "DocumentProperties.LinkCustomDocumentPropertiesToBookmark.docx");
```

### Смотрите также

* class [DocumentProperty](../)
* пространство имен [Aspose.Words.Properties](../../documentproperty/)
* сборка [Aspose.Words](../../../)


