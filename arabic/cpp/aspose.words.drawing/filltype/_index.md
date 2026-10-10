---
title: "Aspose::Words::Drawing::FillType enum"
linktitle: "FillType"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::FillType enum. يحدد نوع التعبئة لكائن قابل للتعبئة في C++."
type: docs
weight: 22000
url: /ar/cpp/aspose.words.drawing/filltype/
---
## FillType enum


يحدد نوع التعبئة لكائن قابل للتعبئة.

```cpp
enum class FillType
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| Solid | 1 | تعبئة صلبة. |
| منقوش | 2 | تعبئة منقوشة. |
| تدرج | 3 | تعبئة متدرجة. |
| محكم القوام | 4 | تعبئة محكم القوام. |
| Background | 5 | [Fill](../fill/) هو نفسه الخلفية. |
| صورة | 6 | تعبئة صورة. |


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

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
