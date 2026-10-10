---
title: "الفئة Aspose::Words::Saving::SaveOutputParameters"
linktitle: "SaveOutputParameters"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "الفئة Aspose::Words::Saving::SaveOutputParameters. يتم إرجاع هذا الكائن إلى المستدعي بعد حفظ المستند ويحتوي على معلومات إضافية تم إنشاؤها أو حسابها أثناء عملية الحفظ. يمكن للمستدعي استخدام هذا الكائن أو تجاهله. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 30000
url: /ar/cpp/aspose.words.saving/saveoutputparameters/
---
## SaveOutputParameters class


يتم إرجاع هذا الكائن إلى المستدعي بعد حفظ المستند ويحتوي على معلومات إضافية تم إنشاؤها أو حسابها أثناء عملية الحفظ. يمكن للمستدعي استخدام هذا الكائن أو تجاهله. لمعرفة المزيد، قم بزيارة مقالة الوثائق [Save a Document](https://docs.aspose.com/words/cpp/save-a-document/).

```cpp
class SaveOutputParameters : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_ContentType](./get_contenttype/)() const | يعيد سلسلة Content-Type (نوع وسائط الإنترنت) التي تحدد نوع المستند المحفوظ. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

## أمثلة



يوضح كيفية الوصول إلى معلمات الإخراج لعملية حفظ المستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

// بعد حفظ المستند، يمكننا الوصول إلى نوع وسائط الإنترنت (نوع MIME) للمستند الناتج الذي تم إنشاؤه حديثًا.
System::SharedPtr<Aspose::Words::Saving::SaveOutputParameters> parameters = doc->Save(get_ArtifactsDir() + u"Document.SaveOutputParameters.doc");

ASSERT_EQ(u"application/msword", parameters->get_ContentType());

// تتغير هذه الخاصية اعتمادًا على صيغة الحفظ.
parameters = doc->Save(get_ArtifactsDir() + u"Document.SaveOutputParameters.pdf");

ASSERT_EQ(u"application/pdf", parameters->get_ContentType());
```

## انظر أيضًا

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
