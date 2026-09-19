---
title: "Aspose::Words::Drawing::FillType enum"
linktitle: "FillType"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::FillType enum. Specifica il tipo di riempimento per un oggetto riempibile in C++."
type: docs
weight: 22000
url: /it/cpp/aspose.words.drawing/filltype/
---
## FillType enum


Specifica il tipo di riempimento per un oggetto riempibile.

```cpp
enum class FillType
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Solid | 1 | Riempimento solido. |
| Motivo | 2 | Riempimento a motivo. |
| Gradiente | 3 | Riempimento a gradiente. |
| Testurizzato | 4 | Riempimento testurizzato. |
| Background | 5 | [Fill](../fill/) è lo stesso dello sfondo. |
| Picture | 6 | Riempimento immagine. |


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

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
