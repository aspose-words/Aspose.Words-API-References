---
title: Shape.SignatureLine
second_title: Aspose.Words لمراجع .NET API
description: Shape ملكية. يحصلSignatureLine الكائن إذا كان الشكل عبارة عن خط توقيع. عائدات لا شيء خلاف ذلك.
type: docs
weight: 160
url: /ar/net/aspose.words.drawing/shape/signatureline/
---
## Shape.SignatureLine property

يحصل`SignatureLine` الكائن إذا كان الشكل عبارة عن خط توقيع. عائدات **لا شيء** خلاف ذلك.

```csharp
public SignatureLine SignatureLine { get; }
```

### ملاحظات

يمكنك إدراج خطوط التوقيع الجديدة في المستند باستخدام[`InsertSignatureLine`](../../../aspose.words/documentbuilder/insertsignatureline/) و

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

// أدخل شكلًا يحتوي على سطر توقيع ، سنظهر مظهره
// تخصيص باستخدام كائن "SignatureLineOptions" الذي أنشأناه أعلاه.
// إذا أدخلنا شكلًا تنشأ إحداثياته في الركن الأيمن السفلي من الصفحة ،
// سنحتاج إلى توفير إحداثيات سالبة س و ص لإبراز الشكل.
Shape shape = builder.InsertSignatureLine(options, RelativeHorizontalPosition.RightMargin, -170.0, 
        RelativeVerticalPosition.BottomMargin, -60.0, WrapType.None);

Assert.True(shape.IsSignatureLine);

// تحقق من خصائص خط التوقيع الخاص بنا عبر كائن الشكل الخاص به.
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
* مساحة الاسم [Aspose.Words.Drawing](../../shape/)
* المجسم [Aspose.Words](../../../)


