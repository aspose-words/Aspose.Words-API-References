---
title: "Aspose::Words::Saving::IResourceSavingCallback interface"
linktitle: "IResourceSavingCallback"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::IResourceSavingCallback interface. Implemente esta interfaz si desea controlar cómo Aspose.Words guarda recursos externos (imágenes, fuentes y css) al guardar un documento en HTML o SVG de página fija en C++."
type: docs
weight: 45000
url: /es/cpp/aspose.words.saving/iresourcesavingcallback/
---
## IResourceSavingCallback interface


Implemente esta interfaz si desea controlar cómo Aspose.Words guarda recursos externos (imágenes, fuentes y css) al guardar un documento en HTML o SVG de página fija.

```cpp
class IResourceSavingCallback : public virtual System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [ResourceSaving](./resourcesaving/)(System::SharedPtr\<Aspose::Words::Saving::ResourceSavingArgs\>) | Se llama cuando Aspose.Words guarda un recurso externo en formatos HTML o SVG de página fija. |
| static [Type](./type/)() |  |
## Ver también

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
