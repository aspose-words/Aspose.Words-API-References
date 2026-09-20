---
title: "Aspose::Words::DocumentBuilder::EndBookmark método"
linktitle: "EndBookmark"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::DocumentBuilder::EndBookmark método. Marca la posición actual en el documento como el final de un marcador en C++."
type: docs
weight: 4000
url: /es/cpp/aspose.words/documentbuilder/endbookmark/
---
## DocumentBuilder::EndBookmark method


Marca la posición actual en el documento como el final de un marcador.

```cpp
System::SharedPtr<Aspose::Words::BookmarkEnd> Aspose::Words::DocumentBuilder::EndBookmark(const System::String &bookmarkName)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| bookmarkName | const System::String\& | Nombre del marcador. |

### ReturnValue

El nodo de fin de marcador que acaba de crearse.
## Observaciones


Los marcadores en un documento pueden superponerse y abarcar cualquier rango. Para crear un marcador válido necesitas llamar tanto a [StartBookmark()](../) como a [EndBookmark()](../) con el mismo parámetro *bookmarkName*.

Los marcadores mal formados o los marcadores con nombres duplicados serán ignorados al guardar el documento.

## Ejemplos



Muestra cómo crear un marcador.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Un marcador válido necesita que el texto del cuerpo del documento esté encerrado por
// nodos BookmarkStart y BookmarkEnd creados con un nombre de marcador coincidente.
builder->StartBookmark(u"MyBookmark");
builder->Writeln(u"Hello world!");
builder->EndBookmark(u"MyBookmark");

ASSERT_EQ(1, doc->get_Range()->get_Bookmarks()->get_Count());
ASSERT_EQ(u"MyBookmark", doc->get_Range()->get_Bookmarks()->idx_get(0)->get_Name());
ASSERT_EQ(u"Hello world!", doc->get_Range()->get_Bookmarks()->idx_get(0)->get_Text().Trim());
```


Muestra cómo insertar un hipervínculo que hace referencia a un marcador local.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->StartBookmark(u"Bookmark1");
builder->Write(u"Bookmarked text. ");
builder->EndBookmark(u"Bookmark1");
builder->Writeln(u"Text outside of the bookmark.");

// Inserta un campo HYPERLINK que enlaza al marcador. Podemos pasar conmutadores de campo
// al método "InsertHyperlink" como parte del argumento que contiene el nombre del marcador referenciado.
builder->get_Font()->set_Color(System::Drawing::Color::get_Blue());
builder->get_Font()->set_Underline(Aspose::Words::Underline::Single);
auto hyperlink = System::ExplicitCast<Aspose::Words::Fields::FieldHyperlink>(builder->InsertHyperlink(u"Link to Bookmark1", u"Bookmark1", true));
hyperlink->set_ScreenTip(u"Hyperlink Tip");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertHyperlinkToLocalBookmark.docx");
```

## Ver también

* Class [BookmarkEnd](../../bookmarkend/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
