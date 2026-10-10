---
title: "Método Aspose::Words::Drawing::Fill::get_Color"
linktitle: "get_Color"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Drawing::Fill::get_Color. Obtiene o establece un objeto Color que representa el color de primer plano para el relleno en C++."
type: docs
weight: 5000
url: /es/cpp/aspose.words.drawing/fill/get_color/
---
## Fill::get_Color method


Obtiene o establece un objeto Color que representa el color de primer plano del relleno.

```cpp
System::Drawing::Color Aspose::Words::Drawing::Fill::get_Color()
```


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

* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
