---
title: "Método Aspose::Words::IDocumentReaderPlugin::Read"
linktitle: "Leer"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::IDocumentReaderPlugin::Read. Lee los datos del flujo especificado en la instancia Document en C++."
type: docs
weight: 4000
url: /es/cpp/aspose.words/idocumentreaderplugin/read/
---
## IDocumentReaderPlugin::Read method


Lee los datos del flujo especificado en la instancia [Document](../../document/).

```cpp
virtual void Aspose::Words::IDocumentReaderPlugin::Read(System::SharedPtr<System::IO::Stream> src, System::SharedPtr<Aspose::Words::Loading::LoadOptions> loadOptions, System::SharedPtr<Aspose::Words::Document> document)=0
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| src | System::SharedPtr\<System::IO::Stream\> | El flujo de origen desde el cual leer el documento. |
| loadOptions | System::SharedPtr\<Aspose::Words::Loading::LoadOptions\> | Una opción de carga adicional para cargar el documento. |
| document | System::SharedPtr\<Aspose::Words::Document\> | La instancia de la clase [Document](../../document/) a la que se leerán los datos. Si la instancia contiene contenido, será sobrescrita por los datos del flujo de origen. |

## Ver también

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [Document](../../document/)
* Interface [IDocumentReaderPlugin](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
