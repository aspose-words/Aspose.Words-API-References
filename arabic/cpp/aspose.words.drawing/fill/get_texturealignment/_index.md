---
title: "طريقة Aspose::Words::Drawing::Fill::get_TextureAlignment"
linktitle: "get_TextureAlignment"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Drawing::Fill::get_TextureAlignment. يحصل أو يضبط محاذاة تعبئة نسيج البلاط في C++."
type: docs
weight: 20000
url: /ar/cpp/aspose.words.drawing/fill/get_texturealignment/
---
## Fill::get_TextureAlignment method


يحصل أو يعيّن محاذاة تعبئة نسيج البلاط.

```cpp
Aspose::Words::Drawing::TextureAlignment Aspose::Words::Drawing::Fill::get_TextureAlignment()
```


## أمثلة



يظهر كيفية ملء وتكرار النسيج داخل الشكل.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 80, 80);

// تطبيق محاذاة النسيج على تعبئة الشكل.
shape->get_Fill()->PresetTextured(Aspose::Words::Drawing::PresetTexture::Canvas);
shape->get_Fill()->set_TextureAlignment(Aspose::Words::Drawing::TextureAlignment::TopRight);

// استخدم خيار الامتثال لتحديد الشكل باستخدام DML إذا كنت تريد الحصول على "TextureAlignment"
// خاصية بعد حفظ المستند.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
saveOptions->set_Compliance(Aspose::Words::Saving::OoxmlCompliance::Iso29500_2008_Strict);

doc->Save(get_ArtifactsDir() + u"Shape.TextureFill.docx", saveOptions);

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Shape.TextureFill.docx");
shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

ASSERT_EQ(Aspose::Words::Drawing::TextureAlignment::TopRight, shape->get_Fill()->get_TextureAlignment());
ASSERT_EQ(Aspose::Words::Drawing::PresetTexture::Canvas, shape->get_Fill()->get_PresetTexture());
```

## انظر أيضًا

* Enum [TextureAlignment](../../texturealignment/)
* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
