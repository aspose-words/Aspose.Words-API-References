---
title: "Método Aspose::Words::DocumentBase::get_Document"
linktitle: "get_Document"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::DocumentBase::get_Document. Obtiene esta instancia en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words/documentbase/get_document/
---
## DocumentBase::get_Document method


Obtiene esta instancia.

```cpp
System::SharedPtr<Aspose::Words::DocumentBase> Aspose::Words::DocumentBase::get_Document() const override
```


## Ejemplos



Muestra cómo crear un documento simple.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Los nuevos objetos Document por defecto vienen con el conjunto mínimo de nodos
// requeridos para comenzar a agregar contenido como texto y formas: una Section, un Body y un Paragraph.
doc->AppendChild<System::SharedPtr<Aspose::Words::Section>>(System::MakeObject<Aspose::Words::Section>(doc))->AppendChild<System::SharedPtr<Aspose::Words::Body>>(System::MakeObject<Aspose::Words::Body>(doc))->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(System::MakeObject<Aspose::Words::Paragraph>(doc))->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));
```

## Ver también

* Class [DocumentBase](../)
* Class [DocumentBase](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
