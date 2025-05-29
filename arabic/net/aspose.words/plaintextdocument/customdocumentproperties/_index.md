---
title: PlainTextDocument.CustomDocumentProperties
linktitle: CustomDocumentProperties
articleTitle: CustomDocumentProperties
second_title: Aspose.Words لـ .NET
description: اكتشف كيفية الوصول إلى CustomDocumentProperties في PlainTextDocument لتحسين إدارة المستندات وتخصيصها. أطلق العنان لإمكانات مستندك!
type: docs
weight: 30
url: /ar/net/aspose.words/plaintextdocument/customdocumentproperties/
---
## PlainTextDocument.CustomDocumentProperties property

يحصل`CustomDocumentProperties` من الوثيقة.

```csharp
public CustomDocumentProperties CustomDocumentProperties { get; }
```

## أمثلة

يوضح كيفية تحميل محتويات مستند Microsoft Word في نص عادي ثم الوصول إلى خصائص المستند الأصلي المخصصة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
doc.CustomDocumentProperties.Add("Location of writing", "123 Main St, London, UK");

doc.Save(ArtifactsDir + "PlainTextDocument.CustomDocumentProperties.docx");

PlainTextDocument plaintext = new PlainTextDocument(ArtifactsDir + "PlainTextDocument.CustomDocumentProperties.docx");

Assert.AreEqual("Hello world!", plaintext.Text.Trim());
Assert.AreEqual("123 Main St, London, UK", plaintext.CustomDocumentProperties["Location of writing"].Value);
```

### أنظر أيضا

* class [CustomDocumentProperties](../../../aspose.words.properties/customdocumentproperties/)
* class [PlainTextDocument](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
