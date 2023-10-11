---
title: OfficeMath.GetMathRenderer
second_title: Aspose.Words لمراجع .NET API
description: OfficeMath طريقة. إنشاء وإرجاع كائن يمكن استخدامه لتحويل هذه المعادلة إلى صورة.
type: docs
weight: 90
url: /ar/net/aspose.words.math/officemath/getmathrenderer/
---
## OfficeMath.GetMathRenderer method

إنشاء وإرجاع كائن يمكن استخدامه لتحويل هذه المعادلة إلى صورة.

```csharp
public OfficeMathRenderer GetMathRenderer()
```

### قيمة الإرجاع

كائن العارض لهذه المعادلة.

### ملاحظات

هذه الطريقة تستدعي فقط[`OfficeMathRenderer`](../../../aspose.words.rendering/officemathrenderer/) منشئ ويمرر هذا الكائن كمعلمة.

### أمثلة

يوضح كيفية تقديم كائن Office Math إلى ملف صورة في نظام الملفات المحلي.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath math = (OfficeMath)doc.GetChild(NodeType.OfficeMath, 0, true);

// قم بإنشاء كائن "ImageSaveOptions" لتمريره إلى طريقة "حفظ" عارض العقدة لتعديله
// كيفية تحويل عقدة OfficeMath إلى صورة.
ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Png);

// اضبط خاصية "Scale" على 5 لجعل الكائن يصل إلى خمسة أضعاف حجمه الأصلي.
saveOptions.Scale = 5;

math.GetMathRenderer().Save(ArtifactsDir + "Shape.RenderOfficeMath.png", saveOptions);
```

### أنظر أيضا

* class [OfficeMathRenderer](../../../aspose.words.rendering/officemathrenderer/)
* class [OfficeMath](../)
* مساحة الاسم [Aspose.Words.Math](../../officemath/)
* المجسم [Aspose.Words](../../../)


