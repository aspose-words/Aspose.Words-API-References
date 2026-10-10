---
title: "Método Aspose::Words::Loading::IDocumentLoadingCallback::Notify"
linktitle: "Notificar"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Loading::IDocumentLoadingCallback::Notify. Se llama para notificar el progreso de carga del documento en C++."
type: docs
weight: 4000
url: /es/cpp/aspose.words.loading/idocumentloadingcallback/notify/
---
## IDocumentLoadingCallback::Notify method


Esto se llama para notificar el progreso de carga del documento.

```cpp
virtual void Aspose::Words::Loading::IDocumentLoadingCallback::Notify(System::SharedPtr<Aspose::Words::Loading::DocumentLoadingArgs> args)=0
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| argumentos | System::SharedPtr\<Aspose::Words::Loading::DocumentLoadingArgs\> | Un argumento del evento. |
## Observaciones


Los usos principales de esta interfaz son permitir que el código de la aplicación obtenga el estado de progreso y abortar el proceso de carga.

Se debe lanzar una excepción desde la devolución de llamada de progreso para abortar y debe ser capturada en el código del consumidor.

## Ver también

* Class [DocumentLoadingArgs](../../documentloadingargs/)
* Interface [IDocumentLoadingCallback](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
