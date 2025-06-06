---
title: Font.Subscript
linktitle: Subscript
articleTitle: Subscript
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية الخط السفلي. نسّق النص بسهولة كخط سفلي لتحسين سهولة القراءة والأناقة في مستنداتك. حسّن تصميمك اليوم!
type: docs
weight: 440
url: /ar/net/aspose.words/font/subscript/
---
## Font.Subscript property

صحيح إذا تم تنسيق الخط على شكل خط منخفض.

```csharp
public bool Subscript { get; set; }
```

## أمثلة

يوضح كيفية تنسيق النص لإزاحة موضعه.

```csharp
Document doc = new Document();
Paragraph para = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);

// ارفع هذا النص بمقدار 5 نقاط فوق خط الأساس.
Run run = new Run(doc, "Raised text. ");
run.Font.Position = 5;
para.AppendChild(run);

// قم بخفض هذا النص بمقدار 10 نقاط أسفل خط الأساس.
run = new Run(doc, "Lowered text. ");
run.Font.Position = -10;
para.AppendChild(run);

//أضف سلسلة من النص العادي.
run = new Run(doc, "Text in its default position. ");
para.AppendChild(run);

//أضف سلسلة من النص تظهر على شكل خط سفلي.
run = new Run(doc, "Subscript. ");
run.Font.Subscript = true;
para.AppendChild(run);

//أضف سلسلة من النص تظهر كنص علوي.
run = new Run(doc, "Superscript.");
run.Font.Superscript = true;
para.AppendChild(run);

doc.Save(ArtifactsDir + "Font.PositionSubscript.docx");
```

### أنظر أيضا

* class [Font](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
