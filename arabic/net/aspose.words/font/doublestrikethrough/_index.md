---
title: Font.DoubleStrikeThrough
linktitle: DoubleStrikeThrough
articleTitle: DoubleStrikeThrough
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية الخط المزدوج. نسّق النص بسهولة باستخدام خط مزدوج لتحسين الوضوح والأناقة في مستنداتك.
type: docs
weight: 90
url: /ar/net/aspose.words/font/doublestrikethrough/
---
## Font.DoubleStrikeThrough property

صحيح إذا تم تنسيق الخط كنص مزدوج الشطب.

```csharp
public bool DoubleStrikeThrough { get; set; }
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
