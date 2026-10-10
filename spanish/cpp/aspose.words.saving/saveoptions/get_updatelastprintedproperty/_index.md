---
title: "Aspose::Words::Saving::SaveOptions::get_UpdateLastPrintedProperty método"
linktitle: "get_UpdateLastPrintedProperty"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::SaveOptions::get_UpdateLastPrintedProperty método. Obtiene o establece un valor que determina si la propiedad LastPrinted se actualiza antes de guardar en C++."
type: docs
weight: 18000
url: /es/cpp/aspose.words.saving/saveoptions/get_updatelastprintedproperty/
---
## SaveOptions::get_UpdateLastPrintedProperty method


Obtiene o establece un valor que determina si la propiedad [LastPrinted](../../../aspose.words.properties/builtindocumentproperties/get_lastprinted/) se actualiza antes de guardar.

```cpp
bool Aspose::Words::Saving::SaveOptions::get_UpdateLastPrintedProperty() const
```


## Ejemplos



Muestra cómo actualizar la propiedad "Last printed" de un documento al guardar.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::DateTime lastPrinted(2019, 12, 20);
doc->get_BuiltInDocumentProperties()->set_LastPrinted(lastPrinted);

// Esta bandera determina si la fecha de última impresión, que es una propiedad incorporada, se actualiza.
// Si es así, entonces la fecha de la operación de guardado más reciente del documento
// con este objeto SaveOptions pasado como parámetro se utiliza como la fecha de impresión.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::DocSaveOptions>();
saveOptions->set_UpdateLastPrintedProperty(isUpdateLastPrintedProperty);

// En Microsoft Word 2003, esta propiedad se puede encontrar a través de Archivo -> Propiedades -> Estadísticas -> Impreso.
// También puede mostrarse en el cuerpo del documento mediante un campo PRINTDATE.
doc->Save(get_ArtifactsDir() + u"DocSaveOptions.UpdateLastPrintedProperty.doc", saveOptions);

// Abra el documento guardado y luego verifique el valor de la propiedad.
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"DocSaveOptions.UpdateLastPrintedProperty.doc");

if (isUpdateLastPrintedProperty)
{
    ASSERT_NE(lastPrinted, doc->get_BuiltInDocumentProperties()->get_LastPrinted());
}
else
{
    ASSERT_EQ(lastPrinted, doc->get_BuiltInDocumentProperties()->get_LastPrinted());
}
```

## Ver también

* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
