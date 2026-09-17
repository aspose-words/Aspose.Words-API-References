---
title: "Aspose::Words::Drawing::Fill::get_Pattern méthode"
linktitle: "get_Pattern"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::Fill::get_Pattern méthode. Obtient un PatternType pour le remplissage en C++."
type: docs
weight: 17000
url: /fr/cpp/aspose.words.drawing/fill/get_pattern/
---
## Fill::get_Pattern method


Obtient un [PatternType](../../patterntype/) pour le remplissage.

```cpp
Aspose::Words::Drawing::PatternType Aspose::Words::Drawing::Fill::get_Pattern()
```


## Exemples



Montre comment définir un motif pour une forme.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shape stroke pattern border.docx");

auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::Fill> fill = shape->get_Fill();

std::cout << System::String::Format(u"Pattern value is: {0}", fill->get_Pattern()) << std::endl;

// Il existe plusieurs façons de spécifier le remplissage avec un motif.
// 1 -  Appliquer le motif au remplissage de la forme:
fill->Patterned(Aspose::Words::Drawing::PatternType::DiagonalBrick);

// 2 -  Appliquer le motif avec les couleurs de premier plan et d'arrière-plan au remplissage de la forme:
fill->Patterned(Aspose::Words::Drawing::PatternType::DiagonalBrick, System::Drawing::Color::get_Aqua(), System::Drawing::Color::get_Bisque());

doc->Save(get_ArtifactsDir() + u"Shape.FillPattern.docx");
```

## Voir aussi

* Enum [PatternType](../../patterntype/)
* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
