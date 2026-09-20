---
title: "Clase Aspose::Words::Saving::DocumentPartSavingArgs"
linktitle: "DocumentPartSavingArgs"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::Saving::DocumentPartSavingArgs. Proporciona datos para la devolución de llamada DocumentPartSaving(). Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 4000
url: /es/cpp/aspose.words.saving/documentpartsavingargs/
---
## DocumentPartSavingArgs class


Proporciona datos para la devolución de llamada [DocumentPartSaving()](../idocumentpartsavingcallback/documentpartsaving/). Para obtener más información, visite el artículo de documentación [Guardar un documento](https://docs.aspose.com/words/cpp/save-a-document/).

```cpp
class DocumentPartSavingArgs : public System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_Document](./get_document/)() const | Obtiene el objeto de documento que se está guardando. |
| [get_DocumentPartFileName](./get_documentpartfilename/)() const | Obtiene o establece el nombre de archivo (sin ruta) donde se guardará la parte del documento. |
| [get_DocumentPartStream](./get_documentpartstream/)() const | Permite especificar el flujo donde se guardará la parte del documento. |
| [get_KeepDocumentPartStreamOpen](./get_keepdocumentpartstreamopen/)() const | Especifica si Aspose.Words debe mantener el flujo abierto o cerrarlo después de guardar una parte del documento. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_DocumentPartFileName](./set_documentpartfilename/)(const System::String\&) | Método setter para [Aspose::Words::Saving::DocumentPartSavingArgs::get_DocumentPartFileName](./get_documentpartfilename/). |
| [set_DocumentPartStream](./set_documentpartstream/)(const System::SharedPtr\<System::IO::Stream\>\&) | Método setter para [Aspose::Words::Saving::DocumentPartSavingArgs::get_DocumentPartStream](./get_documentpartstream/). |
| [set_DocumentPartStream](./set_documentpartstream/)(std::basic_ostream\<CharType, Traits\>\&) |  |
| [set_KeepDocumentPartStreamOpen](./set_keepdocumentpartstreamopen/)(bool) | Método setter para [Aspose::Words::Saving::DocumentPartSavingArgs::get_KeepDocumentPartStreamOpen](./get_keepdocumentpartstreamopen/). |
| static [Type](./type/)() |  |
## Observaciones


Cuando Aspose.Words guarda un documento en HTML u formatos relacionados y se especifica [DocumentSplitCriteria](../htmlsaveoptions/get_documentsplitcriteria/), el documento se divide en partes y, por defecto, cada parte del documento se guarda en un archivo separado.

La clase [DocumentPartSavingArgs](./) le permite controlar cómo se guardará cada parte del documento. Permite redefinir cómo se generan los nombres de archivo o evitar completamente el guardado de partes del documento en archivos proporcionando sus propios objetos de flujo.

Para guardar partes del documento en flujos en lugar de archivos, use la propiedad [DocumentPartStream](./get_documentpartstream/).
## Ver también

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
