---
title: "Aspose::Words::Drawing::Fill::get_FillType metod"
linktitle: "get_FillType"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::Fill::get_FillType metod. Hämtar en fyllningstyp i C++."
type: docs
weight: 6000
url: /sv/cpp/aspose.words.drawing/fill/get_filltype/
---
## Fill::get_FillType method


Hämtar en fyllningstyp.

```cpp
Aspose::Words::Drawing::FillType Aspose::Words::Drawing::Fill::get_FillType()
```


## Exempel



Visar hur man konverterar någon av fyllningarna tillbaka till solid fyllning.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Two color gradient.docx");

// Hämta Fill-objekt för Font för den första Run.
System::SharedPtr<Aspose::Words::Drawing::Fill> fill = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_Runs()->idx_get(0)->get_Font()->get_Fill();

// Kontrollera Fill-egenskaperna för Font.
std::cout << System::String::Format(u"The type of the fill is: {0}", fill->get_FillType()) << std::endl;
std::cout << "The foreground color of the fill is: " << fill->get_ForeColor() << std::endl;
std::cout << "The fill is transparent at " << (fill->get_Transparency() * 100) << "%" << std::endl;

// Ändra fyllningstyp till Solid med enhetlig grön färg.
fill->Solid();
std::cout << "\nThe fill is changed:" << std::endl;
std::cout << System::String::Format(u"The type of the fill is: {0}", fill->get_FillType()) << std::endl;
std::cout << "The foreground color of the fill is: " << fill->get_ForeColor() << std::endl;
std::cout << "The fill transparency is " << (fill->get_Transparency() * 100) << "%" << std::endl;

doc->Save(get_ArtifactsDir() + u"Drawing.FillSolid.docx");
```

## Se även

* Enum [FillType](../../filltype/)
* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
