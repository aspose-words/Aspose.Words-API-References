---
title: "Aspose::Words::Style::Equals método"
linktitle: "Equals"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Style::Equals método. Compara con el estilo especificado. Los Istds de estilos se comparan solo para estilos incorporados. Los valores predeterminados de estilos no se incluyen en la comparación. El estilo base, el estilo vinculado y el estilo de párrafo siguiente se comparan recursivamente en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words/style/equals/
---
## Style::Equals method


Compara con el estilo especificado. Los Istds de estilos se comparan solo para estilos incorporados. Los valores predeterminados de los estilos no se incluyen en la comparación. El estilo base, el estilo enlazado y el estilo del siguiente párrafo se comparan recursivamente.

```cpp
bool Aspose::Words::Style::Equals(const System::SharedPtr<Aspose::Words::Style> &style)
```


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

## Ver también

* Class [Style](../)
* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
