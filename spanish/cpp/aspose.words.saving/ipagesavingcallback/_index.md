---
title: "Interfaz Aspose::Words::Saving::IPageSavingCallback"
linktitle: "IPageSavingCallback"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Interfaz Aspose::Words::Saving::IPageSavingCallback. Implemente esta interfaz si desea controlar cómo Aspose.Words guarda páginas separadas al guardar un documento en formatos de página fija en C++."
type: docs
weight: 44000
url: /es/cpp/aspose.words.saving/ipagesavingcallback/
---
## IPageSavingCallback interface


Implemente esta interfaz si desea controlar cómo Aspose.Words guarda páginas separadas al guardar un documento en formatos de página fija.

```cpp
class IPageSavingCallback : public virtual System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [PageSaving](./pagesaving/)(System::SharedPtr\<Aspose::Words::Saving::PageSavingArgs\>) | Se llama cuando Aspose.Words guarda una página separada en formatos de página fija. |
| static [Type](./type/)() |  |
## Ver también

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
