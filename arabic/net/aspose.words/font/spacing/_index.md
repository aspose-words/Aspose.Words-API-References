---
title: Font.Spacing
linktitle: Spacing
articleTitle: Spacing
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية "تباعد الخطوط" لضبط تباعد الأحرف بسهولة. حسّن سهولة القراءة والتصميم بتحكم دقيق في الطباعة.
type: docs
weight: 390
url: /ar/net/aspose.words/font/spacing/
---
## Font.Spacing property

يعيد أو يضبط المسافة (بالنقاط) بين الأحرف.

```csharp
public double Spacing { get; set; }
```

## أمثلة

يوضح كيفية ضبط المقياس الأفقي والتباعد للأحرف.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

//أضف سلسلة من النص وزد عرض الحرف إلى 150%.
builder.Font.Scaling = 150;
builder.Writeln("Wide characters");

// أضف نصًا ممتدًا وأضف مسافة أفقية إضافية قدرها 1 نقطة بين كل حرف.
builder.Font.Spacing = 1;
builder.Writeln("Expanded by 1pt");

// أضف سلسلة من النص وقرب الأحرف من بعضها البعض بمقدار نقطة واحدة.
builder.Font.Spacing = -1;
builder.Writeln("Condensed by 1pt");

doc.Save(ArtifactsDir + "Font.ScalingSpacing.docx");
```

### أنظر أيضا

* class [Font](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
