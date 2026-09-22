---
title: "Aspose::Words::Drawing::ImageData class"
linktitle: "ImageData"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::ImageData class. يعرّف صورة لشكل. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 6000
url: /ar/cpp/aspose.words.drawing/imagedata/
---
## ImageData class


يحدد صورة لشكل. لمعرفة المزيد، زر مقالة الوثائق [Working with Images](https://docs.aspose.com/words/cpp/working-with-images/).

```cpp
class ImageData : public Aspose::Words::IBorderAttrSource
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [FitImageToShape](./fitimagetoshape/)() | يضبط بيانات الصورة لتتناسب مع إطار [Shape](../shape/) بحيث تتطابق نسبة العرض إلى الارتفاع لبيانات الصورة مع نسبة العرض إلى الارتفاع لإطار [Shape](../shape/). |
| [get_BiLevel](./get_bilevel/)() | يحدد ما إذا كانت الصورة ستُعرض بالأبيض والأسود. |
| [get_Borders](./get_borders/)() | يحصل على مجموعة حدود الصورة. الحدود لها تأثير فقط على الصور المضمنة. |
| [get_Brightness](./get_brightness/)() | يحصل أو يضبط سطوع الصورة. يجب أن تكون قيمة هذه الخاصية رقمًا بين 0.0 (أكثر تعتيمًا) إلى 1.0 (أكثر سطوعًا). |
| [get_ChromaKey](./get_chromakey/)() | يحدد قيمة اللون للصورة التي ستُعامل كشفافة. |
| [get_Contrast](./get_contrast/)() | يحصل أو يضبط التباين للصورة المحددة. يجب أن تكون قيمة هذه الخاصية رقمًا بين 0.0 (أقل تباين) إلى 1.0 (أعلى تباين). |
| [get_CropBottom](./get_cropbottom/)() | يحدد جزء إزالة الصورة من الجانب السفلي. |
| [get_CropLeft](./get_cropleft/)() | يحدد جزء إزالة الصورة من الجانب الأيسر. |
| [get_CropRight](./get_cropright/)() | يحدد جزء إزالة الصورة من الجانب الأيمن. |
| [get_CropTop](./get_croptop/)() | يحدد جزء إزالة الصورة من الجانب العلوي. |
| [get_GrayScale](./get_grayscale/)() | يحدد ما إذا كانت الصورة ستُعرض بنمط التدرج الرمادي. |
| [get_HasImage](./get_hasimage/)() | يرجع **true** إذا كان الشكل يحتوي على بايتات صورة أو يربط بصورة. |
| [get_ImageBytes](./get_imagebytes/)() | يحصل أو يعيّن البايتات الخام للصورة المخزنة في الشكل. |
| [get_ImageSize](./get_imagesize/)() | يحصل على المعلومات حول حجم الصورة ودقتها. |
| [get_ImageType](./get_imagetype/)() | يحصل على نوع الصورة. |
| [get_IsLink](./get_islink/)() | يرجع **true** إذا كانت الصورة مرتبطة بالشكل (عند تحديد [SourceFullName](./get_sourcefullname/)). |
| [get_IsLinkOnly](./get_islinkonly/)() | يرجع **true** إذا كانت الصورة مرتبطة ولم تُخزن في المستند. |
| [get_SourceFullName](./get_sourcefullname/)() | يحصل أو يعيّن المسار واسم ملف المصدر للصورة المرتبطة. |
| [get_Title](./get_title/)() | يحدد عنوان الصورة. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Save](./save/)(const System::SharedPtr\<System::IO::Stream\>\&) | يحفظ الصورة في الدفق المحدد. |
| [Save](./save/)(const System::String\&) | يحفظ الصورة في ملف. |
| [Save](./save/)(std::basic_ostream\<CharType, Traits\>\&) |  |
| [set_BiLevel](./set_bilevel/)(bool) | المُعيّن لـ [Aspose::Words::Drawing::ImageData::get_BiLevel](./get_bilevel/). |
| [set_Brightness](./set_brightness/)(double) | المُعيّن لـ [Aspose::Words::Drawing::ImageData::get_Brightness](./get_brightness/). |
| [set_ChromaKey](./set_chromakey/)(System::Drawing::Color) | المُعيّن لـ [Aspose::Words::Drawing::ImageData::get_ChromaKey](./get_chromakey/). |
| [set_Contrast](./set_contrast/)(double) | المُعيّن لـ [Aspose::Words::Drawing::ImageData::get_Contrast](./get_contrast/). |
| [set_CropBottom](./set_cropbottom/)(double) | المُعيّن لـ [Aspose::Words::Drawing::ImageData::get_CropBottom](./get_cropbottom/). |
| [set_CropLeft](./set_cropleft/)(double) | المُعيّن لـ [Aspose::Words::Drawing::ImageData::get_CropLeft](./get_cropleft/). |
| [set_CropRight](./set_cropright/)(double) | المُعيّن لـ [Aspose::Words::Drawing::ImageData::get_CropRight](./get_cropright/). |
| [set_CropTop](./set_croptop/)(double) | المُعيّن لـ [Aspose::Words::Drawing::ImageData::get_CropTop](./get_croptop/). |
| [set_GrayScale](./set_grayscale/)(bool) | المُعيّن لـ [Aspose::Words::Drawing::ImageData::get_GrayScale](./get_grayscale/). |
| [set_ImageBytes](./set_imagebytes/)(const System::ArrayPtr\<uint8_t\>\&) | المُعيّن لـ [Aspose::Words::Drawing::ImageData::get_ImageBytes](./get_imagebytes/). |
| [set_SourceFullName](./set_sourcefullname/)(const System::String\&) | المُعيّن لـ [Aspose::Words::Drawing::ImageData::get_SourceFullName](./get_sourcefullname/). |
| [set_Title](./set_title/)(const System::String\&) | المُعيّن لـ [Aspose::Words::Drawing::ImageData::get_Title](./get_title/). |
| [SetImage](./setimage/)(const System::SharedPtr\<System::Drawing::Image\>\&) | يعيّن الصورة التي يعرضها الشكل. |
| [SetImage](./setimage/)(const System::SharedPtr\<System::IO::Stream\>\&) | يعيّن الصورة التي يعرضها الشكل. |
| [SetImage](./setimage/)(const System::String\&) | يعيّن الصورة التي يعرضها الشكل. |
| [SetImage](./setimage/)(std::basic_istream\<CharType, Traits\>\&) |  |
| [ToByteArray](./tobytearray/)() | يرجع بايتات الصورة لأي صورة بغض النظر عما إذا كانت الصورة مخزنة أو مرتبطة. |
| [ToImage](./toimage/)() | يحصل على الصورة المخزنة في الشكل ككائن **Image**. |
| [ToStream](./tostream/)() | ينشئ ويرجع دفقًا يحتوي على بايتات الصورة. |
| static [Type](./type/)() |  |
## ملاحظات


استخدم خاصية [ImageData](../shape/get_imagedata/) للوصول إلى الصورة داخل الشكل وتعديلها. لا تقوم بإنشاء مثيلات من الفئة [ImageData](./) مباشرةً.

يمكن تخزين صورة داخل الشكل، أو ربطها بملف خارجي أو كليهما (مرتبطة ومخزنة في المستند).

بغض النظر عما إذا كانت الصورة مخزنة داخل الشكل أو مرتبطة، يمكنك دائمًا الوصول إلى الصورة الفعلية باستخدام طرق [ToByteArray](./tobytearray/)، [ToStream](./tostream/)، [ToImage](./toimage/) أو [Save()](../). إذا كانت الصورة مخزنة داخل الشكل، يمكنك أيضًا الوصول إليها مباشرةً باستخدام خاصية [ImageBytes](./get_imagebytes/).

لتخزين صورة داخل الشكل استخدم طريقة [SetImage()](../). لربط صورة بشكل، اضبط خاصية [SourceFullName](./get_sourcefullname/).

## أمثلة



يوضح كيفية استخراج الصور من مستند، وحفظها على نظام الملفات المحلي كملفات منفصلة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Images.docx");

// احصل على مجموعة الأشكال من المستند،
// واحفظ بيانات الصورة لكل شكل يحتوي على صورة كملف على نظام الملفات المحلي.
System::SharedPtr<Aspose::Words::NodeCollection> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true);

ASSERT_EQ(9, shapes->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> s)>>([](System::SharedPtr<Aspose::Words::Node> s) -> bool
{
    return (System::ExplicitCast<Aspose::Words::Drawing::Shape>(s))->get_HasImage();
}))));

int32_t imageIndex = 0;
for (auto&& shape : System::IterateOver(shapes->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()))
{
    if (shape->get_HasImage())
    {
        // قد تحتوي بيانات الصور للأشكال على صور بعدة تنسيقات صورة محتملة.
        // يمكننا تحديد امتداد الملف لكل صورة تلقائيًا بناءً على تنسيقها.
        System::String imageFileName = System::String::Format(u"File.ExtractImages.{0}{1}", imageIndex, Aspose::Words::FileFormatUtil::ImageTypeToExtension(shape->get_ImageData()->get_ImageType()));
        shape->get_ImageData()->Save(get_ArtifactsDir() + imageFileName);
        imageIndex++;
    }
}
```


يوضح كيفية إدراج صورة مرتبطة في مستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::String imageFileName = get_ImageDir() + u"Windows MetaFile.wmf";

// فيما يلي طريقتان لتطبيق صورة على شكل بحيث يمكنه عرضها.
// 1 -  اضبط الشكل ليحتوي على الصورة.
auto shape = System::MakeObject<Aspose::Words::Drawing::Shape>(builder->get_Document(), Aspose::Words::Drawing::ShapeType::Image);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::Inline);
shape->get_ImageData()->SetImage(imageFileName);

