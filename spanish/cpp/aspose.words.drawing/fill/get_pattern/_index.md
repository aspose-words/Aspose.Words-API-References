---
title: "Aspose::Words::Drawing::Fill::get_Pattern método"
linktitle: "get_Pattern"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::Fill::get_Pattern método. Obtiene un PatternType para el relleno en C++."
type: docs
weight: 17000
url: /es/cpp/aspose.words.drawing/fill/get_pattern/
---
## Fill::get_Pattern method


Obtiene un [PatternType](../../patterntype/) para el relleno.

```cpp
Aspose::Words::Drawing::PatternType Aspose::Words::Drawing::Fill::get_Pattern()
```


## Ejemplos



Muestra cómo establecer un patrón para una forma.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shape stroke pattern border.docx");

auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::Fill> fill = shape->get_Fill();

std::cout << System::String::Format(u"Pattern value is: {0}", fill->get_Pattern()) << std::endl;

// Hay varias formas de especificar el relleno con un patrón.
// 1 -  Aplicar patrón al relleno de la forma:
fill->Patterned(Aspose::Words::Drawing::PatternType::DiagonalBrick);

// 2 -  Aplicar patrón con colores de primer plano y de fondo al relleno de la forma:
fill->Patterned(Aspose::Words::Drawing::PatternType::DiagonalBrick, System::Drawing::Color::get_Aqua(), System::Drawing::Color::get_Bisque());

doc->Save(get_ArtifactsDir() + u"Shape.FillPattern.docx");
```

## Ver también

* Enum [PatternType](../../patterntype/)
* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
