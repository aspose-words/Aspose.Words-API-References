---
title: "Método Aspose::Words::BorderCollection::Equals"
linktitle: "Equals"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::BorderCollection::Equals. Compara colecciones de bordes en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words/bordercollection/equals/
---
## BorderCollection::Equals method


Compara colecciones de bordes.

```cpp
bool Aspose::Words::BorderCollection::Equals(const System::SharedPtr<Aspose::Words::BorderCollection> &brColl)
```


## Ejemplos



Muestra cómo las colecciones de bordes pueden compartir elementos.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Paragraph 1.");
builder->Write(u"Paragraph 2.");

// Dado que utilizamos la misma configuración de borde al crear
// estos párrafos, sus colecciones de bordes comparten los mismos elementos.
System::SharedPtr<Aspose::Words::BorderCollection> firstParagraphBorders = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Borders();
System::SharedPtr<Aspose::Words::BorderCollection> secondParagraphBorders = builder->get_CurrentParagraph()->get_ParagraphFormat()->get_Borders();

for (int32_t i = 0; i < firstParagraphBorders->get_Count(); i++)
{
    ASSERT_TRUE(System::ObjectExt::Equals(firstParagraphBorders->idx_get(i), secondParagraphBorders->idx_get(i)));
    ASSERT_EQ(System::ObjectExt::GetHashCode(firstParagraphBorders->idx_get(i)), System::ObjectExt::GetHashCode(secondParagraphBorders->idx_get(i)));
    ASSERT_FALSE(firstParagraphBorders->idx_get(i)->get_IsVisible());
}

for (auto&& border : System::IterateOver(secondParagraphBorders))
{
    border->set_LineStyle(Aspose::Words::LineStyle::DotDash);
}

// Después de cambiar el estilo de línea de los bordes solo en el segundo párrafo,
// las colecciones de bordes ya no comparten los mismos elementos.
for (int32_t i = 0; i < firstParagraphBorders->get_Count(); i++)
{
    ASSERT_FALSE(System::ObjectExt::Equals(firstParagraphBorders->idx_get(i), secondParagraphBorders->idx_get(i)));
    ASSERT_NE(System::ObjectExt::GetHashCode(firstParagraphBorders->idx_get(i)), System::ObjectExt::GetHashCode(secondParagraphBorders->idx_get(i)));

    // Cambiar la apariencia de un borde vacío lo hace visible.
    ASSERT_TRUE(secondParagraphBorders->idx_get(i)->get_IsVisible());
}

doc->Save(get_ArtifactsDir() + u"Border.SharedElements.docx");
```

## Ver también

* Class [BorderCollection](../)
* Class [BorderCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
