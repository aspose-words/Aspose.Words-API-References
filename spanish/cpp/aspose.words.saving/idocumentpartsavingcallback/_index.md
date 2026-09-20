---
title: "Aspose::Words::Saving::IDocumentPartSavingCallback interface"
linktitle: "IDocumentPartSavingCallback"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::IDocumentPartSavingCallback interface. Implemente esta interfaz si desea recibir notificaciones y controlar cómo Aspose.Words guarda las partes del documento al exportar un documento a formato Html o Epub en C++."
type: docs
weight: 40000
url: /es/cpp/aspose.words.saving/idocumentpartsavingcallback/
---
## IDocumentPartSavingCallback interface


Implemente esta interfaz si desea recibir notificaciones y controlar cómo Aspose.Words guarda las partes del documento al exportar un documento a formato [Html](../../aspose.words/saveformat/) o [Epub](../../aspose.words/saveformat/).

```cpp
class IDocumentPartSavingCallback : public virtual System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| virtual [DocumentPartSaving](./documentpartsaving/)(System::SharedPtr\<Aspose::Words::Saving::DocumentPartSavingArgs\>) | Se llama cuando Aspose.Words está a punto de guardar una parte del documento. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Ver también

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
