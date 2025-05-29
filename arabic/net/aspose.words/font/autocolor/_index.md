---
title: Font.AutoColor
linktitle: AutoColor
articleTitle: AutoColor
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية "اللون التلقائي للخط"، واحصل على لون النص الحالي (أسود أو أبيض) لتعديل الألوان تلقائيًا. حسّن تصميمك بسهولة!
type: docs
weight: 20
url: /ar/net/aspose.words/font/autocolor/
---
## Font.AutoColor property

يعيد اللون المحسوب الحالي للنص (أسود أو أبيض) الذي سيتم استخدامه لـ "اللون التلقائي". إذا لم يكن اللون "تلقائيًا"، فيتم إرجاع[`Color`](../color/) .

```csharp
public Color AutoColor { get; }
```

## ملاحظات

عند استخدام "لون تلقائي" للنص، يُحسب لونه الفعلي تلقائيًا ليكون مقروءًا مع لون الخلفية. عند تغيير لون الخلفية، يتحول لون النص تلقائيًا إلى الأسود أو الأبيض في مايكروسوفت وورد لتحسين وضوحه.

## أمثلة

يوضح كيفية تحسين قابلية القراءة عن طريق تحديد لون النص تلقائيًا استنادًا إلى سطوع خلفيته.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// إذا لم يحدد كائن الخط الخاص بالتشغيل لون النص، فسيتم تلقائيًا
// حدد إما الأسود أو الأبيض اعتمادًا على لون لون الخلفية.
Assert.AreEqual(Color.Empty.ToArgb(), builder.Font.Color.ToArgb());

// اللون الافتراضي للنص هو الأسود. إذا كان لون الخلفية داكنًا، فسيكون من الصعب رؤية النص الأسود.
// لحل هذه المشكلة، ستعرض خاصية AutoColor هذا النص باللون الأبيض.
builder.Font.Shading.BackgroundPatternColor = Color.DarkBlue;

builder.Writeln("The text color automatically chosen for this run is white.");

Assert.AreEqual(Color.White.ToArgb(), doc.FirstSection.Body.Paragraphs[0].Runs[0].Font.AutoColor.ToArgb());

// إذا قمنا بتغيير الخلفية إلى لون فاتح، سيكون اللون الأسود أكثر
//لون النص المناسب هو الأبيض حتى يتم عرض اللون التلقائي باللون الأسود.
builder.Font.Shading.BackgroundPatternColor = Color.LightBlue;

builder.Writeln("The text color automatically chosen for this run is black.");

Assert.AreEqual(Color.Black.ToArgb(), doc.FirstSection.Body.Paragraphs[1].Runs[0].Font.AutoColor.ToArgb());

doc.Save(ArtifactsDir + "Font.SetFontAutoColor.docx");
```

### أنظر أيضا

* class [Font](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
