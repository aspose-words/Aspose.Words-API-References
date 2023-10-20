---
title: CustomDocumentProperties.AddLinkToContent
linktitle: AddLinkToContent
articleTitle: AddLinkToContent
second_title: Aspose.Words для .NET
description: CustomDocumentProperties AddLinkToContent метод. Создает новое свойство пользовательского документа связанное с содержимым на С#.
type: docs
weight: 20
url: /ru/net/aspose.words.properties/customdocumentproperties/addlinktocontent/
---
## CustomDocumentProperties.AddLinkToContent method

Создает новое свойство пользовательского документа, связанное с содержимым.

```csharp
public DocumentProperty AddLinkToContent(string name, string linkSource)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| name | String | Название объекта недвижимости. |
| linkSource | String | Источник собственности. |

### Возвращаемое значение

Вновь созданный объект свойства или`нулевой` когда*linkSource* является недействительным.

## Примеры

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

* class [DocumentProperty](../../documentproperty/)
* class [CustomDocumentProperties](../)
* пространство имен [Aspose.Words.Properties](../../../aspose.words.properties/)
* сборка [Aspose.Words](../../../)
