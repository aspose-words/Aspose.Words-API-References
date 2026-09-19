---
title: "Aspose::Words::Properties::DocumentProperty::ToByteArray metodo"
linktitle: "ToByteArray"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Properties::DocumentProperty::ToByteArray metodo. Restituisce il valore della proprietà come array di byte in C++."
type: docs
weight: 11000
url: /it/cpp/aspose.words.properties/documentproperty/tobytearray/
---
## DocumentProperty::ToByteArray method


Restituisce il valore della proprietà come array di byte.

```cpp
System::ArrayPtr<uint8_t> Aspose::Words::Properties::DocumentProperty::ToByteArray()
```

## Note


Genera un'eccezione se il tipo della proprietà non è [ByteArray](../../propertytype/).

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

* Class [DocumentProperty](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
