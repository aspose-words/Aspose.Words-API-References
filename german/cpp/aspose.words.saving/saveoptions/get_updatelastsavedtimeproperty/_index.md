---
title: "Aspose::Words::Saving::SaveOptions::get_UpdateLastSavedTimeProperty Methode"
linktitle: "get_UpdateLastSavedTimeProperty"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::SaveOptions::get_UpdateLastSavedTimeProperty Methode. Gibt einen Wert zurück oder legt ihn fest, der bestimmt, ob die LastSavedTime‑Eigenschaft vor dem Speichern in C++ aktualisiert wird."
type: docs
weight: 19000
url: /de/cpp/aspose.words.saving/saveoptions/get_updatelastsavedtimeproperty/
---
## SaveOptions::get_UpdateLastSavedTimeProperty method


Gibt einen Wert zurück oder legt ihn fest, der bestimmt, ob die [LastSavedTime](../../../aspose.words.properties/builtindocumentproperties/get_lastsavedtime/)‑Eigenschaft vor dem Speichern aktualisiert wird.

```cpp
bool Aspose::Words::Saving::SaveOptions::get_UpdateLastSavedTimeProperty() const
```


## Beispiele



Zeigt, wie man bestimmt, ob die Dokument‑Eigenschaft \"Last saved time\" beim Speichern erhalten bleiben soll.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

ASSERT_EQ(System::DateTime(2021, 5, 11, 6, 32, 0), doc->get_BuiltInDocumentProperties()->get_LastSavedTime());

// Wenn wir das Dokument in ein OOXML-Format speichern, können wir ein OoxmlSaveOptions-Objekt erstellen
// und es dann an die Speichermethode des Dokuments übergeben, um zu ändern, wie wir das Dokument speichern.
// Setzen Sie die Eigenschaft \"UpdateLastSavedTimeProperty\" auf \"true\", um
// die integrierte Eigenschaft \"Last saved time\" des Ausgabedokuments auf das aktuelle Datum/Uhrzeit zu setzen.
// Setzen Sie die Eigenschaft \"UpdateLastSavedTimeProperty\" auf \"false\", um
// den ursprünglichen Wert der integrierten Eigenschaft \"Last saved time\" des Eingabedokuments beizubehalten.
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

## Siehe auch

* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
