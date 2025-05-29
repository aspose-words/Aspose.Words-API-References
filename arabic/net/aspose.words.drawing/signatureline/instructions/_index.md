---
title: SignatureLine.Instructions
linktitle: Instructions
articleTitle: Instructions
second_title: Aspose.Words لـ .NET
description: اكتشف كيفية تخصيص تعليمات المُوقِّع باستخدام خاصية SignatureLine. حسّن تجربة التوقيع بإضافة إرشادات واضحة ومُخصَّصة.
type: docs
weight: 50
url: /ar/net/aspose.words.drawing/signatureline/instructions/
---
## SignatureLine.Instructions property

يحصل على التعليمات أو يعينها للموقع والتي يتم عرضها عند توقيع سطر التوقيع. يتم تجاهل هذه الخاصية إذا[`DefaultInstructions`](../defaultinstructions/) تم تعيين. القيمة الافتراضية لهذه الخاصية هي**سلسلة فارغة** (Empty ).

```csharp
public string Instructions { get; set; }
```

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

* class [SignatureLine](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
