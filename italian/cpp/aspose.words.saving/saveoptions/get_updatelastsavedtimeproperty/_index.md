---
title: "Metodo Aspose::Words::Saving::SaveOptions::get_UpdateLastSavedTimeProperty"
linktitle: "get_UpdateLastSavedTimeProperty"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Saving::SaveOptions::get_UpdateLastSavedTimeProperty. Ottiene o imposta un valore che determina se la proprietà LastSavedTime viene aggiornata prima del salvataggio in C++."
type: docs
weight: 19000
url: /it/cpp/aspose.words.saving/saveoptions/get_updatelastsavedtimeproperty/
---
## SaveOptions::get_UpdateLastSavedTimeProperty method


Ottiene o imposta un valore che determina se la proprietà [LastSavedTime](../../../aspose.words.properties/builtindocumentproperties/get_lastsavedtime/) viene aggiornata prima del salvataggio.

```cpp
bool Aspose::Words::Saving::SaveOptions::get_UpdateLastSavedTimeProperty() const
```


## Esempi



Mostra come determinare se conservare la proprietà "Last saved time" del documento durante il salvataggio.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

ASSERT_EQ(System::DateTime(2021, 5, 11, 6, 32, 0), doc->get_BuiltInDocumentProperties()->get_LastSavedTime());

// Quando salviamo il documento in un formato OOXML, possiamo creare un oggetto OoxmlSaveOptions
// e poi passarlo al metodo di salvataggio del documento per modificare il modo in cui salviamo il documento.
// Imposta la proprietà "UpdateLastSavedTimeProperty" su "true" per
// impostare la proprietà incorporata "Last saved time" del documento di output alla data/ora corrente.
// Imposta la proprietà "UpdateLastSavedTimeProperty" su "false" per
// preservare il valore originale della proprietà incorporata "Last saved time" del documento di input.
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

## Vedi anche

* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
