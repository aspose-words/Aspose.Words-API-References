---
title: "Aspose::Words::Drawing::Fill::get_Pattern metodo"
linktitle: "get_Pattern"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::Fill::get_Pattern metodo. Ottiene un PatternType per il riempimento in C++."
type: docs
weight: 17000
url: /it/cpp/aspose.words.drawing/fill/get_pattern/
---
## Fill::get_Pattern method


Ottiene un [PatternType](../../patterntype/) per il riempimento.

```cpp
Aspose::Words::Drawing::PatternType Aspose::Words::Drawing::Fill::get_Pattern()
```


## Esempi



Mostra come impostare il modello per una forma.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shape stroke pattern border.docx");

auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::Fill> fill = shape->get_Fill();

std::cout << System::String::Format(u"Pattern value is: {0}", fill->get_Pattern()) << std::endl;

// Esistono diversi modi per specificare il riempimento con un modello.
// 1 -  Applica il modello al riempimento della forma:
fill->Patterned(Aspose::Words::Drawing::PatternType::DiagonalBrick);

// 2 -  Applica il modello con colori di primo piano e di sfondo al riempimento della forma:
fill->Patterned(Aspose::Words::Drawing::PatternType::DiagonalBrick, System::Drawing::Color::get_Aqua(), System::Drawing::Color::get_Bisque());

doc->Save(get_ArtifactsDir() + u"Shape.FillPattern.docx");
```

## Vedi anche

* Enum [PatternType](../../patterntype/)
* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
