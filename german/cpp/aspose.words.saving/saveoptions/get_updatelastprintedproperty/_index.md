---
title: "Aspose::Words::Saving::SaveOptions::get_UpdateLastPrintedProperty-Methode"
linktitle: "get_UpdateLastPrintedProperty"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::SaveOptions::get_UpdateLastPrintedProperty-Methode. Liest oder setzt einen Wert, der bestimmt, ob die LastPrinted-Eigenschaft vor dem Speichern in C++ aktualisiert wird."
type: docs
weight: 18000
url: /de/cpp/aspose.words.saving/saveoptions/get_updatelastprintedproperty/
---
## SaveOptions::get_UpdateLastPrintedProperty method


Liest oder setzt einen Wert, der bestimmt, ob die [LastPrinted](../../../aspose.words.properties/builtindocumentproperties/get_lastprinted/) Eigenschaft vor dem Speichern aktualisiert wird.

```cpp
bool Aspose::Words::Saving::SaveOptions::get_UpdateLastPrintedProperty() const
```


## Beispiele



Zeigt, wie die "Zuletzt gedruckt"-Eigenschaft eines Dokuments beim Speichern aktualisiert wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::DateTime lastPrinted(2019, 12, 20);
doc->get_BuiltInDocumentProperties()->set_LastPrinted(lastPrinted);

// Dieses Flag bestimmt, ob das Datum der letzten Druckausgabe, das eine integrierte Eigenschaft ist, aktualisiert wird.
// Falls ja, wird das Datum der zuletzt gespeicherten Version des Dokuments
// mit diesem SaveOptions-Objekt, das als Parameter übergeben wird, als Druckdatum verwendet.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::DocSaveOptions>();
saveOptions->set_UpdateLastPrintedProperty(isUpdateLastPrintedProperty);

// In Microsoft Word 2003 kann diese Eigenschaft über Datei -> Eigenschaften -> Statistik -> Gedruckt gefunden werden.
// Sie kann auch im Dokumentenkörper angezeigt werden, indem ein PRINTDATE-Feld verwendet wird.
doc->Save(get_ArtifactsDir() + u"DocSaveOptions.UpdateLastPrintedProperty.doc", saveOptions);

// Öffnen Sie das gespeicherte Dokument und prüfen Sie anschließend den Wert der Eigenschaft.
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

## Siehe auch

* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
