---
title: CustomDocumentProperties.AddLinkToContent
linktitle: AddLinkToContent
articleTitle: AddLinkToContent
second_title: Aspose.Words لـ .NET
description: CustomDocumentProperties AddLinkToContent طريقة. إنشاء خاصية وثيقة مخصصة جديدة مرتبطة بالمحتوى في C#.
type: docs
weight: 20
url: /ar/net/aspose.words.properties/customdocumentproperties/addlinktocontent/
---
## CustomDocumentProperties.AddLinkToContent method

إنشاء خاصية وثيقة مخصصة جديدة مرتبطة بالمحتوى.

```csharp
public DocumentProperty AddLinkToContent(string name, string linkSource)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| name | String | اسم العقار. |
| linkSource | String | مصدر العقار. |

### قيمة الإرجاع

كائن الخاصية الذي تم إنشاؤه حديثًا أو`باطل` عندما*linkSource* غير صالح.

## أمثلة

يوضح كيفية ربط خاصية مستند مخصص بإشارة مرجعية.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartBookmark("MyBookmark");
builder.Write("Hello world!");
builder.EndBookmark("MyBookmark");

// ربط خاصية مخصصة جديدة بإشارة مرجعية. قيمة هذا العقار
// ستكون محتويات الإشارة المرجعية التي تشير إليها في العضو "LinkSource".
CustomDocumentProperties customProperties = doc.CustomDocumentProperties;
DocumentProperty customProperty = customProperties.AddLinkToContent("Bookmark", "MyBookmark");

Assert.AreEqual(true, customProperty.IsLinkToContent);
Assert.AreEqual("MyBookmark", customProperty.LinkSource);
Assert.AreEqual("Hello world!", customProperty.Value);

doc.Save(ArtifactsDir + "DocumentProperties.LinkCustomDocumentPropertiesToBookmark.docx");
```

### أنظر أيضا

* class [DocumentProperty](../../documentproperty/)
* class [CustomDocumentProperties](../)
* مساحة الاسم [Aspose.Words.Properties](../../../aspose.words.properties/)
* المجسم [Aspose.Words](../../../)
