---
title: OfficeMath.GetMathRenderer
linktitle: GetMathRenderer
articleTitle: GetMathRenderer
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة GetMathRenderer الخاصة بـ OfficeMath لتحويل المعادلات إلى صور بسهولة، وتحسين مستنداتك باستخدام صور واضحة واحترافية.
type: docs
weight: 90
url: /ar/net/aspose.words.math/officemath/getmathrenderer/
---
## OfficeMath.GetMathRenderer method

ينشئ ويعيد كائنًا يمكن استخدامه لعرض هذه المعادلة في صورة.

```csharp
public OfficeMathRenderer GetMathRenderer()
```

### قيمة الإرجاع

كائن العرض لهذه المعادلة.

## ملاحظات

هذه الطريقة تستدعي فقط[`OfficeMathRenderer`](../../../aspose.words.rendering/officemathrenderer/) المنشئ ويمرر هذا الكائن كمعلمة.

## أمثلة

يوضح كيفية تحويل كائن Office Math إلى ملف صورة في نظام الملفات المحلي.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath math = (OfficeMath)doc.GetChild(NodeType.OfficeMath, 0, true);

// قم بإنشاء كائن "ImageSaveOptions" لتمريره إلى طريقة "Save" الخاصة بمقدم العقدة لتعديلها
// كيف يتم تحويل عقدة OfficeMath إلى صورة.
ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Png);

// اضبط خاصية "المقياس" على 5 لجعل الكائن أكبر بخمس مرات من حجمه الأصلي.
saveOptions.Scale = 5;

math.GetMathRenderer().Save(ArtifactsDir + "Shape.RenderOfficeMath.png", saveOptions);
```

### أنظر أيضا

* class [OfficeMathRenderer](../../../aspose.words.rendering/officemathrenderer/)
* class [OfficeMath](../)
* مساحة الاسم [Aspose.Words.Math](../../../aspose.words.math/)
* المجسم [Aspose.Words](../../../)
