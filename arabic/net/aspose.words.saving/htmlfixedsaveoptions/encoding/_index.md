---
title: HtmlFixedSaveOptions.Encoding
linktitle: Encoding
articleTitle: Encoding
second_title: Aspose.Words لـ .NET
description: HtmlFixedSaveOptions Encoding ملكية. يحدد الترميز الذي سيتم استخدامه عند التصدير إلى HTML. القيمة الافتراضية هيترميز UTF8 الجديد صحيح UTF8 مع قائمة مكونات الصنف في C#.
type: docs
weight: 30
url: /ar/net/aspose.words.saving/htmlfixedsaveoptions/encoding/
---
## HtmlFixedSaveOptions.Encoding property

يحدد الترميز الذي سيتم استخدامه عند التصدير إلى HTML. القيمة الافتراضية هي`ترميز UTF8 الجديد (صحيح)` (UTF-8 مع قائمة مكونات الصنف).

```csharp
public Encoding Encoding { get; set; }
```

## أمثلة

يوضح كيفية تعيين الترميز الذي سيتم استخدامه أثناء تصدير مستند إلى HTML.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello World!");

// الترميز الافتراضي هو UTF-8. إذا أردنا تمثيل وثيقتنا باستخدام ترميز مختلف،
// يمكننا استخدام كائن SaveOptions لتعيين ترميز محدد.
HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions
{
    Encoding = Encoding.GetEncoding("ASCII")
};

Assert.AreEqual("US-ASCII", htmlFixedSaveOptions.Encoding.EncodingName);

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.UseEncoding.html", htmlFixedSaveOptions);
```

### أنظر أيضا

* class [HtmlFixedSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
