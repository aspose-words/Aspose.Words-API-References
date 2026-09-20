---
title: "Método Aspose::Words::Markup::StructuredDocumentTag::RemoveSelfOnly"
linktitle: "RemoveSelfOnly"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Markup::StructuredDocumentTag::RemoveSelfOnly. Elimina solo este nodo SDT, pero mantiene su contenido dentro del árbol del documento en C++."
type: docs
weight: 37000
url: /es/cpp/aspose.words.markup/structureddocumenttag/removeselfonly/
---
## StructuredDocumentTag::RemoveSelfOnly method


Elimina únicamente este nodo SDT, pero conserva su contenido dentro del árbol del documento.

```cpp
void Aspose::Words::Markup::StructuredDocumentTag::RemoveSelfOnly() override
```


## Ejemplos



Muestra cómo crear una etiqueta de documento estructurado en un cuadro de texto sin formato y modificar su apariencia.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Cree una etiqueta de documento estructurado que contendrá texto sin formato.
auto tag = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Inline);

// Establezca el título y el color del marco que aparece al pasar el mouse sobre la etiqueta de documento estructurado en Microsoft Word.
tag->set_Title(u"My plain text");
tag->set_Color(System::Drawing::Color::get_Magenta());

// Establezca una etiqueta para esta etiqueta de documento estructurado, que es obtenible
// como un elemento XML llamado "tag", con la cadena siguiente en su atributo "@val".
tag->set_Tag(u"MyPlainTextSDT");

// Cada etiqueta de documento estructurado tiene un ID único aleatorio.
ASSERT_TRUE(tag->get_Id() > 0);

// Establezca la fuente del texto dentro de la etiqueta de documento estructurado.
tag->get_ContentsFont()->set_Name(u"Arial");

// Establezca la fuente del texto al final de la etiqueta de documento estructurado.
// Cualquier texto que escribamos en el cuerpo del documento después de salir de la etiqueta con las teclas de flecha usará esta fuente.
tag->get_EndCharacterFont()->set_Name(u"Arial Black");

// Por defecto, esto es false y al presionar Enter mientras está dentro de una etiqueta de documento estructurado no ocurre nada.
// Cuando se establece en true, nuestra etiqueta de documento estructurado puede tener varias líneas.

// Establezca la propiedad "Multiline" en "false" para permitir solo el contenido
// de esta etiqueta de documento estructurado que ocupe una sola línea.
// Establezca la propiedad "Multiline" en "true" para permitir que la etiqueta contenga varias líneas de contenido.
tag->set_Multiline(true);

// Establezca la propiedad "Appearance" en "SdtAppearance.Tags" para mostrar etiquetas alrededor del contenido.
// Por defecto, la etiqueta de documento estructurado se muestra como BoundingBox.
tag->set_Appearance(Aspose::Words::Markup::SdtAppearance::Tags);

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->InsertNode(tag);

// Inserte un clon de nuestra etiqueta de documento estructurado en un nuevo párrafo.
auto tagClone = System::ExplicitCast<Aspose::Words::Markup::StructuredDocumentTag>(System::ExplicitCast<Aspose::Words::Node>(tag)->Clone(true));
builder->InsertParagraph();
builder->InsertNode(tagClone);

// Utilice el método "RemoveSelfOnly" para eliminar una etiqueta de documento estructurado, manteniendo su contenido en el documento.
tagClone->RemoveSelfOnly();

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.PlainText.docx");
```

## Ver también

* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
