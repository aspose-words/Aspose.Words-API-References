---
title: DocumentProperty.IsLinkToContent
second_title: Aspose.Words لمراجع .NET API
description: DocumentProperty ملكية. يوضح ما إذا كانت هذه الخاصية مرتبطة بالمحتوى أم لا.
type: docs
weight: 10
url: /ar/net/aspose.words.properties/documentproperty/islinktocontent/
---
## DocumentProperty.IsLinkToContent property

يوضح ما إذا كانت هذه الخاصية مرتبطة بالمحتوى أم لا.

```csharp
public bool IsLinkToContent { get; }
```

### أمثلة

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

* class [DocumentProperty](../)
* مساحة الاسم [Aspose.Words.Properties](../../documentproperty/)
* المجسم [Aspose.Words](../../../)


