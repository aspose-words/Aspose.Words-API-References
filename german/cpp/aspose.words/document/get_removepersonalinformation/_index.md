---
title: "Aspose::Words::Document::get_RemovePersonalInformation-Methode"
linktitle: "get_RemovePersonalInformation"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Document::get_RemovePersonalInformation-Methode. Ruft ein Flag ab oder legt es fest, das anzeigt, dass Microsoft Word beim Speichern des Dokuments in C++ alle Benutzerinformationen aus Kommentaren, Änderungen und Dokumenteigenschaften entfernt."
type: docs
weight: 45000
url: /de/cpp/aspose.words/document/get_removepersonalinformation/
---
## Document::get_RemovePersonalInformation method


Liest oder legt ein Flag fest, das angibt, dass Microsoft Word beim Speichern des Dokuments alle Benutzerinformationen aus Kommentaren, Änderungen und Dokumenteigenschaften entfernt.

```cpp
bool Aspose::Words::Document::get_RemovePersonalInformation()
```


## Beispiele



Zeigt, wie das Entfernen persönlicher Informationen bei einem manuellen Speichern aktiviert wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Fügen Sie einige Inhalte mit persönlichen Informationen ein.
doc->get_BuiltInDocumentProperties()->set_Author(u"John Doe");
doc->get_BuiltInDocumentProperties()->set_Company(u"Placeholder Inc.");

doc->StartTrackRevisions(doc->get_BuiltInDocumentProperties()->get_Author(), System::DateTime::get_Now());
builder->Write(u"Hello world!");
doc->StopTrackRevisions();

// Dieses Flag entspricht Datei -> Optionen -> Trust Center -> Trust Center-Einstellungen... ->
// Datenschutzoptionen -> "Persönliche Informationen aus Dateieigenschaften beim Speichern entfernen" in Microsoft Word.
doc->set_RemovePersonalInformation(saveWithoutPersonalInfo);

// Diese Option wird bei einem Speichervorgang, der mit Aspose.Words durchgeführt wird, nicht wirksam.
// Persönliche Daten werden aus unserem Dokument entfernt, wenn das Flag gesetzt ist und wir es manuell mit Microsoft Word speichern.
doc->Save(get_ArtifactsDir() + u"Document.RemovePersonalInformation.docx");
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Document.RemovePersonalInformation.docx");

ASPOSE_ASSERT_EQ(saveWithoutPersonalInfo, doc->get_RemovePersonalInformation());
ASSERT_EQ(u"John Doe", doc->get_BuiltInDocumentProperties()->get_Author());
ASSERT_EQ(u"Placeholder Inc.", doc->get_BuiltInDocumentProperties()->get_Company());
ASSERT_EQ(u"John Doe", doc->get_Revisions()->idx_get(0)->get_Author());
```

## Siehe auch

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
