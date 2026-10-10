---
title: "طريقة Aspose::Words::Drawing::Fill::get_Color"
linktitle: "get_Color"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Drawing::Fill::get_Color. تحصل أو تعيّن كائن Color الذي يمثل لون المقدمة للتعبئة في C++."
type: docs
weight: 5000
url: /ar/cpp/aspose.words.drawing/fill/get_color/
---
## Fill::get_Color method


يحصل أو يعيّن كائن Color الذي يمثل لون المقدمة للتعبئة.

```cpp
System::Drawing::Color Aspose::Words::Drawing::Fill::get_Color()
```


## أمثلة



يظهر كيفية تحويل أي من التعبئات إلى تعبئة صلبة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Two color gradient.docx");

// احصل على كائن Fill للخط من الـ Run الأول.
System::SharedPtr<Aspose::Words::Drawing::Fill> fill = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_Runs()->idx_get(0)->get_Font()->get_Fill();

// تحقق من خصائص Fill للخط.
std::cout << System::String::Format(u"The type of the fill is: {0}", fill->get_FillType()) << std::endl;
std::cout << "The foreground color of the fill is: " << fill->get_ForeColor() << std::endl;
std::cout << "The fill is transparent at " << (fill->get_Transparency() * 100) << "%" << std::endl;

// غيّر نوع التعبئة إلى صلبة بلون أخضر موحد.
fill->Solid();
std::cout << "\nThe fill is changed:" << std::endl;
std::cout << System::String::Format(u"The type of the fill is: {0}", fill->get_FillType()) << std::endl;
std::cout << "The foreground color of the fill is: " << fill->get_ForeColor() << std::endl;
std::cout << "The fill transparency is " << (fill->get_Transparency() * 100) << "%" << std::endl;

doc->Save(get_ArtifactsDir() + u"Drawing.FillSolid.docx");
```

## انظر أيضًا

* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
