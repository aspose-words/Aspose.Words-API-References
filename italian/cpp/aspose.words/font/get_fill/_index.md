---
title: "Metodo Aspose::Words::Font::get_Fill"
linktitle: "get_Fill"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Font::get_Fill. Ottiene la formattazione di riempimento per il Font in C++."
type: docs
weight: 15000
url: /it/cpp/aspose.words/font/get_fill/
---
## Font::get_Fill method


Ottiene la formattazione di riempimento per il [Font](../).

```cpp
System::SharedPtr<Aspose::Words::Drawing::Fill> Aspose::Words::Font::get_Fill()
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

* Class [Fill](../../../aspose.words.drawing/fill/)
* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
