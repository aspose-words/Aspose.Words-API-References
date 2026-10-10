---
title: "Aspose::Words::Drawing::Fill::get_Pattern-Methode"
linktitle: "get_Pattern"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::Fill::get_Pattern-Methode. Ruft einen PatternType für die Füllung ab in C++."
type: docs
weight: 17000
url: /de/cpp/aspose.words.drawing/fill/get_pattern/
---
## Fill::get_Pattern method


Ruft einen [PatternType](../../patterntype/) für die Füllung ab.

```cpp
Aspose::Words::Drawing::PatternType Aspose::Words::Drawing::Fill::get_Pattern()
```


## Beispiele



Zeigt, wie man ein Muster für eine Form festlegt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shape stroke pattern border.docx");

auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::Fill> fill = shape->get_Fill();

std::cout << System::String::Format(u"Pattern value is: {0}", fill->get_Pattern()) << std::endl;

// Es gibt mehrere Möglichkeiten, eine Füllung mit einem Muster anzugeben.
// 1 -  Muster auf die Formfüllung anwenden:
fill->Patterned(Aspose::Words::Drawing::PatternType::DiagonalBrick);

// 2 -  Muster mit Vorder- und Hintergrundfarben auf die Formfüllung anwenden:
fill->Patterned(Aspose::Words::Drawing::PatternType::DiagonalBrick, System::Drawing::Color::get_Aqua(), System::Drawing::Color::get_Bisque());

doc->Save(get_ArtifactsDir() + u"Shape.FillPattern.docx");
```

## Siehe auch

* Enum [PatternType](../../patterntype/)
* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
