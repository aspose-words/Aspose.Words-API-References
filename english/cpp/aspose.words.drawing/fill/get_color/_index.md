---
title: get_Color
second_title: Aspose.Words for C++ API Reference
description: 
type: docs
weight: 27
url: /cpp/aspose.words.drawing/fill/get_color/
---
## Fill::get_Color method




```cpp
System::Drawing::Color Aspose::Words::Drawing::Fill::get_Color()
```


## Examples



Shows how to convert any of the fills back to solid fill. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Two color gradient.docx");

// Get Fill object for Font of the first Run.
SharedPtr<Fill> fill = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_Runs()->idx_get(0)->get_Font()->get_Fill();

// Check Fill properties of the Font.
std::cout << String::Format(u"The type of the fill is: {0}", fill->get_FillType()) << std::endl;
std::cout << "The foreground color of the fill is: " << fill->get_ForeColor() << std::endl;
std::cout << "The fill is transparent at " << (fill->get_Transparency() * 100) << "%" << std::endl;

// Change type of the fill to Solid with uniform green color.
fill->Solid(System::Drawing::Color::get_Green());
std::cout << "\nThe fill is changed:" << std::endl;
std::cout << String::Format(u"The type of the fill is: {0}", fill->get_FillType()) << std::endl;
std::cout << "The foreground color of the fill is: " << fill->get_ForeColor() << std::endl;
std::cout << "The fill transparency is " << (fill->get_Transparency() * 100) << "%" << std::endl;

doc->Save(ArtifactsDir + u"Drawing.FillSolid.docx");
```

## See Also

* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words](../../../)
