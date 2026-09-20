---
title: "Clase Aspose::Words::Loading::ResourceLoadingArgs"
linktitle: "ResourceLoadingArgs"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::Loading::ResourceLoadingArgs. Proporciona datos para el método ResourceLoading() en C++."
type: docs
weight: 7000
url: /es/cpp/aspose.words.loading/resourceloadingargs/
---
## ResourceLoadingArgs class


Proporciona datos para el método [ResourceLoading()](../iresourceloadingcallback/resourceloading/).

```cpp
class ResourceLoadingArgs : public System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_OriginalUri](./get_originaluri/)() const | URI original del recurso según se especifica en el documento importado. |
| [get_ResourceType](./get_resourcetype/)() const | Tipo de recurso. |
| [get_Uri](./get_uri/)() const | URI del recurso que se utiliza para descargar si [ResourceLoading()](../iresourceloadingcallback/resourceloading/) devuelve [Default](../resourceloadingaction/). Inicialmente se establece en la URI absoluta del recurso, pero el usuario puede redefinirla a cualquier valor. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Uri](./set_uri/)(const System::String\&) | Método setter para [Aspose::Words::Loading::ResourceLoadingArgs::get_Uri](./get_uri/). |
| [SetData](./setdata/)(const System::ArrayPtr\<uint8_t\>\&) | Establece los datos proporcionados por el usuario del recurso que se utilizan si [ResourceLoading()](../iresourceloadingcallback/resourceloading/) devuelve [UserProvided](../resourceloadingaction/). |
| static [Type](./type/)() |  |
## Ver también

* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
