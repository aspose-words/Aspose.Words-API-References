---
title: HtmlFixedSaveOptions.Encoding
linktitle: Encoding
articleTitle: Encoding
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ترميز HtmlFixedSaveOptions لتصدير HTML بسلاسة. اضبط ترميز UTF-8 بسهولة باستخدام BOM لضمان سلامة البيانات على أكمل وجه.
type: docs
weight: 30
url: /ar/net/aspose.words.saving/htmlfixedsaveoptions/encoding/
---
## HtmlFixedSaveOptions.Encoding property

يحدد الترميز الذي سيتم استخدامه عند التصدير إلى HTML. القيمة الافتراضية هي`ترميز UTF8 الجديد (true)` (UTF-8 مع BOM).

```csharp
public Encoding Encoding { get; set; }
```

## أمثلة

يوضح كيفية تعيين الترميز الذي سيتم استخدامه أثناء تصدير مستند إلى HTML.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello World!");

// الترميز الافتراضي هو UTF-8. إذا أردنا تمثيل مستندنا باستخدام ترميز مختلف،
// يمكننا استخدام كائن SaveOptions لتعيين ترميز معين.
HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions
{
    Encoding = Encoding.ASCII
};

Assert.AreEqual("US-ASCII", htmlFixedSaveOptions.Encoding.EncodingName);

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.UseEncoding.html", htmlFixedSaveOptions);
```

### أنظر أيضا

* class [HtmlFixedSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
