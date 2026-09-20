---
title: "Método Aspose::Words::Markup::StructuredDocumentTag::get_LockContents"
linktitle: "get_LockContents"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Markup::StructuredDocumentTag::get_LockContents. Cuando se establece en true, esta propiedad prohibirá que un usuario edite el contenido de este SDT en C++."
type: docs
weight: 23000
url: /es/cpp/aspose.words.markup/structureddocumenttag/get_lockcontents/
---
## StructuredDocumentTag::get_LockContents method


Cuando se establece en **true**, esta propiedad prohibirá que un usuario edite el contenido de este **SDT**.

```cpp
bool Aspose::Words::Markup::StructuredDocumentTag::get_LockContents() override
```


## Ejemplos



Muestra cómo aplicar restricciones de edición a las etiquetas de documento estructurado.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserte una etiqueta de documento estructurado de texto plano, que actúa como un cuadro de texto que solicita al usuario que lo complete.
auto tag = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Inline);

// Establezca la propiedad "LockContents" a "true" para prohibir al usuario editar el contenido de este cuadro de texto.
tag->set_LockContents(true);
builder->Write(u"The contents of this structured document tag cannot be edited: ");
builder->InsertNode(tag);

tag = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Inline);

// Establezca la propiedad "LockContentControl" a "true" para prohibir al usuario que
// eliminar esta etiqueta de documento estructurado manualmente en Microsoft Word.
tag->set_LockContentControl(true);

builder->InsertParagraph();
builder->Write(u"This structured document tag cannot be deleted but its contents can be edited: ");
builder->InsertNode(tag);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.Lock.docx");
```

## Ver también

* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
