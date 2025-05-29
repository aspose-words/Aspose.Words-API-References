---
title: PdfSaveOptions.UseCoreFonts
linktitle: UseCoreFonts
articleTitle: UseCoreFonts
second_title: Aspose.Words لـ .NET
description: حسّن ملفات PDF الخاصة بك مع PdfSaveOptions! تحكّم في استبدال الخطوط بخطوط TrueType مثل Arial وTimes New Roman لتحسين جودة المستندات.
type: docs
weight: 330
url: /ar/net/aspose.words.saving/pdfsaveoptions/usecorefonts/
---
## PdfSaveOptions.UseCoreFonts property

يحصل على قيمة أو يعينها لتحديد ما إذا كان سيتم استبدال خطوط TrueType Arial وTimes New Roman و Courier New وSymbol بخطوط PDF Type 1 الأساسية أم لا.

```csharp
public bool UseCoreFonts { get; set; }
```

## ملاحظات

القيمة الافتراضية هي`خطأ شنيع` . عندما يتم تعيين هذه القيمة على`حقيقي` سيتم استبدال الخطوط Arial وTimes New Roman وCourier New وSymbol في مستند PDF بالخطوط الأساسية Type 1 المقابلة.

يجب أن تكون الخطوط الأساسية لملفات PDF، أو مقاييس الخطوط الخاصة بها وخطوط الاستبدال المناسبة، متاحة لأي تطبيق عارض PDF.

يعمل هذا الإعداد فقط مع النص المُشفّر بترميز ANSI (Windows-1252). سيتم كتابة النص غير المُشفّر بترميز ANSI بخط TrueType مُضمّن بغض النظر عن هذا الإعداد.

يتطلب التوافق مع PDF/A وPDF/UA تضمين كافة الخطوط.`خطأ شنيع` سيتم استخدام القيمة تلقائيًا عند الحفظ في PDF/A وPDF/UA.

لا يتم دعم الخطوط الأساسية عند الحفظ بتنسيق PDF 2.0.`خطأ شنيع` سيتم استخدام القيمة تلقائيًا عند الحفظ في PDF 2.0.

هذا الخيار له أولوية أعلى من[`FontEmbeddingMode`](../fontembeddingmode/) خيار.

## أمثلة

يوضح كيفية تمكين/تعطيل استبدال الخط من النوع 1 في PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Courier New";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

// قم بإنشاء كائن "PdfSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" الخاصة بالمستند
// لتعديل كيفية تحويل هذه الطريقة للمستند إلى .PDF.
PdfSaveOptions options = new PdfSaveOptions();
// اضبط خاصية "UseCoreFonts" على "true" لاستبدال بعض الخطوط،
// بما في ذلك الخطين الموجودين في مستندنا، مع ما يعادلهما من نوع PDF 1.
// قم بتعيين خاصية "UseCoreFonts" إلى "false" لعدم تطبيق خطوط PDF Type 1.
options.UseCoreFonts = useCoreFonts;

doc.Save(ArtifactsDir + "PdfSaveOptions.EmbedCoreFonts.pdf", options);
```

### أنظر أيضا

* class [PdfSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
