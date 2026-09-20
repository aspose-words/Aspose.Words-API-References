---
title: "Aspose::Words::Saving::SaveOptions::get_UpdateLastSavedTimeProperty método"
linktitle: "get_UpdateLastSavedTimeProperty"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::SaveOptions::get_UpdateLastSavedTimeProperty método. Obtiene o establece un valor que determina si la propiedad LastSavedTime se actualiza antes de guardar en C++."
type: docs
weight: 19000
url: /es/cpp/aspose.words.saving/saveoptions/get_updatelastsavedtimeproperty/
---
## SaveOptions::get_UpdateLastSavedTimeProperty method


Obtiene o establece un valor que determina si la propiedad [LastSavedTime](../../../aspose.words.properties/builtindocumentproperties/get_lastsavedtime/) se actualiza antes de guardar.

```cpp
bool Aspose::Words::Saving::SaveOptions::get_UpdateLastSavedTimeProperty() const
```


## Ejemplos



Muestra cómo determinar si se debe conservar la propiedad "Last saved time" del documento al guardar.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

ASSERT_EQ(System::DateTime(2021, 5, 11, 6, 32, 0), doc->get_BuiltInDocumentProperties()->get_LastSavedTime());

// Cuando guardamos el documento en un formato OOXML, podemos crear un objeto OoxmlSaveOptions
// y luego pasarlo al método de guardado del documento para modificar cómo guardamos el documento.
// Establezca la propiedad "UpdateLastSavedTimeProperty" a "true" para
// establecer la propiedad incorporada "Last saved time" del documento de salida a la fecha/hora actual.
// Establezca la propiedad "UpdateLastSavedTimeProperty" a "false" para
// conservar el valor original de la propiedad incorporada "Last saved time" del documento de entrada.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
saveOptions->set_UpdateLastSavedTimeProperty(updateLastSavedTimeProperty);

doc->Save(get_ArtifactsDir() + u"OoxmlSaveOptions.LastSavedTime.docx", saveOptions);

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OoxmlSaveOptions.LastSavedTime.docx");
System::DateTime lastSavedTimeNew = doc->get_BuiltInDocumentProperties()->get_LastSavedTime();

if (updateLastSavedTimeProperty)
{
    ASSERT_TRUE((System::DateTime::get_Now() - lastSavedTimeNew).get_Days() < 1);
}
else
{
    ASSERT_EQ(System::DateTime(2021, 5, 11, 6, 32, 0), lastSavedTimeNew);
}
```

## Ver también

* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
