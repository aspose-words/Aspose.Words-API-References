---
title: "Aspose::Words::Drawing::TextureAlignment enum"
linktitle: "TextureAlignment"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::TextureAlignment enum. يحدد محاذاة تجانب تعبئة النسيج في C++."
type: docs
weight: 42000
url: /ar/cpp/aspose.words.drawing/texturealignment/
---
## TextureAlignment enum


يحدد محاذاة تجانب تعبئة النسيج.

```cpp
enum class TextureAlignment
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| أعلى اليسار | 0 | محاذاة النسيج أعلى اليسار. |
| أعلى | 1 | محاذاة النسيج أعلى. |
| أعلى اليمين | 2 | محاذاة النسيج أعلى اليمين. |
| يسار | 3 | محاذاة النسيج إلى اليسار. |
| وسط | 4 | محاذاة النسيج إلى الوسط. |
| يمين | 5 | محاذاة النسيج إلى اليمين. |
| أسفل اليسار | 6 | محاذاة النسيج أسفل اليسار. |
| أسفل | 7 | محاذاة النسيج أسفل. |
| أسفل اليمين | 8 | محاذاة النسيج أسفل اليمين. |
| None | 9 | لا محاذاة للنسيج. |


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

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
