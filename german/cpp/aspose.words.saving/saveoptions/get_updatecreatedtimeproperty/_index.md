---
title: "Aspose::Words::Saving::SaveOptions::get_UpdateCreatedTimeProperty-Methode"
linktitle: "get_UpdateCreatedTimeProperty"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::SaveOptions::get_UpdateCreatedTimeProperty-Methode. Gibt einen Wert zurück oder legt ihn fest, der bestimmt, ob die CreatedTime-Eigenschaft vor dem Speichern aktualisiert wird. Der Standardwert ist false; in C++."
type: docs
weight: 16000
url: /de/cpp/aspose.words.saving/saveoptions/get_updatecreatedtimeproperty/
---
## SaveOptions::get_UpdateCreatedTimeProperty method


Gibt einen Wert zurück oder legt ihn fest, der bestimmt, ob die [CreatedTime](../../../aspose.words.properties/builtindocumentproperties/get_createdtime/) Eigenschaft vor dem Speichern aktualisiert wird. Der Standardwert ist **false**;.

```cpp
bool Aspose::Words::Saving::SaveOptions::get_UpdateCreatedTimeProperty() const
```


## Beispiele



Zeigt, wie die "CreatedTime"-Eigenschaft eines Dokuments beim Speichern aktualisiert wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::DateTime createdTime(2019, 12, 20);
doc->get_BuiltInDocumentProperties()->set_CreatedTime(createdTime);

// Dieses Flag bestimmt, ob die Erstellungszeit, die eine integrierte Eigenschaft ist, aktualisiert wird.
// Falls ja, wird das Datum der zuletzt gespeicherten Version des Dokuments
// wird mit diesem SaveOptions-Objekt, das als Parameter übergeben wird, als Erstellungszeit verwendet.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::DocSaveOptions>();
saveOptions->set_UpdateCreatedTimeProperty(isUpdateCreatedTimeProperty);

doc->Save(get_ArtifactsDir() + u"DocSaveOptions.UpdateCreatedTimeProperty.docx", saveOptions);

// Öffnen Sie das gespeicherte Dokument und prüfen Sie anschließend den Wert der Eigenschaft.
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

## Siehe auch

* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
