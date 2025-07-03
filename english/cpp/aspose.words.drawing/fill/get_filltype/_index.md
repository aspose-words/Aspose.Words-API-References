---
title: Aspose::Words::Drawing::Fill::get_FillType method
linktitle: get_FillType
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::Fill::get_FillType method. Gets a fill type in C++.'
type: docs
weight: 6000
url: /cpp/aspose.words.drawing/fill/get_filltype/
---
## Fill::get_FillType method


Gets a fill type.

```cpp
Aspose::Words::Drawing::FillType Aspose::Words::Drawing::Fill::get_FillType()
```


## Examples



Shows how to convert any of the fills back to solid fill. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Two color gradient.docx");

// Get Fill object for Font of the first Run.
System::SharedPtr<Aspose::Words::Drawing::Fill> fill = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_Runs()->idx_get(0)->get_Font()->get_Fill();

// Check Fill properties of the Font.
std::cout << System::String::Format(u"The type of the fill is: {0}", fill->get_FillType()) << std::endl;
std::cout << "The foreground color of the fill is: " << fill->get_ForeColor() << std::endl;
std::cout << "The fill is transparent at " << (fill->get_Transparency() * 100) << "%" << std::endl;

// Change type of the fill to Solid with uniform green color.
fill->Solid();
std::cout << "\nThe fill is changed:" << std::endl;
std::cout << System::String::Format(u"The type of the fill is: {0}", fill->get_FillType()) << std::endl;
std::cout << "The foreground color of the fill is: " << fill->get_ForeColor() << std::endl;
std::cout << "The fill transparency is " << (fill->get_Transparency() * 100) << "%" << std::endl;

doc->Save(get_ArtifactsDir() + u"Drawing.FillSolid.docx");
```

## See Also

* Enum [FillType](../../filltype/)
* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
