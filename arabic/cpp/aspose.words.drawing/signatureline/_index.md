---
title: "Aspose::Words::Drawing::SignatureLine class"
linktitle: "SignatureLine"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::SignatureLine class. يوفر الوصول إلى خصائص خط التوقيع. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 13000
url: /ar/cpp/aspose.words.drawing/signatureline/
---
## SignatureLine class


يوفر إمكانية الوصول إلى خصائص سطر التوقيع. لمعرفة المزيد، زر مقالة الوثائق [Work with Digital Signatures](https://docs.aspose.com/words/cpp/working-with-digital-signatures/).

```cpp
class SignatureLine : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_AllowComments](./get_allowcomments/)() | يحصل أو يعيّن قيمة تشير إلى أن الموقّع يمكنه إضافة تعليقات في مربع حوار التوقيع. القيمة الافتراضية لهذه الخاصية هي **false** |
| [get_DefaultInstructions](./get_defaultinstructions/)() | يحصل أو يعيّن قيمة تشير إلى أن التعليمات الافتراضية تُعرض في مربع حوار التوقيع. القيمة الافتراضية لهذه الخاصية هي **true**. |
| [get_Email](./get_email/)() | يحصل أو يعيّن عنوان البريد الإلكتروني المقترح للموقّع. القيمة الافتراضية لهذه الخاصية هي **empty string**. |
| [get_Id](./get_id/)() | يحصل أو يضبط المعرف لهذا خط التوقيع. يمكن ربط هذا المعرف بتوقيع رقمي، عند توقيع المستند باستخدام [DigitalSignatureUtil](../../aspose.words.digitalsignatures/digitalsignatureutil/). يجب أن تكون هذه القيمة فريدة وبشكل افتراضي يتم توليد Guid جديد عشوائيًا (**NewGuid**). |
| [get_Instructions](./get_instructions/)() | يحصل أو يعيّن التعليمات للموقع التي تُعرض عند توقيع سطر التوقيع. يتم تجاهل هذه الخاصية إذا تم تعيين [DefaultInstructions](./get_defaultinstructions/). القيمة الافتراضية لهذه الخاصية هي **empty string**. |
| [get_IsSigned](./get_issigned/)() | يشير إلى أن سطر التوقيع موقّع بتوقيع رقمي. |
| [get_IsValid](./get_isvalid/)() | يشير إلى أن سطر التوقيع موقّع بتوقيع رقمي وأن هذا التوقيع الرقمي صالح. |
| [get_ProviderId](./get_providerid/)() | يحصل أو يعيّن معرف موفر التوقيع لهذا سطر التوقيع. القيمة الافتراضية هي "{00000000-0000-0000-0000-000000000000}". |
| [get_ShowDate](./get_showdate/)() | يحصل أو يعيّن قيمة تشير إلى أن تاريخ التوقيع يُعرض في سطر التوقيع. القيمة الافتراضية لهذه الخاصية هي **true**. |
| [get_Signer](./get_signer/)() | يحصل أو يعيّن الموقع المقترح لسطر التوقيع. القيمة الافتراضية لهذه الخاصية هي **empty string**. |
| [get_SignerTitle](./get_signertitle/)() | يحصل أو يعيّن لقب الموقع المقترح (مثال: مدير). القيمة الافتراضية لهذه الخاصية هي **empty string**. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AllowComments](./set_allowcomments/)(bool) | مُعيّن لـ [Aspose::Words::Drawing::SignatureLine::get_AllowComments](./get_allowcomments/). |
| [set_DefaultInstructions](./set_defaultinstructions/)(bool) | مُعيّن لـ [Aspose::Words::Drawing::SignatureLine::get_DefaultInstructions](./get_defaultinstructions/). |
| [set_Email](./set_email/)(const System::String\&) | مُعيّن لـ [Aspose::Words::Drawing::SignatureLine::get_Email](./get_email/). |
| [set_Id](./set_id/)(System::Guid) | مُعيّن لـ [Aspose::Words::Drawing::SignatureLine::get_Id](./get_id/). |
| [set_Instructions](./set_instructions/)(const System::String\&) | مُعيّن لـ [Aspose::Words::Drawing::SignatureLine::get_Instructions](./get_instructions/). |
| [set_ProviderId](./set_providerid/)(System::Guid) | مُعيّن لـ [Aspose::Words::Drawing::SignatureLine::get_ProviderId](./get_providerid/). |
| [set_ShowDate](./set_showdate/)(bool) | مُعيّن لـ [Aspose::Words::Drawing::SignatureLine::get_ShowDate](./get_showdate/). |
| [set_Signer](./set_signer/)(const System::String\&) | مُعيّن لـ [Aspose::Words::Drawing::SignatureLine::get_Signer](./get_signer/). |
| [set_SignerTitle](./set_signertitle/)(const System::String\&) | مُعيّن لـ [Aspose::Words::Drawing::SignatureLine::get_SignerTitle](./get_signertitle/). |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
