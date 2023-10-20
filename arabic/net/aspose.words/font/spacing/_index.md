---
title: Font.Spacing
linktitle: Spacing
articleTitle: Spacing
second_title: Aspose.Words لـ .NET
description: Font Spacing ملكية. إرجاع أو ضبط التباعد بالنقاط بين الأحرف  في C#.
type: docs
weight: 380
url: /ar/net/aspose.words/font/spacing/
---
## Font.Spacing property

إرجاع أو ضبط التباعد (بالنقاط) بين الأحرف .

```csharp
public double Spacing { get; set; }
```

## أمثلة

يوضح كيفية ضبط القياس الأفقي والتباعد للأحرف.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// إضافة نص وزيادة عرض الأحرف إلى 150%.
builder.Font.Scaling = 150;
builder.Writeln("Wide characters");

// أضف نصًا وأضف 1pt من التباعد الأفقي الإضافي بين كل حرف.
builder.Font.Spacing = 1;
builder.Writeln("Expanded by 1pt");

// إضافة نص وتقريب الأحرف من بعضها البعض بمقدار 1pt.
builder.Font.Spacing = -1;
builder.Writeln("Condensed by 1pt");

doc.Save(ArtifactsDir + "Font.ScalingSpacing.docx");
```

### أنظر أيضا

* class [Font](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
