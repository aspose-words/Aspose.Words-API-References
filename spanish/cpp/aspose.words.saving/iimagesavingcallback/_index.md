---
title: "Interfaz Aspose::Words::Saving::IImageSavingCallback"
linktitle: "IImageSavingCallback"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Interfaz Aspose::Words::Saving::IImageSavingCallback. Implemente esta interfaz si desea controlar cómo Aspose.Words guarda imágenes al guardar un documento en HTML. Puede ser utilizada por otros formatos en C++."
type: docs
weight: 43000
url: /es/cpp/aspose.words.saving/iimagesavingcallback/
---
## IImageSavingCallback interface


Implemente esta interfaz si desea controlar cómo Aspose.Words guarda imágenes al guardar un documento en HTML. Puede ser utilizada por otros formatos.

```cpp
class IImageSavingCallback : public virtual System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| virtual [ImageSaving](./imagesaving/)(System::SharedPtr\<Aspose::Words::Saving::ImageSavingArgs\>) | Se llama cuando Aspose.Words guarda una imagen en HTML. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Ver también

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
