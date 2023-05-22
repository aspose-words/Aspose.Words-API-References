---
title: Aspose::Words::Drawing::Fill::Solid method
linktitle: Solid
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::Fill::Solid method. Sets the fill to a uniform color in C++.'
type: docs
weight: 43000
url: /cpp/aspose.words.drawing/fill/solid/
---
## Fill::Solid() method


Sets the fill to a uniform color.

```cpp
void Aspose::Words::Drawing::Fill::Solid()
```

## See Also

* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
## Fill::Solid(System::Drawing::Color) method


Sets the fill to a specified uniform color.

```cpp
void Aspose::Words::Drawing::Fill::Solid(System::Drawing::Color color)
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
* Library [Aspose.Words for C++](../../../)
