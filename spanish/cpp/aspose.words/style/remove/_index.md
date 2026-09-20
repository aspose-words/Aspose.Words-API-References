---
title: "Método Aspose::Words::Style::Remove"
linktitle: "Remove"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Style::Remove. Elimina el estilo especificado del documento en C++."
type: docs
weight: 22000
url: /es/cpp/aspose.words/style/remove/
---
## Style::Remove method


Elimina el estilo especificado del documento.

```cpp
void Aspose::Words::Style::Remove()
```

## Observaciones


[Style](../) removal has following effects on the document model:

* All references to the style are removed from corresponding paragraphs, runs and tables.
* If base style is removed its formatting is moved to child styles.
* If style to be deleted has a linked style, then both of these are deleted.



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
