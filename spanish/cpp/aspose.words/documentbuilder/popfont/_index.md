---
title: "Método Aspose::Words::DocumentBuilder::PopFont"
linktitle: "PopFont"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::DocumentBuilder::PopFont. Recupera el formato de carácter previamente guardado en la pila en C++."
type: docs
weight: 62000
url: /es/cpp/aspose.words/documentbuilder/popfont/
---
## DocumentBuilder::PopFont method


Recupera el formato de carácter guardado previamente en la pila.

```cpp
void Aspose::Words::DocumentBuilder::PopFont()
```


## Ejemplos



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

## Ver también

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
