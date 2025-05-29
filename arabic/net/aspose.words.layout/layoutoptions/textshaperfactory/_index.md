---
title: LayoutOptions.TextShaperFactory
linktitle: TextShaperFactory
articleTitle: TextShaperFactory
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية TextShaperFactory في LayoutOptions للطباعة المتقدمة. حسّن عرضك باستخدام تطبيقات ITextShaperFactory القابلة للتخصيص.
type: docs
weight: 100
url: /ar/net/aspose.words.layout/layoutoptions/textshaperfactory/
---
## LayoutOptions.TextShaperFactory property

يحصل أو يعين[`ITextShaperFactory`](../../../aspose.words.shaping/itextshaperfactory/) التنفيذ المستخدم لميزات عرض الطباعة المتقدمة.

```csharp
public ITextShaperFactory TextShaperFactory { get; set; }
```

## أمثلة

يوضح كيفية دعم ميزات OpenType باستخدام محرك تشكيل النص HarfBuzz.

```csharp
Document doc = new Document(MyDir + "OpenType text shaping.docx");

// يمكن لـ Aspose.Words استخدام كائنات تشكيل النص المقدمة خارجيًا،
// والتي تمثل الخطوط وتحسب معلومات التشكيل للنص.
// يعد مصنع تشكيل النص ضروريًا للمستندات التي تستخدم خطوطًا متعددة.
// عندما يتم تعيين مصنع تشكيل النص، يستخدم التخطيط ميزات OpenType.
// تقوم خاصية Instance بإرجاع كائن BasicTextShaperCache ثابت يلف HarfBuzzTextShaperFactory.
doc.LayoutOptions.TextShaperFactory = HarfBuzzTextShaperFactory.Instance;

// حاليًا، يتم تنفيذ تشكيل النص عند التصدير إلى تنسيقات PDF أو XPS.
doc.Save(ArtifactsDir + "Document.OpenType.pdf");
```

### أنظر أيضا

* interface [ITextShaperFactory](../../../aspose.words.shaping/itextshaperfactory/)
* class [LayoutOptions](../)
* مساحة الاسم [Aspose.Words.Layout](../../../aspose.words.layout/)
* المجسم [Aspose.Words](../../../)
