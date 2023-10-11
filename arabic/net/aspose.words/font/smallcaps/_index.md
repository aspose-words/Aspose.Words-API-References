---
title: Font.SmallCaps
second_title: Aspose.Words لمراجع .NET API
description: Font ملكية. صحيح إذا تم تنسيق الخط بأحرف كبيرة صغيرة.
type: docs
weight: 360
url: /ar/net/aspose.words/font/smallcaps/
---
## Font.SmallCaps property

صحيح إذا تم تنسيق الخط بأحرف كبيرة صغيرة.

```csharp
public bool SmallCaps { get; set; }
```

### أمثلة

يوضح كيفية تنسيق التشغيل لعرض محتوياته بالأحرف الكبيرة.

```csharp
Document doc = new Document();
Paragraph para = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);

// هناك طريقتان للتشغيل لعرض النص الصغير بأحرف كبيرة دون تغيير المحتويات.
// 1 - قم بتعيين علامة AllCaps لعرض كافة الأحرف بأحرف كبيرة عادية:
Run run = new Run(doc, "all capitals");
run.Font.AllCaps = true;
para.AppendChild(run);

para = (Paragraph)para.ParentNode.AppendChild(new Paragraph(doc));

// 2 - قم بتعيين علامة SmallCaps لعرض كافة الأحرف بأحرف كبيرة صغيرة:
// إذا كان الحرف صغيرًا، فسوف يظهر بالشكل الكبير
// لكن سيكون له نفس ارتفاع الأحرف الصغيرة (ارتفاع الخط x).
// الأحرف التي كانت بالأحرف الكبيرة في الأصل ستبدو كما هي.
run = new Run(doc, "Small Capitals");
run.Font.SmallCaps = true;
para.AppendChild(run);

doc.Save(ArtifactsDir + "Font.Caps.docx");
```

### أنظر أيضا

* class [Font](../)
* مساحة الاسم [Aspose.Words](../../font/)
* المجسم [Aspose.Words](../../../)


