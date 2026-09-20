---
title: "Método Aspose::Words::DocumentBuilder::InsertDocumentInline"
linktitle: "InsertDocumentInline"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::DocumentBuilder::InsertDocumentInline. Inserta un documento en línea en la posición del cursor en C++."
type: docs
weight: 33500
url: /es/cpp/aspose.words/documentbuilder/insertdocumentinline/
---
## DocumentBuilder::InsertDocumentInline method


Inserta un documento en línea en la posición del cursor.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::DocumentBuilder::InsertDocumentInline(const System::SharedPtr<Aspose::Words::Document> &srcDoc, Aspose::Words::ImportFormatMode importFormatMode, const System::SharedPtr<Aspose::Words::ImportFormatOptions> &importFormatOptions)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| srcDoc | const System::SharedPtr\<Aspose::Words::Document\>\& | Documento fuente para insertar. |
| importFormatMode | Aspose::Words::ImportFormatMode | Especifica cómo combinar el formato de estilo que entra en conflicto. |
| importFormatOptions | const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\& | Permite especificar opciones que afectan el formato de un documento resultante. |

### ReturnValue

Primer nodo del contenido insertado.
## Observaciones


Este método imita el comportamiento de MS Word, como si se presionara CTRL+'A' (seleccionar todo el contenido), luego CTRL+'C' (copiar lo seleccionado al portapapeles) en un documento y después CTRL+'V' (insertar contenido del portapapeles) en otro documento.

A diferencia de [InsertDocument()](../), este método mueve el contenido del párrafo del documento de destino, antes del cual se inserta el documento fuente, al último párrafo del documento fuente insertado. En realidad, esto significa que el salto de párrafo del último párrafo insertado se elimina.

Nota: si el último nodo del documento fuente no es un párrafo, no se realizará ninguna acción.

## Ejemplos



Muestra cómo insertar un documento en línea en la posición del cursor.
```cpp
auto srcDoc = System::MakeObject<Aspose::Words::DocumentBuilder>();
srcDoc->Write(u"[src content]");

// Cree el documento de destino.
auto dstDoc = System::MakeObject<Aspose::Words::DocumentBuilder>();
dstDoc->Write(u"Before ");
dstDoc->InsertNode(System::MakeObject<Aspose::Words::BookmarkStart>(dstDoc->get_Document(), u"src_place"));
dstDoc->InsertNode(System::MakeObject<Aspose::Words::BookmarkEnd>(dstDoc->get_Document(), u"src_place"));
dstDoc->Write(u" after");

ASSERT_EQ(u"Before  after", dstDoc->get_Document()->GetText().TrimEnd(System::MakeObject<System::Array<char16_t>>(0)));

// Inserte el documento fuente en el destino en línea.
dstDoc->MoveToBookmark(u"src_place");
dstDoc->InsertDocumentInline(srcDoc->get_Document(), Aspose::Words::ImportFormatMode::UseDestinationStyles, System::MakeObject<Aspose::Words::ImportFormatOptions>());

ASSERT_EQ(u"Before [src content] after", dstDoc->get_Document()->GetText().TrimEnd(System::MakeObject<System::Array<char16_t>>(0)));
```

## Ver también

* Class [Node](../../node/)
* Class [Document](../../document/)
* Enum [ImportFormatMode](../../importformatmode/)
* Class [ImportFormatOptions](../../importformatoptions/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
