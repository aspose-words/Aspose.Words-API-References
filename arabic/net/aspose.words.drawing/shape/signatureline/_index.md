---
title: Shape.SignatureLine
linktitle: SignatureLine
articleTitle: SignatureLine
second_title: Aspose.Words لـ .NET
description: اكتشف كيفية الوصول إلى كائن SignatureLine لأشكالك. تعرّف بسهولة على خطوط التوقيع، وحسّن من احترافية مستندك!
type: docs
weight: 170
url: /ar/net/aspose.words.drawing/shape/signatureline/
---
## Shape.SignatureLine property

يحصل[`SignatureLine`](../../signatureline/) الكائن إذا كان الشكل عبارة عن سطر توقيع. يُرجع`باطل` وإلا.

```csharp
public SignatureLine SignatureLine { get; }
```

## ملاحظات

يمكنك إدراج جديد[`SignatureLine`](../../signatureline/) في المستند باستخدام[`InsertSignatureLine`](../../../aspose.words/documentbuilder/insertsignatureline/) و

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

* class [SignatureLine](../../signatureline/)
* class [Shape](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
