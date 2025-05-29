---
title: PlainTextDocument.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words لـ .NET
description: يمكنك الوصول إلى خاصية النص في PlainTextDocument لاسترداد محتوى المستند كسلسلة واحدة، مما يعزز معالجة البيانات وتحليلها.
type: docs
weight: 40
url: /ar/net/aspose.words/plaintextdocument/text/
---
## PlainTextDocument.Text property

يحصل على محتوى نصي للمستند مُدمجًا كسلسلة.

```csharp
public string Text { get; }
```

## أمثلة

يوضح كيفية تحميل محتويات مستند Microsoft Word في نص عادي.

```csharp
Document doc = new Document(); 
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

doc.Save(ArtifactsDir + "PlainTextDocument.Load.docx");

PlainTextDocument plaintext = new PlainTextDocument(ArtifactsDir + "PlainTextDocument.Load.docx");

Assert.AreEqual("Hello world!", plaintext.Text.Trim());
```

### أنظر أيضا

* class [PlainTextDocument](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
