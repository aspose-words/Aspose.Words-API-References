---
title: "Aspose::Words::Saving::IDocumentSavingCallback interfaz"
linktitle: "IDocumentSavingCallback"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::IDocumentSavingCallback interfaz. Implemente esta interfaz si desea tener su propio método personalizado llamado durante el guardado de un documento en C++."
type: docs
weight: 41000
url: /es/cpp/aspose.words.saving/idocumentsavingcallback/
---
## IDocumentSavingCallback interface


Implemente esta interfaz si desea tener su propio método personalizado llamado durante el guardado de un documento.

```cpp
class IDocumentSavingCallback : public virtual System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Notify](./notify/)(System::SharedPtr\<Aspose::Words::Saving::DocumentSavingArgs\>) | Esto se llama para notificar el progreso del guardado del documento. |
| static [Type](./type/)() |  |
## Ver también

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
