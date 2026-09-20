---
title: "Método Aspose::Words::Style::get_AutomaticallyUpdate"
linktitle: "get_AutomaticallyUpdate"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Style::get_AutomaticallyUpdate. Especifica si este estilo se redefine automáticamente según el valor apropiado en C++."
type: docs
weight: 4000
url: /es/cpp/aspose.words/style/get_automaticallyupdate/
---
## Style::get_AutomaticallyUpdate method


Especifica si este estilo se redefine automáticamente según el valor apropiado.

```cpp
bool Aspose::Words::Style::get_AutomaticallyUpdate() const
```

## Observaciones


Si el valor de la propiedad se establece en true, MS Word redefine automáticamente el estilo actual cuando se ha cambiado el formato de párrafo apropiado.

La propiedad AutomaticallyUpdate solo se aplica a estilos de párrafo.

El valor predeterminado es **false**.

## Ejemplos



Muestra cómo crear y aplicar un estilo personalizado.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::Style> style = doc->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle");
style->get_Font()->set_Name(u"Times New Roman");
style->get_Font()->set_Size(16);
style->get_Font()->set_Color(System::Drawing::Color::get_Navy());
// Redefinir el estilo automáticamente.
style->set_AutomaticallyUpdate(true);

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Aplica uno de los estilos del documento al párrafo que el generador de documentos está creando.
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"MyStyle"));
builder->Writeln(u"Hello world!");

System::SharedPtr<Aspose::Words::Style> firstParagraphStyle = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Style();

ASPOSE_ASSERT_EQ(style, firstParagraphStyle);

// Elimina nuestro estilo personalizado de la colección de estilos del documento.
doc->get_Styles()->idx_get(u"MyStyle")->Remove();

firstParagraphStyle = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Style();

// Cualquier texto que utilizó un estilo eliminado vuelve al formato predeterminado.
ASSERT_FALSE(doc->get_Styles()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Style>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Style> s)>>([](System::SharedPtr<Aspose::Words::Style> s) -> bool
{
    return s->get_Name() == u"MyStyle";
}))));
ASSERT_EQ(u"Times New Roman", firstParagraphStyle->get_Font()->get_Name());
ASPOSE_ASSERT_EQ(12.0, firstParagraphStyle->get_Font()->get_Size());
ASSERT_EQ(System::Drawing::Color::Empty.ToArgb(), firstParagraphStyle->get_Font()->get_Color().ToArgb());
```

## Ver también

* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
