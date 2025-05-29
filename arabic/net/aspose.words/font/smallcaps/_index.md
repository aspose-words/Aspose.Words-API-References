---
title: Font.SmallCaps
linktitle: SmallCaps
articleTitle: SmallCaps
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية الخط SmallCaps. نسّق النصوص بسهولة بأحرف كبيرة وصغيرة لتحسين سهولة القراءة وإضفاء لمسة أنيقة على تصميماتك.
type: docs
weight: 370
url: /ar/net/aspose.words/font/smallcaps/
---
## Font.SmallCaps property

صحيح إذا تم تنسيق الخط بأحرف كبيرة صغيرة.

```csharp
public bool SmallCaps { get; set; }
```

## أمثلة

يوضح كيفية تنسيق التشغيل لعرض محتوياته بالأحرف الكبيرة.

```csharp
Document doc = new Document();
Paragraph para = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);

// هناك طريقتان لجعل تشغيل ما يعرض نصه بأحرف صغيرة بأحرف كبيرة دون تغيير المحتويات.
// 1 - اضبط علم AllCaps لعرض جميع الأحرف بالأحرف الكبيرة العادية:
Run run = new Run(doc, "all capitals");
run.Font.AllCaps = true;
para.AppendChild(run);

para = (Paragraph)para.ParentNode.AppendChild(new Paragraph(doc));

// 2 - اضبط علم SmallCaps لعرض جميع الأحرف بأحرف كبيرة صغيرة:
// إذا كان الحرف صغيرًا، فسوف يظهر في شكله الكبير
// ولكن سيكون له نفس ارتفاع الأحرف الصغيرة (ارتفاع x للخط).
//الأحرف التي كانت في الأصل بأحرف كبيرة ستبدو متشابهة.
run = new Run(doc, "Small Capitals");
run.Font.SmallCaps = true;
para.AppendChild(run);

doc.Save(ArtifactsDir + "Font.Caps.docx");
```

### أنظر أيضا

* class [Font](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
