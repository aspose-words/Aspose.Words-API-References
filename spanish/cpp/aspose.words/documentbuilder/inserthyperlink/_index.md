---
title: "Método Aspose::Words::DocumentBuilder::InsertHyperlink"
linktitle: "InsertHyperlink"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::DocumentBuilder::InsertHyperlink. Inserta un hipervínculo en el documento en C++."
type: docs
weight: 38000
url: /es/cpp/aspose.words/documentbuilder/inserthyperlink/
---
## DocumentBuilder::InsertHyperlink method


Inserta un hipervínculo en el documento.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::DocumentBuilder::InsertHyperlink(const System::String &displayText, const System::String &urlOrBookmark, bool isBookmark)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| displayText | const System::String\& | Texto del enlace que se mostrará en el documento. |
| urlOrBookmark | const System::String\& | Destino del enlace. Puede ser una url o el nombre de un marcador dentro del documento. Este método siempre agrega comillas al principio y al final del url. |
| isBookmark | bool | **true** si el parámetro anterior es el nombre de un marcador dentro del documento; **false** si el parámetro anterior es una URL. |

### ReturnValue

Un objeto [Field](../../../aspose.words.fields/field/) que representa el campo insertado.
## Observaciones


Tenga en cuenta que debe especificar el formato de fuente para el texto de visualización del hipervínculo explícitamente usando la propiedad [Font](../get_font/).

Este método llama internamente a [InsertField()](../) para insertar un campo HYPERLINK de MS Word en el documento.

## Ejemplos



Muestra cómo insertar un campo de hipervínculo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"For more information, please visit the ");

// Inserta un hipervínculo y enfatízalo con formato personalizado.
// El hipervínculo será un fragmento de texto clicable que nos llevará a la ubicación especificada en la URL.
builder->get_Font()->set_Color(System::Drawing::Color::get_Blue());
builder->get_Font()->set_Underline(Aspose::Words::Underline::Single);
builder->InsertHyperlink(u"Google website", u"https://www.google.com", false);
builder->get_Font()->ClearFormatting();
builder->Writeln(u".");

// Ctrl + clic izquierdo en el enlace del texto en Microsoft Word nos llevará a la URL mediante una nueva ventana del navegador web.
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertHyperlink.docx");
```


Muestra cómo usar la pila de formato de un document builder.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Configura el formato de fuente, luego escribe el texto que va antes del hipervínculo.
builder->get_Font()->set_Name(u"Arial");
builder->get_Font()->set_Size(24);
builder->Write(u"To visit Google, hold Ctrl and click ");

// Preserva nuestra configuración de formato actual en la pila.
builder->PushFont();

// Modifica el formato actual del builder aplicando un nuevo estilo.
builder->get_Font()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Hyperlink);
builder->InsertHyperlink(u"here", u"http://www.google.com", false);

ASSERT_EQ(System::Drawing::Color::get_Blue().ToArgb(), builder->get_Font()->get_Color().ToArgb());
ASSERT_EQ(Aspose::Words::Underline::Single, builder->get_Font()->get_Underline());

// Restablece el formato de fuente que guardamos anteriormente y elimina el elemento de la pila.
builder->PopFont();

ASSERT_EQ(System::Drawing::Color::Empty.ToArgb(), builder->get_Font()->get_Color().ToArgb());
ASSERT_EQ(Aspose::Words::Underline::None, builder->get_Font()->get_Underline());

builder->Write(u". We hope you enjoyed the example.");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.PushPopFont.docx");
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

* Class [Field](../../../aspose.words.fields/field/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
