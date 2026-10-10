---
title: "Interfaz Aspose::Words::Loading::IDocumentLoadingCallback"
linktitle: "IDocumentLoadingCallback"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Interfaz Aspose::Words::Loading::IDocumentLoadingCallback. Implemente esta interfaz si desea tener su propio método personalizado llamado durante la carga de un documento en C++."
type: docs
weight: 10000
url: /es/cpp/aspose.words.loading/idocumentloadingcallback/
---
## IDocumentLoadingCallback interface


Implemente esta interfaz si desea tener su propio método personalizado llamado durante la carga de un documento.

```cpp
class IDocumentLoadingCallback : public virtual System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Notify](./notify/)(System::SharedPtr\<Aspose::Words::Loading::DocumentLoadingArgs\>) | Esto se llama para notificar el progreso de carga del documento. |
| static [Type](./type/)() |  |
## Ver también

* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
