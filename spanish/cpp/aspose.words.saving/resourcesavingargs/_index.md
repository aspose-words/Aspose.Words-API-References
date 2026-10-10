---
title: "Aspose::Words::Saving::ResourceSavingArgs clase"
linktitle: "ResourceSavingArgs"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::ResourceSavingArgs clase. Proporciona datos para el evento ResourceSaving(). Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 27000
url: /es/cpp/aspose.words.saving/resourcesavingargs/
---
## ResourceSavingArgs class


Proporciona datos para el evento [ResourceSaving()](../iresourcesavingcallback/resourcesaving/). Para obtener más información, visite el artículo de documentación [Guardar un documento](https://docs.aspose.com/words/cpp/save-a-document/).

```cpp
class ResourceSavingArgs : public System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_Document](./get_document/)() const | Obtiene el objeto documento que se está guardando actualmente. |
| [get_KeepResourceStreamOpen](./get_keepresourcestreamopen/)() const | Especifica si Aspose.Words debe mantener el flujo abierto o cerrarlo después de guardar un recurso. |
| [get_ResourceFileName](./get_resourcefilename/)() const | Obtiene o establece el nombre de archivo (sin ruta) donde se guardará el recurso. |
| [get_ResourceFileUri](./get_resourcefileuri/)() const | Obtiene o establece el identificador uniforme de recursos (URI) utilizado para referenciar el archivo de recurso desde el documento. |
| [get_ResourceStream](./get_resourcestream/)() const | Permite especificar el flujo donde se guardará el recurso. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_KeepResourceStreamOpen](./set_keepresourcestreamopen/)(bool) | Establecedor para [Aspose::Words::Saving::ResourceSavingArgs::get_KeepResourceStreamOpen](./get_keepresourcestreamopen/). |
| [set_ResourceFileName](./set_resourcefilename/)(const System::String\&) | Establecedor para [Aspose::Words::Saving::ResourceSavingArgs::get_ResourceFileName](./get_resourcefilename/). |
| [set_ResourceFileUri](./set_resourcefileuri/)(const System::String\&) | Establecedor para [Aspose::Words::Saving::ResourceSavingArgs::get_ResourceFileUri](./get_resourcefileuri/). |
| [set_ResourceStream](./set_resourcestream/)(const System::SharedPtr\<System::IO::Stream\>\&) | Establecedor para [Aspose::Words::Saving::ResourceSavingArgs::get_ResourceStream](./get_resourcestream/). |
| [set_ResourceStream](./set_resourcestream/)(std::basic_ostream\<CharType, Traits\>\&) |  |
| static [Type](./type/)() |  |
## Observaciones


Por defecto, cuando Aspose.Words guarda un documento en HTML, SVG o Markdown de página fija, guarda cada recurso en un archivo separado. Aspose.Words utiliza el nombre de archivo del documento y un número único para generar un nombre de archivo único para cada recurso encontrado en el documento.

[ResourceSavingArgs](./) allows to redefine how resource file names are generated or to completely circumvent saving of resources into files by providing your own stream objects.

Para aplicar su propia lógica para generar nombres de archivo de recursos, use la propiedad [ResourceFileName](./get_resourcefilename/).

Para guardar recursos en flujos en lugar de archivos, use la propiedad [ResourceStream](./get_resourcestream/).
## Ver también

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
