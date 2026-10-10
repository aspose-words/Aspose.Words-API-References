---
title: "Aspose::Words::Drawing::FillType enum"
linktitle: "FillType"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::FillType enum. Especifica el tipo de relleno para un objeto rellenable en C++."
type: docs
weight: 22000
url: /es/cpp/aspose.words.drawing/filltype/
---
## FillType enum


Especifica el tipo de relleno para un objeto rellenable.

```cpp
enum class FillType
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Solid | 1 | Relleno sólido. |
| Con patrón | 2 | Relleno con patrón. |
| Degradado | 3 | Relleno degradado. |
| Con textura | 4 | Relleno con textura. |
| Background | 5 | [Fill](../fill/) es lo mismo que el fondo. |
| Picture | 6 | Relleno de imagen. |


## Ejemplos



Muestra cómo convertir cualquiera de los rellenos de nuevo a relleno sólido.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Two color gradient.docx");

// Obtén el objeto Fill para la Font del primer Run.
System::SharedPtr<Aspose::Words::Drawing::Fill> fill = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_Runs()->idx_get(0)->get_Font()->get_Fill();

// Comprueba las propiedades Fill de la Font.
std::cout << System::String::Format(u"The type of the fill is: {0}", fill->get_FillType()) << std::endl;
std::cout << "The foreground color of the fill is: " << fill->get_ForeColor() << std::endl;
std::cout << "The fill is transparent at " << (fill->get_Transparency() * 100) << "%" << std::endl;

// Cambia el tipo del relleno a Sólido con color verde uniforme.
fill->Solid();
std::cout << "\nThe fill is changed:" << std::endl;
std::cout << System::String::Format(u"The type of the fill is: {0}", fill->get_FillType()) << std::endl;
std::cout << "The foreground color of the fill is: " << fill->get_ForeColor() << std::endl;
std::cout << "The fill transparency is " << (fill->get_Transparency() * 100) << "%" << std::endl;

doc->Save(get_ArtifactsDir() + u"Drawing.FillSolid.docx");
```

## Ver también

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
