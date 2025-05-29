---
title: PlainTextDocument.BuiltInDocumentProperties
linktitle: BuiltInDocumentProperties
articleTitle: BuiltInDocumentProperties
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية PlainTextDocument BuiltInDocumentProperties للوصول بسهولة إلى بيانات التعريف الأساسية للمستندات وإدارتها لتحسين تنظيم المستندات.
type: docs
weight: 20
url: /ar/net/aspose.words/plaintextdocument/builtindocumentproperties/
---
## PlainTextDocument.BuiltInDocumentProperties property

يحصل`BuiltInDocumentProperties` من الوثيقة.

```csharp
public BuiltInDocumentProperties BuiltInDocumentProperties { get; }
```

## أمثلة

يوضح كيفية تحميل محتويات مستند Microsoft Word في نص عادي ثم الوصول إلى خصائص المستند الأصلي المضمنة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
doc.BuiltInDocumentProperties.Author = "John Doe";

doc.Save(ArtifactsDir + "PlainTextDocument.BuiltInProperties.docx");

PlainTextDocument plaintext = new PlainTextDocument(ArtifactsDir + "PlainTextDocument.BuiltInProperties.docx");

Assert.AreEqual("Hello world!", plaintext.Text.Trim());
Assert.AreEqual("John Doe", plaintext.BuiltInDocumentProperties.Author);
```

### أنظر أيضا

* class [BuiltInDocumentProperties](../../../aspose.words.properties/builtindocumentproperties/)
* class [PlainTextDocument](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
