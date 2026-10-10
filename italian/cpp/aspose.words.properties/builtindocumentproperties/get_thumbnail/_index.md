---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::get_Thumbnail metodo"
linktitle: "get_Thumbnail"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Properties::BuiltInDocumentProperties::get_Thumbnail metodo. Ottiene o imposta la miniatura del documento in C++."
type: docs
weight: 28000
url: /it/cpp/aspose.words.properties/builtindocumentproperties/get_thumbnail/
---
## BuiltInDocumentProperties::get_Thumbnail method


Ottiene o imposta la miniatura del documento.

```cpp
System::ArrayPtr<uint8_t> Aspose::Words::Properties::BuiltInDocumentProperties::get_Thumbnail()
```

## Note


Per ora questa proprietà è usata solo quando un documento viene esportato in ePub; non viene letta né scritta in altri formati di documento.

Un'immagine di formato arbitrario può essere impostata su questa proprietà, ma il formato viene verificato durante l'esportazione.

Solo le immagini gif, jpeg e png possono essere utilizzate per la pubblicazione ePub.

## Esempi



Mostra come aggiungere una miniatura a un documento che salviamo come Epub.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

// Se salviamo un documento, la cui proprietà "Thumbnail" contiene i dati dell'immagine che abbiamo aggiunto, come un Epub,
// un lettore che apre quel documento potrebbe visualizzare l'immagine prima della prima pagina.
System::SharedPtr<Aspose::Words::Properties::BuiltInDocumentProperties> properties = doc->get_BuiltInDocumentProperties();

System::ArrayPtr<uint8_t> thumbnailBytes = System::IO::File::ReadAllBytes(get_ImageDir() + u"Logo.jpg");
properties->set_Thumbnail(thumbnailBytes);

doc->Save(get_ArtifactsDir() + u"DocumentProperties.Thumbnail.epub");

// Possiamo estrarre l'immagine della miniatura di un documento e salvarla nel file system locale.
System::SharedPtr<Aspose::Words::Properties::DocumentProperty> thumbnail = doc->get_BuiltInDocumentProperties()->idx_get(u"Thumbnail");
System::IO::File::WriteAllBytes(get_ArtifactsDir() + u"DocumentProperties.Thumbnail.gif", thumbnail->ToByteArray());
```

## Vedi anche

* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
