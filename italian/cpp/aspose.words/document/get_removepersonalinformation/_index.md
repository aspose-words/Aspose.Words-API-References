---
title: "Metodo Aspose::Words::Document::get_RemovePersonalInformation"
linktitle: "get_RemovePersonalInformation"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Document::get_RemovePersonalInformation. Ottiene o imposta un flag che indica che Microsoft Word rimuoverà tutte le informazioni dell'utente da commenti, revisioni e proprietà del documento al salvataggio del documento in C++."
type: docs
weight: 45000
url: /it/cpp/aspose.words/document/get_removepersonalinformation/
---
## Document::get_RemovePersonalInformation method


Ottiene o imposta un flag che indica che Microsoft Word rimuoverà tutte le informazioni utente da commenti, revisioni e proprietà del documento al salvataggio del documento.

```cpp
bool Aspose::Words::Document::get_RemovePersonalInformation()
```


## Esempi



Mostra come abilitare la rimozione delle informazioni personali durante un salvataggio manuale.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserisci del contenuto con informazioni personali.
doc->get_BuiltInDocumentProperties()->set_Author(u"John Doe");
doc->get_BuiltInDocumentProperties()->set_Company(u"Placeholder Inc.");

doc->StartTrackRevisions(doc->get_BuiltInDocumentProperties()->get_Author(), System::DateTime::get_Now());
builder->Write(u"Hello world!");
doc->StopTrackRevisions();

// Questo flag è equivalente a File -> Opzioni -> Centro protezione -> Impostazioni centro protezione... ->
// Opzioni privacy -> "Remove personal information from file properties on save" in Microsoft Word.
doc->set_RemovePersonalInformation(saveWithoutPersonalInfo);

// Questa opzione non avrà effetto durante un'operazione di salvataggio effettuata con Aspose.Words.
// I dati personali saranno rimossi dal nostro documento con il flag impostato quando lo salviamo manualmente usando Microsoft Word.
doc->Save(get_ArtifactsDir() + u"Document.RemovePersonalInformation.docx");
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Document.RemovePersonalInformation.docx");

ASPOSE_ASSERT_EQ(saveWithoutPersonalInfo, doc->get_RemovePersonalInformation());
ASSERT_EQ(u"John Doe", doc->get_BuiltInDocumentProperties()->get_Author());
ASSERT_EQ(u"Placeholder Inc.", doc->get_BuiltInDocumentProperties()->get_Company());
ASSERT_EQ(u"John Doe", doc->get_Revisions()->idx_get(0)->get_Author());
```

## Vedi anche

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
