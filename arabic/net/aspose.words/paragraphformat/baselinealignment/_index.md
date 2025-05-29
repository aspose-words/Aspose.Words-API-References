---
title: ParagraphFormat.BaselineAlignment
linktitle: BaselineAlignment
articleTitle: BaselineAlignment
second_title: Aspose.Words لـ .NET
description: قم بتحسين تخطيط النص الخاص بك باستخدام خاصية ParagraphFormat BaselineAlignment، مما يتيح لك التحكم الدقيق في وضع الخط الرأسي لتحسين قابلية القراءة.
type: docs
weight: 40
url: /ar/net/aspose.words/paragraphformat/baselinealignment/
---
## ParagraphFormat.BaselineAlignment property

يحصل على أو يعين الموضع الرأسي للخطوط على السطر.

```csharp
public BaselineAlignment BaselineAlignment { get; set; }
```

## أمثلة

يوضح كيفية تعيين الموضع الرأسي للخطوط على خط ما.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

ParagraphFormat format = doc.FirstSection.Body.Paragraphs[0].ParagraphFormat;
if (format.BaselineAlignment == BaselineAlignment.Auto)
{                
    format.BaselineAlignment = BaselineAlignment.Top;
}

doc.Save(ArtifactsDir + "ParagraphFormat.ParagraphBaselineAlignment.docx");
```

### أنظر أيضا

* enum [BaselineAlignment](../../baselinealignment/)
* class [ParagraphFormat](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
