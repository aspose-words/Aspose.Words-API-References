---
title: Font.AutoColor
second_title: Aspose.Words لمراجع .NET API
description: Font ملكية. إرجاع اللون المحسوب الحالي للنص أسود أو أبيض لاستخدامه في اللون التلقائي. إذا لم يكن اللون تلقائيًا فسيتم إرجاعهColor .
type: docs
weight: 20
url: /ar/net/aspose.words/font/autocolor/
---
## Font.AutoColor property

إرجاع اللون المحسوب الحالي للنص (أسود أو أبيض) لاستخدامه في "اللون التلقائي". إذا لم يكن اللون "تلقائيًا"، فسيتم إرجاعه[`Color`](../color/) .

```csharp
public Color AutoColor { get; }
```

### ملاحظات

عندما يكون للنص "لون تلقائي"، يتم حساب اللون الفعلي للنص تلقائيًا بحيث يكون قابلاً للقراءة مقابل لون الخلفية. عندما تقوم بتغيير لون الخلفية، سيتحول لون النص تلقائيًا إلى الأسود أو الأبيض في برنامج MS Word لزيادة الوضوح إلى أقصى حد.

### أمثلة

يوضح كيفية تحسين إمكانية القراءة عن طريق تحديد لون النص تلقائيًا بناءً على سطوع خلفيته.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// إذا لم يحدد كائن الخط الخاص بالتشغيل لون النص، فسيتم ذلك تلقائيًا
// اختر إما الأسود أو الأبيض حسب لون الخلفية.
Assert.AreEqual(Color.Empty.ToArgb(), builder.Font.Color.ToArgb());

// اللون الافتراضي للنص هو الأسود. إذا كان لون الخلفية داكنًا، فسيكون من الصعب رؤية النص الأسود.
// لحل هذه المشكلة، ستعرض خاصية AutoColor هذا النص باللون الأبيض.
builder.Font.Shading.BackgroundPatternColor = Color.DarkBlue;

builder.Writeln("The text color automatically chosen for this run is white.");

Assert.AreEqual(Color.White.ToArgb(), doc.FirstSection.Body.Paragraphs[0].Runs[0].Font.AutoColor.ToArgb());

// إذا قمنا بتغيير الخلفية إلى لون فاتح، فسيكون اللون الأسود أكثر
// لون النص مناسب أكثر من اللون الأبيض بحيث يعرضه اللون التلقائي باللون الأسود.
builder.Font.Shading.BackgroundPatternColor = Color.LightBlue;

builder.Writeln("The text color automatically chosen for this run is black.");

Assert.AreEqual(Color.Black.ToArgb(), doc.FirstSection.Body.Paragraphs[1].Runs[0].Font.AutoColor.ToArgb());

doc.Save(ArtifactsDir + "Font.SetFontAutoColor.docx");
```

### أنظر أيضا

* class [Font](../)
* مساحة الاسم [Aspose.Words](../../font/)
* المجسم [Aspose.Words](../../../)


