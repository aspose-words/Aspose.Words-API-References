---
title: "Aspose::Words::Saving::FontSavingArgs class"
linktitle: "FontSavingArgs"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::FontSavingArgs class. Proporciona datos para el evento FontSaving(). Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 8000
url: /es/cpp/aspose.words.saving/fontsavingargs/
---
## FontSavingArgs class


Proporciona datos para el evento [FontSaving()](../ifontsavingcallback/fontsaving/). Para obtener más información, visite el artículo de documentación [Save a Document](https://docs.aspose.com/words/cpp/save-a-document/).

```cpp
class FontSavingArgs : public System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_Bold](./get_bold/)() const | Indica si la fuente actual está en negrita. |
| [get_Document](./get_document/)() const | Obtiene el objeto de documento que se está guardando. |
| [get_FontFamilyName](./get_fontfamilyname/)() const | Indica el nombre de la familia de la fuente actual. |
| [get_FontFileName](./get_fontfilename/)() const | Obtiene o establece el nombre de archivo (sin ruta) donde se guardará la fuente. |
| [get_FontStream](./get_fontstream/)() const | Permite especificar el flujo donde se guardará la fuente. |
| [get_IsExportNeeded](./get_isexportneeded/)() const | Permite especificar si la fuente actual se exportará como un recurso de fuente. Por defecto es **true**. |
| [get_IsSubsettingNeeded](./get_issubsettingneeded/)() const | Permite especificar si la fuente actual se subestablecerá antes de exportarse como un recurso de fuente. |
| [get_Italic](./get_italic/)() const | Indica si la fuente actual está en cursiva. |
| [get_KeepFontStreamOpen](./get_keepfontstreamopen/)() const | Especifica si Aspose.Words debe mantener el flujo abierto o cerrarlo después de guardar una fuente. |
| [get_OriginalFileName](./get_originalfilename/)() const | Obtiene el nombre original del archivo de fuente con su extensión. |
| [get_OriginalFileSize](./get_originalfilesize/)() const | Obtiene el tamaño original del archivo de fuente. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_FontFileName](./set_fontfilename/)(const System::String\&) | Método set para [Aspose::Words::Saving::FontSavingArgs::get_FontFileName](./get_fontfilename/). |
| [set_FontStream](./set_fontstream/)(const System::SharedPtr\<System::IO::Stream\>\&) | Método set para [Aspose::Words::Saving::FontSavingArgs::get_FontStream](./get_fontstream/). |
| [set_FontStream](./set_fontstream/)(std::basic_ostream\<CharType, Traits\>\&) |  |
| [set_IsExportNeeded](./set_isexportneeded/)(bool) | Permite especificar si la fuente actual se exportará como un recurso de fuente. Por defecto es **true**. |
| [set_IsSubsettingNeeded](./set_issubsettingneeded/)(bool) | Método set para [Aspose::Words::Saving::FontSavingArgs::get_IsSubsettingNeeded](./get_issubsettingneeded/). |
| [set_KeepFontStreamOpen](./set_keepfontstreamopen/)(bool) | Método set para [Aspose::Words::Saving::FontSavingArgs::get_KeepFontStreamOpen](./get_keepfontstreamopen/). |
| static [Type](./type/)() |  |
## Observaciones


Cuando Aspose.Words guarda un documento en HTML o formatos relacionados y [ExportFontResources](../htmlsaveoptions/get_exportfontresources/) está configurado en **true**, guarda cada fuente sujeta a exportación en un archivo separado.

[FontSavingArgs](./) controls whether particular font resource should be exported and how.

[FontSavingArgs](./) also allows to redefine how font file names are generated or to completely circumvent saving of fonts into files by providing your own stream objects.

Para decidir si guardar un recurso de fuente en particular, use la propiedad [IsExportNeeded](./get_isexportneeded/).

Para guardar fuentes en flujos en lugar de archivos, use la propiedad [FontStream](./get_fontstream/).
## Ver también

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
