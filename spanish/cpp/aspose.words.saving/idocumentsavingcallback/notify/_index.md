---
title: "Aspose::Words::Saving::IDocumentSavingCallback::Notify method. Método Notify de Aspose::Words::Saving::IDocumentSavingCallback"
linktitle: "Notificar"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Notify de Aspose::Words::Saving::IDocumentSavingCallback. Se llama para notificar el progreso del guardado del documento en C++."
type: docs
weight: 4000
url: /es/cpp/aspose.words.saving/idocumentsavingcallback/notify/
---
## IDocumentSavingCallback::Notify method


Esto se llama para notificar el progreso del guardado del documento.

```cpp
virtual void Aspose::Words::Saving::IDocumentSavingCallback::Notify(System::SharedPtr<Aspose::Words::Saving::DocumentSavingArgs> args)=0
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| argumentos | System::SharedPtr\<Aspose::Words::Saving::DocumentSavingArgs\> | Un argumento del evento. |
## Observaciones


Los usos principales de esta interfaz son permitir que el código de la aplicación obtenga el estado de progreso y abortar el proceso de guardado.

Se debe lanzar una excepción desde la devolución de llamada de progreso para abortar y debe ser capturada en el código del consumidor.

## Ver también

* Class [DocumentSavingArgs](../../documentsavingargs/)
* Interface [IDocumentSavingCallback](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
