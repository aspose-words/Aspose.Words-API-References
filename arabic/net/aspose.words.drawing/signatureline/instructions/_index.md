---
title: SignatureLine.Instructions
second_title: Aspose.Words لمراجع .NET API
description: SignatureLine ملكية. الحصول على أو تعيين التعليمات للموقّع التي يتم عرضها عند توقيع سطر التوقيع. يتم تجاهل هذه الخاصية إذاDefaultInstructionsتم تعيينها. القيمة الافتراضية لهذه الخاصية هي سلسلة فارغة Empty.
type: docs
weight: 50
url: /ar/net/aspose.words.drawing/signatureline/instructions/
---
## SignatureLine.Instructions property

الحصول على أو تعيين التعليمات للموقّع التي يتم عرضها عند توقيع سطر التوقيع. يتم تجاهل هذه الخاصية إذا[`DefaultInstructions`](../defaultinstructions/)تم تعيينها. القيمة الافتراضية لهذه الخاصية هي **سلسلة فارغة** (Empty).

```csharp
public string Instructions { get; set; }
```

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

* class [SignatureLine](../)
* مساحة الاسم [Aspose.Words.Drawing](../../signatureline/)
* المجسم [Aspose.Words](../../../)


