---
title: "Aspose::Words::Drawing::Fill::get_Transparency metod"
linktitle: "get_Transparency"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::Fill::get_Transparency metod. Hämtar eller anger graden av transparens för den angivna fyllningen som ett värde mellan 0.0 (opak) och 1.0 (klar) i C++."
type: docs
weight: 21000
url: /sv/cpp/aspose.words.drawing/fill/get_transparency/
---
## Fill::get_Transparency method


Hämtar eller anger transparensgraden för den angivna fyllningen som ett värde mellan 0.0 (opaque) och 1.0 (clear).

```cpp
double Aspose::Words::Drawing::Fill::get_Transparency()
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

* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
