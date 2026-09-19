---
title: "Aspose::Words::Saving::SaveOptions::get_TempFolder metodo"
linktitle: "get_TempFolder"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::SaveOptions::get_TempFolder metodo. Specifica la cartella per i file temporanei usati durante il salvataggio in un file DOC o DOCX. Per impostazione predefinita, questa proprietà è null e non vengono utilizzati file temporanei in C++."
type: docs
weight: 15000
url: /it/cpp/aspose.words.saving/saveoptions/get_tempfolder/
---
## SaveOptions::get_TempFolder method


Specifica la cartella per i file temporanei utilizzati durante il salvataggio in un file DOC o DOCX. Per impostazione predefinita, questa proprietà è **null** e non vengono utilizzati file temporanei.

```cpp
System::String Aspose::Words::Saving::SaveOptions::get_TempFolder() const
```

## Note


Quando Aspose.Words salva un documento, deve creare strutture interne temporanee. Per impostazione predefinita, queste strutture interne vengono create in memoria e l'utilizzo della memoria aumenta per un breve periodo mentre il documento viene salvato. Quando il salvataggio è completato, la memoria viene liberata e recuperata dal garbage collector.

Specificare una cartella temporanea usando [TempFolder](./) farà sì che Aspose.Words mantenga le strutture interne in file temporanei anziché in memoria. Riduce l'utilizzo della memoria durante il salvataggio, ma diminuirà le prestazioni di salvataggio.

La cartella deve esistere ed essere scrivibile, altrimenti verrà generata un'eccezione.

Aspose.Words elimina automaticamente tutti i file temporanei al termine del salvataggio.

## Esempi



Mostra come utilizzare il disco rigido anziché la memoria durante il salvataggio di un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// Quando salviamo un documento, vari elementi vengono temporaneamente memorizzati in memoria mentre l'operazione di salvataggio è in corso.
// Possiamo utilizzare questa opzione per usare una cartella temporanea nel file system locale invece,
// il che ridurrà il consumo di memoria della nostra applicazione.
auto options = System::MakeObject<Aspose::Words::Saving::DocSaveOptions>();
options->set_TempFolder(get_ArtifactsDir() + u"TempFiles");

// La cartella temporanea specificata deve esistere nel file system locale prima dell'operazione di salvataggio.
System::IO::Directory::CreateDirectory_(options->get_TempFolder());

doc->Save(get_ArtifactsDir() + u"DocSaveOptions.TempFolder.doc", options);

// La cartella persisterà senza contenuti residui dall'operazione di caricamento.
ASSERT_EQ(0, System::IO::Directory::GetFiles(options->get_TempFolder())->get_Length());
```

## Vedi anche

* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
