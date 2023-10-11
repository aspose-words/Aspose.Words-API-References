---
title: Class SignatureLine
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Drawing.SignatureLine فصل. يوفر الوصول إلى خصائص سطر التوقيع.
type: docs
weight: 1300
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
| [AllowComments](../../aspose.words.drawing/signatureline/allowcomments/) { get; set; } | الحصول على قيمة تشير إلى أنه يمكن للموقع إضافة تعليقات في مربع الحوار "تسجيل" أو تعيينها. القيمة الافتراضية لهذه الخاصية هي`خطأ شنيع` . |
| [DefaultInstructions](../../aspose.words.drawing/signatureline/defaultinstructions/) { get; set; } | الحصول على قيمة أو تعيينها تشير إلى أن التعليمات الافتراضية تظهر في مربع حوار التوقيع. القيمة الافتراضية لهذه الخاصية هي`حقيقي` . |
| [Email](../../aspose.words.drawing/signatureline/email/) { get; set; } | الحصول على عنوان البريد الإلكتروني للمُوقع المقترح أو تعيينه. القيمة الافتراضية لهذه الخاصية هي **سلسلة فارغة** (Empty). |
| [Id](../../aspose.words.drawing/signatureline/id/) { get; set; } | الحصول على المعرف أو تعيينه لسطر التوقيع هذا. |
| [Instructions](../../aspose.words.drawing/signatureline/instructions/) { get; set; } | الحصول على أو تعيين التعليمات للموقّع التي يتم عرضها عند توقيع سطر التوقيع. يتم تجاهل هذه الخاصية إذا[`DefaultInstructions`](./defaultinstructions/)تم تعيينها. القيمة الافتراضية لهذه الخاصية هي **سلسلة فارغة** (Empty). |
| [IsSigned](../../aspose.words.drawing/signatureline/issigned/) { get; } | يشير إلى أن سطر التوقيع موقّع بواسطة التوقيع الرقمي. |
| [IsValid](../../aspose.words.drawing/signatureline/isvalid/) { get; } | يشير إلى أن سطر التوقيع موقّع بواسطة التوقيع الرقمي وأن هذا التوقيع الرقمي صالح. |
| [ProviderId](../../aspose.words.drawing/signatureline/providerid/) { get; set; } | الحصول على أو تعيين معرف موفر التوقيع لسطر التوقيع هذا. القيمة الافتراضية هي "{00000000-0000-0000-0000-000000000000}". |
| [ShowDate](../../aspose.words.drawing/signatureline/showdate/) { get; set; } | الحصول على أو تعيين قيمة تشير إلى أن تاريخ التوقيع يظهر في سطر التوقيع. القيمة الافتراضية لهذه الخاصية هي`حقيقي` . |
| [Signer](../../aspose.words.drawing/signatureline/signer/) { get; set; } | الحصول على أو تعيين الموقّع المقترح لسطر التوقيع. القيمة الافتراضية لهذه الخاصية هي **سلسلة فارغة** (Empty). |
| [SignerTitle](../../aspose.words.drawing/signatureline/signertitle/) { get; set; } | الحصول على أو تعيين عنوان المُوقع المقترح (على سبيل المثال، المدير). القيمة الافتراضية لهذه الخاصية هي **سلسلة فارغة** (Empty). |

### أمثلة

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

// قم بإدراج شكل يحتوي على سطر التوقيع، وسنقوم بمظهره
// التخصيص باستخدام كائن "SignatureLineOptions" الذي أنشأناه أعلاه.
// إذا قمنا بإدراج شكل تقع إحداثياته في الركن الأيمن السفلي من الصفحة،
// سنحتاج إلى توفير إحداثيات x وy السالبة لعرض الشكل.
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


