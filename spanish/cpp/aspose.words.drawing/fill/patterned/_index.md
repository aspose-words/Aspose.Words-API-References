---
title: "Método Aspose::Words::Drawing::Fill::Patterned"
linktitle: "Con patrón"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Drawing::Fill::Patterned. Establece el relleno especificado a un patrón en C++."
type: docs
weight: 26000
url: /es/cpp/aspose.words.drawing/fill/patterned/
---
## Fill::Patterned(Aspose::Words::Drawing::PatternType) method


Establece el relleno especificado a un patrón.

```cpp
void Aspose::Words::Drawing::Fill::Patterned(Aspose::Words::Drawing::PatternType patternType)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| patternType | Aspose::Words::Drawing::PatternType | [PatternType](../../patterntype/) |

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
## Fill::Patterned(Aspose::Words::Drawing::PatternType, System::Drawing::Color, System::Drawing::Color) method


Establece el relleno especificado a un patrón.

```cpp
void Aspose::Words::Drawing::Fill::Patterned(Aspose::Words::Drawing::PatternType patternType, System::Drawing::Color foreColor, System::Drawing::Color backColor)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| patternType | Aspose::Words::Drawing::PatternType | [PatternType](../../patterntype/) |
| foreColor | System::Drawing::Color | El color del relleno de primer plano. |
| backColor | System::Drawing::Color | El color del relleno de fondo. |

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
