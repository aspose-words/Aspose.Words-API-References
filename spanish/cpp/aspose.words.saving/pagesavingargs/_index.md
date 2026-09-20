---
title: "Clase Aspose::Words::Saving::PageSavingArgs"
linktitle: "PageSavingArgs"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::Saving::PageSavingArgs. Proporciona datos para el evento PageSaving(). Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 19000
url: /es/cpp/aspose.words.saving/pagesavingargs/
---
## PageSavingArgs class


Proporciona datos para el evento [PageSaving()](../ipagesavingcallback/pagesaving/). Para obtener más información, visite el artículo de documentación [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/).

```cpp
class PageSavingArgs : public System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_KeepPageStreamOpen](./get_keeppagestreamopen/)() const | Especifica si Aspose.Words debe mantener el flujo abierto o cerrarlo después de guardar una página del documento. |
| [get_PageFileName](./get_pagefilename/)() const | Obtiene el nombre de archivo donde se guardará la página del documento. |
| [get_PageIndex](./get_pageindex/)() const | Índice de página actual. |
| [get_PageStream](./get_pagestream/)() const | Permite especificar el flujo donde se guardará la página del documento. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [PageSavingArgs](./pagesavingargs/)() |  |
| [set_KeepPageStreamOpen](./set_keeppagestreamopen/)(bool) | Setter para [Aspose::Words::Saving::PageSavingArgs::get_KeepPageStreamOpen](./get_keeppagestreamopen/). |
| [set_PageFileName](./set_pagefilename/)(const System::String\&) | Establece el nombre de archivo donde se guardará la página del documento. |
| [set_PageStream](./set_pagestream/)(const System::SharedPtr\<System::IO::Stream\>\&) | Setter para [Aspose::Words::Saving::PageSavingArgs::get_PageStream](./get_pagestream/). |
| [set_PageStream](./set_pagestream/)(std::basic_ostream\<CharType, Traits\>\&) |  |
| static [Type](./type/)() |  |
## Ver también

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
