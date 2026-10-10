---
title: "Aspose::Words::IDocumentReaderPlugin interfaz"
linktitle: "IDocumentReaderPlugin"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::IDocumentReaderPlugin interface. Define una interfaz para complementos externos de lectura que pueden leer un archivo en un documento en C++."
type: docs
weight: 77000
url: /es/cpp/aspose.words/idocumentreaderplugin/
---
## IDocumentReaderPlugin interface


Define una interfaz para complementos de lector externos que pueden leer un archivo en un documento.

```cpp
class IDocumentReaderPlugin : public virtual System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Read](./read/)(System::SharedPtr\<System::IO::Stream\>, System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>, System::SharedPtr\<Aspose::Words::Document\>) | Lee los datos del flujo especificado en la instancia de [Document](../document/). |
| static [Type](./type/)() |  |
## Ver también

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
