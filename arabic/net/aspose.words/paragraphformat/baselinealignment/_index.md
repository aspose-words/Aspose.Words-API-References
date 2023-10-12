---
title: ParagraphFormat.BaselineAlignment
second_title: Aspose.Words لمراجع .NET API
description: ParagraphFormat ملكية. الحصول على أو تعيين الوضع الرأسي للخطوط على السطر.
type: docs
weight: 40
url: /ar/net/aspose.words/paragraphformat/baselinealignment/
---
## ParagraphFormat.BaselineAlignment property

الحصول على أو تعيين الوضع الرأسي للخطوط على السطر.

```csharp
public BaselineAlignment BaselineAlignment { get; set; }
```

### أمثلة

يوضح كيفية ضبط الوضع الرأسي للخطوط على السطر.

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
* مساحة الاسم [Aspose.Words](../../paragraphformat/)
* المجسم [Aspose.Words](../../../)


