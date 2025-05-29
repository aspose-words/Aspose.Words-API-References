---
title: CustomDocumentProperties.AddLinkToContent
linktitle: AddLinkToContent
articleTitle: AddLinkToContent
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة AddLinkToContent الخاصة بـ CustomDocumentProperties لإنشاء خصائص مستند مخصصة مرتبطة بسهولة لتحسين إدارة المستندات.
type: docs
weight: 20
url: /ar/net/aspose.words.properties/customdocumentproperties/addlinktocontent/
---
## CustomDocumentProperties.AddLinkToContent method

ينشئ خاصية مستند مخصصة جديدة مرتبطة بالمحتوى.

```csharp
public DocumentProperty AddLinkToContent(string name, string linkSource)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| name | String | اسم العقار. |
| linkSource | String | مصدر الملكية. |

### قيمة الإرجاع

كائن الخاصية الذي تم إنشاؤه حديثًا أو`باطل` عندما*linkSource* غير صالح.

## أمثلة

يوضح كيفية ربط خاصية مستند مخصصة بإشارة مرجعية.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartBookmark("MyBookmark");
builder.Write("Hello world!");
builder.EndBookmark("MyBookmark");

// اربط خاصية مخصصة جديدة بإشارة مرجعية. قيمة هذه الخاصية
//سيكون محتوى الإشارة المرجعية التي تشير إليها في عضو "LinkSource".
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
