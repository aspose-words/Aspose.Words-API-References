---
title: CustomDocumentProperties.AddLinkToContent
linktitle: AddLinkToContent
articleTitle: AddLinkToContent
second_title: Aspose.Words для .NET
description: Откройте для себя метод CustomDocumentProperties AddLinkToContent, позволяющий легко создавать связанные пользовательские свойства документа для улучшенного управления документами.
type: docs
weight: 20
url: /ru/net/aspose.words.properties/customdocumentproperties/addlinktocontent/
---
## CustomDocumentProperties.AddLinkToContent method

Создает новое связанное с содержимым пользовательское свойство документа.

```csharp
public DocumentProperty AddLinkToContent(string name, string linkSource)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| name | String | Название объекта недвижимости. |
| linkSource | String | Источник собственности. |

### Возвращаемое значение

Вновь созданный объект недвижимости или`нулевой` когда*linkSource* недействительно.

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

* class [DocumentProperty](../../documentproperty/)
* class [CustomDocumentProperties](../)
* пространство имен [Aspose.Words.Properties](../../../aspose.words.properties/)
* сборка [Aspose.Words](../../../)
