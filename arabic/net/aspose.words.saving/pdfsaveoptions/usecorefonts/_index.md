---
title: PdfSaveOptions.UseCoreFonts
linktitle: UseCoreFonts
articleTitle: UseCoreFonts
second_title: Aspose.Words لـ .NET
description: PdfSaveOptions UseCoreFonts ملكية. الحصول على قيمة أو تعيينها لتحديد ما إذا كان سيتم استبدال خطوط TrueType Arial وTimes New Roman و Courier New وSymbol بخطوط PDF Type 1 الأساسية أم لا في C#.
type: docs
weight: 310
url: /ar/net/aspose.words.saving/pdfsaveoptions/usecorefonts/
---
## PdfSaveOptions.UseCoreFonts property

الحصول على قيمة أو تعيينها لتحديد ما إذا كان سيتم استبدال خطوط TrueType Arial وTimes New Roman و Courier New وSymbol بخطوط PDF Type 1 الأساسية أم لا.

```csharp
public bool UseCoreFonts { get; set; }
```

## ملاحظات

القيمة الافتراضية هي`خطأ شنيع` . عندما يتم ضبط هذه القيمة على`حقيقي` يتم استبدال خطوط Arial وTimes New Roman و Courier New وSymbol في مستند PDF بالخط الأساسي المطابق من النوع 1.

يلزم أن تكون خطوط PDF الأساسية، أو مقاييس الخطوط الخاصة بها والخطوط البديلة المناسبة، متاحة لأي تطبيق عارض PDF.

يعمل هذا الإعداد فقط مع النص بتشفير ANSI (Windows-1252). سيتم كتابة النص بخلاف ANSI بخط TrueType المضمن بغض النظر عن هذا الإعداد.

يتطلب التوافق مع PDF/A وPDF/UA تضمين جميع الخطوط.`خطأ شنيع` سيتم استخدام القيمة تلقائيًا عند الحفظ في PDF/A وPDF/UA.

الخطوط الأساسية غير مدعومة عند الحفظ بتنسيق PDF 2.0.`خطأ شنيع` سيتم استخدام القيمة تلقائيًا عند الحفظ في PDF 2.0.

هذا الخيار له أولوية أعلى بعد ذلك[`FontEmbeddingMode`](../fontembeddingmode/) خيار.

## أمثلة

يوضح كيفية تمكين/تعطيل استبدال خط PDF من النوع 1.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Courier New";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

// قم بإنشاء كائن "PdfSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" المستند
// لتعديل كيفية تحويل هذه الطريقة للمستند إلى .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// اضبط خاصية "UseCoreFonts" على "صحيح" لاستبدال بعض الخطوط،
// بما في ذلك الخطين الموجودين في مستندنا، مع ما يعادلهما في ملف PDF من النوع 1.
// اضبط خاصية "UseCoreFonts" على "خطأ" حتى لا يتم تطبيق خطوط PDF من النوع 1.
options.UseCoreFonts = useCoreFonts;

doc.Save(ArtifactsDir + "PdfSaveOptions.EmbedCoreFonts.pdf", options);

if (useCoreFonts)
    Assert.That(3000, Is.AtLeast(new FileInfo(ArtifactsDir + "PdfSaveOptions.EmbedCoreFonts.pdf").Length));
else
    Assert.That(30000, Is.LessThan(new FileInfo(ArtifactsDir + "PdfSaveOptions.EmbedCoreFonts.pdf").Length));
```

### أنظر أيضا

* class [PdfSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
