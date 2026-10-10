---
title: "Aspose::Words::Drawing::Fill::get_Color metodo"
linktitle: "get_Color"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::Fill::get_Color metodo. Ottiene o imposta un oggetto Color che rappresenta il colore di primo piano per il riempimento in C++."
type: docs
weight: 5000
url: /it/cpp/aspose.words.drawing/fill/get_color/
---
## Fill::get_Color method


Ottiene o imposta un oggetto Color che rappresenta il colore di primo piano per il riempimento.

```cpp
System::Drawing::Color Aspose::Words::Drawing::Fill::get_Color()
```


## Esempi



Mostra come convertire qualsiasi riempimento in un riempimento solido.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Two color gradient.docx");

// Ottieni l'oggetto Fill per il Font della prima Run.
System::SharedPtr<Aspose::Words::Drawing::Fill> fill = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_Runs()->idx_get(0)->get_Font()->get_Fill();

// Verifica le proprietà Fill del Font.
std::cout << System::String::Format(u"The type of the fill is: {0}", fill->get_FillType()) << std::endl;
std::cout << "The foreground color of the fill is: " << fill->get_ForeColor() << std::endl;
std::cout << "The fill is transparent at " << (fill->get_Transparency() * 100) << "%" << std::endl;

// Cambia il tipo del riempimento in Solid con colore verde uniforme.
fill->Solid();
std::cout << "\nThe fill is changed:" << std::endl;
std::cout << System::String::Format(u"The type of the fill is: {0}", fill->get_FillType()) << std::endl;
std::cout << "The foreground color of the fill is: " << fill->get_ForeColor() << std::endl;
std::cout << "The fill transparency is " << (fill->get_Transparency() * 100) << "%" << std::endl;

doc->Save(get_ArtifactsDir() + u"Drawing.FillSolid.docx");
```

## Vedi anche

* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