builder->InsertNode(shape);

doc->Save(get_ArtifactsDir() + u"Image.CreateLinkedImage.Embedded.docx");

// كل صورة نقوم بتخزينها في الشكل ستزيد من حجم مستندنا.
ASSERT_TRUE(70000 < System::MakeObject<System::IO::FileInfo>(get_ArtifactsDir() + u"Image.CreateLinkedImage.Embedded.docx")->get_Length());

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->RemoveAllChildren();

// 2 -  اضبط الشكل ليرتبط بملف صورة في نظام الملفات المحلي.
shape = System::MakeObject<Aspose::Words::Drawing::Shape>(builder->get_Document(), Aspose::Words::Drawing::ShapeType::Image);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::Inline);
shape->get_ImageData()->set_SourceFullName(imageFileName);

builder->InsertNode(shape);
doc->Save(get_ArtifactsDir() + u"Image.CreateLinkedImage.Linked.docx");

// ربط الصور سيوفر مساحة ويؤدي إلى مستند أصغر.
// مع ذلك، لا يمكن للمستند عرض الصورة بشكل صحيح إلا بينما
// ملف الصورة موجود في الموقع الذي تشير إليه خاصية "SourceFullName" للشكل.
ASSERT_TRUE(10000 > System::MakeObject<System::IO::FileInfo>(get_ArtifactsDir() + u"Image.CreateLinkedImage.Linked.docx")->get_Length());
```

## انظر أيضًا

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
