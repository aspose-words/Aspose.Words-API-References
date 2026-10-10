---
title: "Método Aspose::Words::Saving::SaveOptions::get_UpdateCreatedTimeProperty"
linktitle: "get_UpdateCreatedTimeProperty"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Saving::SaveOptions::get_UpdateCreatedTimeProperty. Obtiene o establece un valor que determina si la propiedad CreatedTime se actualiza antes de guardar. El valor predeterminado es false; en C++."
type: docs
weight: 16000
url: /es/cpp/aspose.words.saving/saveoptions/get_updatecreatedtimeproperty/
---
## SaveOptions::get_UpdateCreatedTimeProperty method


Obtiene o establece un valor que determina si la propiedad [CreatedTime](../../../aspose.words.properties/builtindocumentproperties/get_createdtime/) se actualiza antes de guardar. El valor predeterminado es **false**;

```cpp
bool Aspose::Words::Saving::SaveOptions::get_UpdateCreatedTimeProperty() const
```


## Ejemplos



Muestra cómo actualizar la propiedad "CreatedTime" de un documento al guardar.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::DateTime createdTime(2019, 12, 20);
doc->get_BuiltInDocumentProperties()->set_CreatedTime(createdTime);

// Esta bandera determina si la hora de creación, que es una propiedad incorporada, se actualiza.
// Si es así, entonces la fecha de la operación de guardado más reciente del documento
// con este objeto SaveOptions pasado como parámetro se usa como la hora de creación.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::DocSaveOptions>();
saveOptions->set_UpdateCreatedTimeProperty(isUpdateCreatedTimeProperty);

doc->Save(get_ArtifactsDir() + u"DocSaveOptions.UpdateCreatedTimeProperty.docx", saveOptions);

// Abra el documento guardado y luego verifique el valor de la propiedad.
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"DocSaveOptions.UpdateCreatedTimeProperty.docx");

if (isUpdateCreatedTimeProperty)
{
    ASSERT_NE(createdTime, doc->get_BuiltInDocumentProperties()->get_CreatedTime());
}
else
{
    ASSERT_EQ(createdTime, doc->get_BuiltInDocumentProperties()->get_CreatedTime());
}
```

## Ver también

* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
