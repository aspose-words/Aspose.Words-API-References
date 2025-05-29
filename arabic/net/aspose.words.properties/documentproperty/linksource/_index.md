---
title: DocumentProperty.LinkSource
linktitle: LinkSource
articleTitle: LinkSource
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية LinkSource لـ DocumentProperty، وقم بالوصول بسهولة إلى مصدر خصائص المستند المخصصة المرتبطة لديك لتحسين إدارة المستندات.
type: docs
weight: 20
url: /ar/net/aspose.words.properties/documentproperty/linksource/
---
## DocumentProperty.LinkSource property

يحصل على مصدر خاصية مستند مخصص مرتبط.

```csharp
public string LinkSource { get; }
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
