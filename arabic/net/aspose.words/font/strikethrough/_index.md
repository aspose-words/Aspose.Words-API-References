---
title: Font.StrikeThrough
linktitle: StrikeThrough
articleTitle: StrikeThrough
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية "خط الشطب". نسّق النصوص بسهولة باستخدام الشطب لإضافة لمسة بصرية واضحة إلى تصاميمك. حسّن سهولة القراءة اليوم!
type: docs
weight: 400
url: /ar/net/aspose.words/font/strikethrough/
---
## Font.StrikeThrough property

صحيح إذا تم تنسيق الخط كنص مشطوب.

```csharp
public bool StrikeThrough { get; set; }
```

## أمثلة

يوضح كيفية إضافة خط مشطوب إلى النص.

```csharp
Document doc = new Document();
Paragraph para = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);

Run run = new Run(doc, "Text with a single-line strikethrough.");
run.Font.StrikeThrough = true;
para.AppendChild(run);

para = (Paragraph)para.ParentNode.AppendChild(new Paragraph(doc));

run = new Run(doc, "Text with a double-line strikethrough.");
run.Font.DoubleStrikeThrough = true;
para.AppendChild(run);

doc.Save(ArtifactsDir + "Font.StrikeThrough.docx");
```

### أنظر أيضا

* class [Font](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
