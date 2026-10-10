---
title: "Aspose::Words::Saving::CssSavingArgs class"
linktitle: "CssSavingArgs"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::CssSavingArgs class. Proporciona datos para el evento CssSaving(). Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words.saving/csssavingargs/
---
## CssSavingArgs class


Proporciona datos para el evento [CssSaving()](../icsssavingcallback/csssaving/). Para obtener más información, visite el artículo de documentación [Save a Document](https://docs.aspose.com/words/cpp/save-a-document/).

```cpp
class CssSavingArgs : public System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_CssStream](./get_cssstream/)() const | Permite especificar el flujo donde se guardará la información CSS. |
| [get_Document](./get_document/)() const | Obtiene el objeto documento que se está guardando actualmente. |
| [get_IsExportNeeded](./get_isexportneeded/)() const | Permite especificar si el CSS se exportará a un archivo y se incrustará en el documento HTML. El valor predeterminado es **true**. Cuando esta propiedad es **false**, la información CSS no se guardará en un archivo CSS y no se incrustará en el documento HTML. |
| [get_KeepCssStreamOpen](./get_keepcssstreamopen/)() const | Especifica si Aspose.Words debe mantener el flujo abierto o cerrarlo después de guardar la información CSS. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_CssStream](./set_cssstream/)(const System::SharedPtr\<System::IO::Stream\>\&) | Método set para [Aspose::Words::Saving::CssSavingArgs::get_CssStream](./get_cssstream/). |
| [set_CssStream](./set_cssstream/)(std::basic_ostream\<CharType, Traits\>\&) |  |
| [set_IsExportNeeded](./set_isexportneeded/)(bool) | Permite especificar si el CSS se exportará a un archivo y se incrustará en el documento HTML. El valor predeterminado es **true**. Cuando esta propiedad es **false**, la información CSS no se guardará en un archivo CSS y no se incrustará en el documento HTML. |
| [set_KeepCssStreamOpen](./set_keepcssstreamopen/)(bool) | Método set para [Aspose::Words::Saving::CssSavingArgs::get_KeepCssStreamOpen](./get_keepcssstreamopen/). |
| static [Type](./type/)() |  |
## Observaciones


De forma predeterminada, cuando Aspose.Words guarda un documento en HTML, guarda la información CSS en línea (como valor del atributo **style** en cada elemento).

[CssSavingArgs](./) allows to save CSS information into file by providing your own stream object.

Para guardar CSS en el flujo, use la propiedad [CssStream](./get_cssstream/).

Para suprimir el guardado de CSS en un archivo y la incrustación en el documento HTML, use la propiedad [IsExportNeeded](./get_isexportneeded/).
## Ver también

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
