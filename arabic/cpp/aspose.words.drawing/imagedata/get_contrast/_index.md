---
title: "Aspose::Words::Drawing::ImageData::get_Contrast طريقة"
linktitle: "get_Contrast"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Drawing::ImageData::get_Contrast. يحصل على أو يضبط التباين للصورة المحددة. يجب أن تكون قيمة هذه الخاصية رقماً من 0.0 (أقل تباين) إلى 1.0 (أعلى تباين) في C++."
type: docs
weight: 6000
url: /ar/cpp/aspose.words.drawing/imagedata/get_contrast/
---
## ImageData::get_Contrast method


يحصل أو يضبط التباين للصورة المحددة. يجب أن تكون قيمة هذه الخاصية رقمًا بين 0.0 (أقل تباين) إلى 1.0 (أعلى تباين).

```cpp
double Aspose::Words::Drawing::ImageData::get_Contrast()
```

## ملاحظات


القيمة الافتراضية هي 0.5.

## أمثلة



يعرض كيفية تعديل بيانات صورة الشكل.
```cpp
auto imgSourceDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Images.docx");
auto sourceShape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(imgSourceDoc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->idx_get(0));

auto dstDoc = System::MakeObject<Aspose::Words::Document>();

// استورد شكلاً من المستند المصدر وألحقه بالفقرة الأولى.
auto importedShape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(dstDoc->ImportNode(sourceShape, true));
dstDoc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(importedShape);

// الشكل المستورد يحتوي على صورة. يمكننا الوصول إلى خصائص الصورة والبيانات الخام عبر كائن ImageData.
System::SharedPtr<Aspose::Words::Drawing::ImageData> imageData = importedShape->get_ImageData();
imageData->set_Title(u"Imported Image");

ASSERT_TRUE(imageData->get_HasImage());

// إذا كانت الصورة لا تحتوي على حدود، سيحدد كائن ImageData لون الحد كقيمة فارغة.
ASSERT_EQ(4, imageData->get_Borders()->get_Count());
ASPOSE_ASSERT_EQ(System::Drawing::Color::Empty, imageData->get_Borders()->idx_get(0)->get_Color());

// هذه الصورة لا ترتبط بشكل آخر أو ملف صورة في نظام الملفات المحلي.
ASSERT_FALSE(imageData->get_IsLink());
ASSERT_FALSE(imageData->get_IsLinkOnly());

// تحدد خصائص \"Brightness\" و \"Contrast\" سطوع الصورة وتباينها
// على مقياس من 0 إلى 1، مع القيمة الافتراضية عند 0.5.
imageData->set_Brightness(0.8);
imageData->set_Contrast(1.0);

// القيم المذكورة أعلاه للسطوع والتباين أنشأت صورة ذات الكثير من اللون الأبيض.
// يمكننا اختيار لون باستخدام خاصية ChromaKey لاستبداله بالشفافية، مثل الأبيض.
imageData->set_ChromaKey(System::Drawing::Color::get_White());

// استورد الشكل المصدر مرة أخرى واضبط الصورة على أحادية اللون.
importedShape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(dstDoc->ImportNode(sourceShape, true));
dstDoc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(importedShape);

importedShape->get_ImageData()->set_GrayScale(true);

// استورد الشكل المصدر مرة أخرى لإنشاء صورة ثالثة واضبطها على BiLevel.
// يقوم BiLevel بتعيين كل بكسل إما إلى الأسود أو الأبيض، أيهما أقرب إلى اللون الأصلي.
importedShape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(dstDoc->ImportNode(sourceShape, true));
dstDoc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(importedShape);

importedShape->get_ImageData()->set_BiLevel(true);

// يتم تحديد القص على مقياس من 0 إلى 1. قص جانب بمقدار 0.3
// سيتم قص 30٪ من الصورة على الجانب المقصوص.
importedShape->get_ImageData()->set_CropBottom(0.3);
importedShape->get_ImageData()->set_CropLeft(0.3);
importedShape->get_ImageData()->set_CropTop(0.3);
importedShape->get_ImageData()->set_CropRight(0.3);

dstDoc->Save(get_ArtifactsDir() + u"Drawing.ImageData.docx");
```

## انظر أيضًا

* Class [ImageData](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
