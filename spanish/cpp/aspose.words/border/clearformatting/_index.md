---
title: "Aspose::Words::Border::ClearFormatting método"
linktitle: "ClearFormatting"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Border::ClearFormatting método. Restablece las propiedades del borde a los valores predeterminados en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words/border/clearformatting/
---
## Border::ClearFormatting method


Restablece las propiedades del borde a los valores predeterminados.

```cpp
void Aspose::Words::Border::ClearFormatting()
```


## Ejemplos



Muestra cómo eliminar bordes de un párrafo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Borders.docx");

// Cada párrafo tiene un conjunto individual de bordes.
// Podemos acceder a la configuración de la apariencia de estos bordes mediante el objeto de formato de párrafo.
System::SharedPtr<Aspose::Words::BorderCollection> borders = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Borders();

ASSERT_EQ(System::Drawing::Color::get_Red().ToArgb(), borders->idx_get(0)->get_Color().ToArgb());
ASPOSE_ASSERT_EQ(3.0, borders->idx_get(0)->get_LineWidth());
ASSERT_EQ(Aspose::Words::LineStyle::Single, borders->idx_get(0)->get_LineStyle());
ASSERT_TRUE(borders->idx_get(0)->get_IsVisible());

// Podemos eliminar un borde de una vez ejecutando el método ClearFormatting.
// Ejecutar este método en cada borde de un párrafo eliminará todos sus bordes.
for (auto&& border : System::IterateOver(borders))
{
    border->ClearFormatting();
}

ASSERT_EQ(System::Drawing::Color::Empty.ToArgb(), borders->idx_get(0)->get_Color().ToArgb());
ASPOSE_ASSERT_EQ(0.0, borders->idx_get(0)->get_LineWidth());
ASSERT_EQ(Aspose::Words::LineStyle::None, borders->idx_get(0)->get_LineStyle());
ASSERT_FALSE(borders->idx_get(0)->get_IsVisible());

doc->Save(get_ArtifactsDir() + u"Border.ClearFormatting.docx");
```

## Ver también

* Class [Border](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
