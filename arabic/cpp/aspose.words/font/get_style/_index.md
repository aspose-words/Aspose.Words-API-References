---
title: "طريقة Aspose::Words::Font::get_Style"
linktitle: "get_Style"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Font::get_Style. يحصل على أو يعيّن نمط الحرف المطبق على هذا التنسيق في C++."
type: docs
weight: 42000
url: /ar/cpp/aspose.words/font/get_style/
---
## Font::get_Style method


الحصول أو تعيين نمط الحرف المطبق على هذا التنسيق.

```cpp
System::SharedPtr<Aspose::Words::Style> Aspose::Words::Font::get_Style()
```


## أمثلة



يطبق خطًا سفليًا مزدوجًا على جميع المقاطع في المستند التي تم تنسيقها بأنماط حرف مخصصة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// أدرج نمطًا مخصصًا وطبقه على النص الذي تم إنشاؤه باستخدام منشئ المستند.
System::SharedPtr<Aspose::Words::Style> style = doc->get_Styles()->Add(Aspose::Words::StyleType::Character, u"MyStyle");
style->get_Font()->set_Color(System::Drawing::Color::get_Red());
style->get_Font()->set_Name(u"Courier New");

builder->get_Font()->set_StyleName(u"MyStyle");
builder->Write(u"This text is in a custom style.");

// تكرّر على كل مقطع وأضف خطًا سفليًا مزدوجًا لكل نمط مخصص.
for (auto&& run : System::IterateOver<Aspose::Words::Run>(doc->GetChildNodes(Aspose::Words::NodeType::Run, true)))
{
    System::SharedPtr<Aspose::Words::Style> charStyle = run->get_Font()->get_Style();

    if (!charStyle->get_BuiltIn())
    {
        run->get_Font()->set_Underline(Aspose::Words::Underline::Double);
    }
}

doc->Save(get_ArtifactsDir() + u"Font.Style.docx");
```

## انظر أيضًا

* Class [Style](../../style/)
* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
