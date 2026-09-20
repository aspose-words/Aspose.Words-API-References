---
title: "Aspose::Words::Style::get_LinkedStyleName method"
linktitle: "get_LinkedStyleName"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Style::get_LinkedStyleName. Obtiene/establece el nombre del Style vinculado a este. Devuelve una cadena vacía si no hay estilos vinculados en C++."
type: docs
weight: 11000
url: /es/cpp/aspose.words/style/get_linkedstylename/
---
## Style::get_LinkedStyleName method


Obtiene/establece el nombre del [Style](../) vinculado a este. Devuelve una cadena vacía si no hay estilos vinculados.

```cpp
System::String Aspose::Words::Style::get_LinkedStyleName()
```

## Observaciones


Solo se permite vincular el estilo de párrafo al estilo de carácter y viceversa.

Establecer LinkedStyleName para el estilo actual conduce automáticamente a establecer LinkedStyleName para el estilo vinculado.

Asignar una cadena vacía equivale a desvincular el estilo previamente vinculado.

## Ejemplos



Muestra cómo usar los alias de estilo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Style with alias.docx");

// Este documento contiene un estilo llamado "MyStyle,MyStyle Alias 1,MyStyle Alias 2".
// Si el nombre de un estilo tiene varios valores separados por comas, cada cláusula es un alias separado.
System::SharedPtr<Aspose::Words::Style> style = doc->get_Styles()->idx_get(u"MyStyle");
ASPOSE_ASSERT_EQ(System::MakeArray<System::String>({u"MyStyle Alias 1", u"MyStyle Alias 2"}), style->get_Aliases());
ASSERT_EQ(u"Title", style->get_BaseStyleName());
ASSERT_EQ(u"MyStyle Char", style->get_LinkedStyleName());

// Podemos referirnos a un estilo usando su alias, así como su nombre.
ASPOSE_ASSERT_EQ(doc->get_Styles()->idx_get(u"MyStyle Alias 1"), doc->get_Styles()->idx_get(u"MyStyle Alias 2"));

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->MoveToDocumentEnd();
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"MyStyle Alias 1"));
builder->Writeln(u"Hello world!");
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"MyStyle Alias 2"));
builder->Write(u"Hello again!");

ASPOSE_ASSERT_EQ(doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_ParagraphFormat()->get_Style(), doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(1)->get_ParagraphFormat()->get_Style());
```


Muestra cómo vincular estilos entre sí.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::Style> styleHeading1 = doc->get_Styles()->idx_get(Aspose::Words::StyleIdentifier::Heading1);

System::SharedPtr<Aspose::Words::Style> styleHeading1Char = doc->get_Styles()->Add(Aspose::Words::StyleType::Character, u"Heading 1 Char");
styleHeading1Char->get_Font()->set_Name(u"Verdana");
styleHeading1Char->get_Font()->set_Bold(true);
styleHeading1Char->get_Font()->get_Border()->set_LineStyle(Aspose::Words::LineStyle::Dot);
styleHeading1Char->get_Font()->get_Border()->set_LineWidth(15);

styleHeading1->set_LinkedStyleName(u"Heading 1 Char");

ASSERT_EQ(u"Heading 1 Char", styleHeading1->get_LinkedStyleName());
ASSERT_EQ(u"Heading 1", styleHeading1Char->get_LinkedStyleName());
```

## Ver también

* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
