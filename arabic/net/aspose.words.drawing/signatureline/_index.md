---
title: SignatureLine Class
linktitle: SignatureLine
articleTitle: SignatureLine
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Drawing.SignatureLine لإدارة خصائص سطر التوقيع وتخصيصها بسهولة لتحسين أمان المستندات.
type: docs
weight: 1700
url: /ar/net/aspose.words.drawing/signatureline/
---
## SignatureLine class

يوفر الوصول إلى خصائص سطر التوقيع.

لمعرفة المزيد، قم بزيارة[العمل مع التوقيعات الرقمية](https://docs.aspose.com/words/net/working-with-digital-signatures/) مقالة توثيقية.

```csharp
public class SignatureLine
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [AllowComments](../../aspose.words.drawing/signatureline/allowcomments/) { get; set; } | يحصل على قيمة أو يعينها تشير إلى أن المُوقِّع يمكنه إضافة تعليقات في مربع حوار التوقيع. القيمة الافتراضية لهذه الخاصية هي`خطأ شنيع` . |
| [DefaultInstructions](../../aspose.words.drawing/signatureline/defaultinstructions/) { get; set; } | يحصل على قيمة أو يعينها تشير إلى أن التعليمات الافتراضية تظهر في مربع الحوار "التوقيع". القيمة الافتراضية لهذه الخاصية هي`حقيقي` . |
| [Email](../../aspose.words.drawing/signatureline/email/) { get; set; } | يحصل على عنوان البريد الإلكتروني للموقع المقترح أو يعينه. القيمة الافتراضية لهذه الخاصية هي**سلسلة فارغة** (Empty ). |
| [Id](../../aspose.words.drawing/signatureline/id/) { get; set; } | يحصل على معرف لسطر التوقيع هذا أو يعينه. |
| [Instructions](../../aspose.words.drawing/signatureline/instructions/) { get; set; } | يحصل على التعليمات أو يعينها للموقع والتي يتم عرضها عند توقيع سطر التوقيع. يتم تجاهل هذه الخاصية إذا[`DefaultInstructions`](./defaultinstructions/) تم تعيين. القيمة الافتراضية لهذه الخاصية هي**سلسلة فارغة** (Empty ). |
| [IsSigned](../../aspose.words.drawing/signatureline/issigned/) { get; } | يشير إلى أن سطر التوقيع موقّع بالتوقيع الرقمي. |
| [IsValid](../../aspose.words.drawing/signatureline/isvalid/) { get; } | يشير إلى أن سطر التوقيع موقّع بتوقيع رقمي وأن هذا التوقيع الرقمي صالح. |
| [ProviderId](../../aspose.words.drawing/signatureline/providerid/) { get; set; } | يحصل على معرف موفر التوقيع أو يعينه لسطر التوقيع هذا. القيمة الافتراضية هي "{00000000-0000-0000-0000-000000000000}". |
| [ShowDate](../../aspose.words.drawing/signatureline/showdate/) { get; set; } | يحصل على قيمة أو يعينها تشير إلى أن تاريخ التوقيع يظهر في سطر التوقيع. القيمة الافتراضية لهذه الخاصية هي`حقيقي` . |
| [Signer](../../aspose.words.drawing/signatureline/signer/) { get; set; } | يحصل على أو يعين الموقع المقترح لسطر التوقيع. القيمة الافتراضية لهذه الخاصية هي**سلسلة فارغة** (Empty ). |
| [SignerTitle](../../aspose.words.drawing/signatureline/signertitle/) { get; set; } | يحصل على أو يعين عنوان المُوقِّع المقترح (على سبيل المثال، المدير). القيمة الافتراضية لهذه الخاصية هي**سلسلة فارغة** (Empty ). |

## أمثلة

يوضح كيفية إنشاء سطر للتوقيع وإدراجه في مستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

SignatureLineOptions options = new SignatureLineOptions
{
    AllowComments = true,
    DefaultInstructions = true,
    Email = "john.doe@management.com",
    Instructions = "Please sign here",
    ShowDate = true,
    Signer = "John Doe",
    SignerTitle = "Senior Manager"
};

// أدخل شكلاً سيحتوي على خط توقيع، والذي سنحدد مظهره
// قم بالتخصيص باستخدام كائن "SignatureLineOptions" الذي أنشأناه أعلاه.
// إذا قمنا بإدراج شكل تنشأ إحداثياته في الزاوية اليمنى السفلية من الصفحة،
// سوف نحتاج إلى توفير إحداثيات x و y سلبية لإظهار الشكل.
Shape shape = builder.InsertSignatureLine(options, RelativeHorizontalPosition.RightMargin, -170.0,
        RelativeVerticalPosition.BottomMargin, -60.0, WrapType.None);

Assert.True(shape.IsSignatureLine);

// التحقق من خصائص خط التوقيع الخاص بنا عبر كائن الشكل الخاص به.
SignatureLine signatureLine = shape.SignatureLine;

Assert.AreEqual("john.doe@management.com", signatureLine.Email);
Assert.AreEqual("John Doe", signatureLine.Signer);
Assert.AreEqual("Senior Manager", signatureLine.SignerTitle);
Assert.AreEqual("Please sign here", signatureLine.Instructions);
Assert.True(signatureLine.ShowDate);
Assert.True(signatureLine.AllowComments);
Assert.True(signatureLine.DefaultInstructions);

doc.Save(ArtifactsDir + "Shape.SignatureLine.docx");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Drawing](../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../)
