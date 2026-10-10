---
title: "طريقة Aspose::Words::Drawing::SignatureLine::get_Instructions"
linktitle: "get_Instructions"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Drawing::SignatureLine::get_Instructions. يحصل أو يضبط التعليمات للموقع التي تُعرض عند توقيع خط التوقيع. يتم تجاهل هذه الخاصية إذا تم تعيين DefaultInstructions. القيمة الافتراضية لهذه الخاصية هي سلسلة فارغة في C++."
type: docs
weight: 6000
url: /ar/cpp/aspose.words.drawing/signatureline/get_instructions/
---
## SignatureLine::get_Instructions method


يحصل أو يضبط التعليمات للموقع التي تُعرض عند توقيع خط التوقيع. يتم تجاهل هذه الخاصية إذا تم تعيين [DefaultInstructions](../get_defaultinstructions/). القيمة الافتراضية لهذه الخاصية هي **empty string**.

```cpp
System::String Aspose::Words::Drawing::SignatureLine::get_Instructions()
```


## أمثلة



يعرض كيفية إنشاء سطر للتوقيع وإدراجه في مستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto options = System::MakeObject<Aspose::Words::SignatureLineOptions>();
options->set_AllowComments(true);
options->set_DefaultInstructions(true);
options->set_Email(u"john.doe@management.com");
options->set_Instructions(u"Please sign here");
options->set_ShowDate(true);
options->set_Signer(u"John Doe");
options->set_SignerTitle(u"Senior Manager");

// أدرج شكلاً سيحتوي على سطر توقيع، والذي سنقوم بمظهره
// تخصيصه باستخدام كائن "SignatureLineOptions" الذي أنشأناه أعلاه.
// إذا أدخلنا شكلاً تبدأ إحداثياته من الزاوية السفلية اليمنى للصفحة،
// سنحتاج إلى توفير إحداثيات x و y سالبة لجلب الشكل إلى العرض.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertSignatureLine(options, Aspose::Words::Drawing::RelativeHorizontalPosition::RightMargin, -170.0, Aspose::Words::Drawing::RelativeVerticalPosition::BottomMargin, -60.0, Aspose::Words::Drawing::WrapType::None);

ASSERT_TRUE(shape->get_IsSignatureLine());

// تحقق من خصائص سطر التوقيع الخاص بنا عبر كائن Shape الخاص به.
System::SharedPtr<Aspose::Words::Drawing::SignatureLine> signatureLine = shape->get_SignatureLine();

ASSERT_EQ(u"john.doe@management.com", signatureLine->get_Email());
ASSERT_EQ(u"John Doe", signatureLine->get_Signer());
ASSERT_EQ(u"Senior Manager", signatureLine->get_SignerTitle());
ASSERT_EQ(u"Please sign here", signatureLine->get_Instructions());
ASSERT_TRUE(signatureLine->get_ShowDate());
ASSERT_TRUE(signatureLine->get_AllowComments());
ASSERT_TRUE(signatureLine->get_DefaultInstructions());

doc->Save(get_ArtifactsDir() + u"Shape.SignatureLine.docx");
```

## انظر أيضًا

* Class [SignatureLine](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
