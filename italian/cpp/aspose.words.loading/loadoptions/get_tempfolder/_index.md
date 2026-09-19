---
title: "Aspose::Words::Loading::LoadOptions::get_TempFolder metodo"
linktitle: "get_TempFolder"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Loading::LoadOptions::get_TempFolder metodo. Consente di utilizzare file temporanei durante la lettura del documento. Per impostazione predefinita questa proprietà è null e non vengono utilizzati file temporanei in C++."
type: docs
weight: 16000
url: /it/cpp/aspose.words.loading/loadoptions/get_tempfolder/
---
## LoadOptions::get_TempFolder method


Consente di utilizzare file temporanei durante la lettura del documento. Per impostazione predefinita questa proprietà è **null** e non vengono utilizzati file temporanei.

```cpp
System::String Aspose::Words::Loading::LoadOptions::get_TempFolder() const
```

## Note


La cartella deve esistere ed essere scrivibile, altrimenti verrà generata un'eccezione.

Aspose.Words elimina automaticamente tutti i file temporanei al termine della lettura.

## Esempi



Mostra come caricare un documento utilizzando file temporanei.
```cpp
// Nota che tale approccio può ridurre l'uso della memoria ma degrada le prestazioni
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->set_TempFolder(u"C:\\TempFolder\\");

// Assicurati che la directory esista e carica
System::IO::Directory::CreateDirectory_(loadOptions->get_TempFolder());

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx", loadOptions);
```


Mostra come utilizzare il disco rigido invece della memoria durante il caricamento di un documento.
```cpp
// Quando carichiamo un documento, vari elementi vengono temporaneamente memorizzati in memoria mentre avviene l'operazione di salvataggio.
// Possiamo utilizzare questa opzione per usare una cartella temporanea nel file system locale invece,
// il che ridurrà il consumo di memoria della nostra applicazione.
auto options = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
options->set_TempFolder(get_ArtifactsDir() + u"TempFiles");

// La cartella temporanea specificata deve esistere nel file system locale prima dell'operazione di caricamento.
System::IO::Directory::CreateDirectory_(options->get_TempFolder());

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx", options);

// La cartella persisterà senza contenuti residui dall'operazione di caricamento.
ASSERT_EQ(0, System::IO::Directory::GetFiles(options->get_TempFolder())->get_Length());
```

## Vedi anche

* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
