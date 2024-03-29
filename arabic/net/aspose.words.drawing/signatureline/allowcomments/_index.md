---
title: SignatureLine.AllowComments
linktitle: AllowComments
articleTitle: AllowComments
second_title: Aspose.Words لـ .NET
description: SignatureLine AllowComments ملكية. الحصول على قيمة تشير إلى أنه يمكن للموقع إضافة تعليقات في مربع الحوار تسجيل أو تعيينها. القيمة الافتراضية لهذه الخاصية هيخطأ شنيع  في C#.
type: docs
weight: 10
url: /ar/net/aspose.words.drawing/signatureline/allowcomments/
---
## SignatureLine.AllowComments property

الحصول على قيمة تشير إلى أنه يمكن للموقع إضافة تعليقات في مربع الحوار "تسجيل" أو تعيينها. القيمة الافتراضية لهذه الخاصية هي`خطأ شنيع` .

```csharp
public bool AllowComments { get; set; }
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
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
