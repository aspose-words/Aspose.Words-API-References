---
title: DocumentProperty.IsLinkToContent
linktitle: IsLinkToContent
articleTitle: IsLinkToContent
second_title: Aspose.Words لـ .NET
description: اكتشف ما إذا كانت خاصية IsLinkToContent في DocumentProperty متصلة بالمحتوى. حسّن سير عملك بحلول إدارة مستندات سلسة.
type: docs
weight: 10
url: /ar/net/aspose.words.properties/documentproperty/islinktocontent/
---
## DocumentProperty.IsLinkToContent property

يُظهر ما إذا كانت هذه الخاصية مرتبطة بالمحتوى أم لا.

```csharp
public bool IsLinkToContent { get; }
```

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

* class [DocumentProperty](../)
* مساحة الاسم [Aspose.Words.Properties](../../../aspose.words.properties/)
* المجسم [Aspose.Words](../../../)
