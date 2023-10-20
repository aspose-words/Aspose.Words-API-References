---
title: LayoutOptions.TextShaperFactory
linktitle: TextShaperFactory
articleTitle: TextShaperFactory
second_title: Aspose.Words لـ .NET
description: LayoutOptions TextShaperFactory ملكية. يحصل على أو مجموعاتITextShaperFactory التنفيذ المستخدم لميزات عرض الطباعة المتقدمة في C#.
type: docs
weight: 100
url: /ar/net/aspose.words.layout/layoutoptions/textshaperfactory/
---
## LayoutOptions.TextShaperFactory property

يحصل على أو مجموعات[`ITextShaperFactory`](../../../aspose.words.shaping/itextshaperfactory/) التنفيذ المستخدم لميزات عرض الطباعة المتقدمة.

```csharp
public ITextShaperFactory TextShaperFactory { get; set; }
```

## أمثلة

يوضح كيفية دعم ميزات OpenType باستخدام محرك تشكيل النص HarfBuzz.

```csharp
Document doc = new Document(MyDir + "OpenType text shaping.docx");

// يمكن لـ Aspose.Words استخدام كائنات تشكيل النص المتوفرة خارجيًا،
// التي تمثل الخطوط وتحسب معلومات تشكيل النص.
// يعد مصنع تشكيل النص ضروريًا للمستندات التي تستخدم خطوطًا متعددة.
// عند ضبط مصنع تشكيل النص، يستخدم التخطيط ميزات OpenType.
// تقوم خاصية المثيل بإرجاع كائن BasicTextShaperCache ثابت يغلف HarfBuzzTextShaperFactory.
doc.LayoutOptions.TextShaperFactory = HarfBuzzTextShaperFactory.Instance;

// حاليًا، يتم تنفيذ عملية تشكيل النص عند التصدير إلى تنسيقات PDF أو XPS.
doc.Save(ArtifactsDir + "Document.OpenType.pdf");
```

### أنظر أيضا

* interface [ITextShaperFactory](../../../aspose.words.shaping/itextshaperfactory/)
* class [LayoutOptions](../)
* مساحة الاسم [Aspose.Words.Layout](../../../aspose.words.layout/)
* المجسم [Aspose.Words](../../../)
