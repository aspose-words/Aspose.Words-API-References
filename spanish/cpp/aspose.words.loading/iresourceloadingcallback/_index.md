---
title: "Aspose::Words::Loading::IResourceLoadingCallback interface"
linktitle: "IResourceLoadingCallback"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Loading::IResourceLoadingCallback interface. Implemente esta interfaz si desea controlar cómo Aspose.Words carga recursos externos al importar un documento e insertar imágenes usando DocumentBuilder en C++."
type: docs
weight: 11000
url: /es/cpp/aspose.words.loading/iresourceloadingcallback/
---
## IResourceLoadingCallback interface


Implemente esta interfaz si desea controlar cómo Aspose.Words carga recursos externos al insertar imágenes usando [DocumentBuilder](../../aspose.words/documentbuilder/).

```cpp
class IResourceLoadingCallback : public virtual System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [ResourceLoading](./resourceloading/)(System::SharedPtr\<Aspose::Words::Loading::ResourceLoadingArgs\>) | Se llama cuando Aspose.Words carga cualquier recurso externo. |
| static [Type](./type/)() |  |
## Ver también

* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
