---
title: Aspose::Words::Drawing::Fill::get_Transparency method
linktitle: get_Transparency
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::Fill::get_Transparency method. Gets or sets the degree of transparency of the specified fill as a value between 0.0 (opaque) and 1.0 (clear) in C++.'
type: docs
weight: 21000
url: /cpp/aspose.words.drawing/fill/get_transparency/
---
## Fill::get_Transparency method


Gets or sets the degree of transparency of the specified fill as a value between 0.0 (opaque) and 1.0 (clear).

```cpp
double Aspose::Words::Drawing::Fill::get_Transparency()
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

* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
