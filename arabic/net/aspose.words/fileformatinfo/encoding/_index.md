---
title: FileFormatInfo.Encoding
second_title: Aspose.Words لمراجع .NET API
description: FileFormatInfo ملكية. يحصل على الترميز المكتشف إذا كان قابلاً للتطبيق على تنسيق المستند الحالي. في الوقت الحالي يكتشف الترميز فقط لمستندات HTML.
type: docs
weight: 10
url: /ar/net/aspose.words/fileformatinfo/encoding/
---
## FileFormatInfo.Encoding property

يحصل على الترميز المكتشف إذا كان قابلاً للتطبيق على تنسيق المستند الحالي. في الوقت الحالي يكتشف الترميز فقط لمستندات HTML.

```csharp
public Encoding Encoding { get; }
```

### أمثلة

يوضح كيفية اكتشاف الترميز في ملف html.

```csharp
FileFormatInfo info = FileFormatUtil.DetectFileFormat(MyDir + "Document.html");

Assert.AreEqual(LoadFormat.Html, info.LoadFormat);

// يتم استخدام خاصية الترميز فقط عندما نقوم بإنشاء كائن FileFormatInfo لمستند html.
Assert.AreEqual("Western European (Windows)", info.Encoding.EncodingName);
Assert.AreEqual(1252, info.Encoding.CodePage);
```

### أنظر أيضا

* class [FileFormatInfo](../)
* مساحة الاسم [Aspose.Words](../../fileformatinfo/)
* المجسم [Aspose.Words](../../../)


