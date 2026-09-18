---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::get_Thumbnail Methode"
linktitle: "get_Thumbnail"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Properties::BuiltInDocumentProperties::get_Thumbnail Methode. Gibt das Thumbnail des Dokuments zurück oder setzt es in C++."
type: docs
weight: 28000
url: /de/cpp/aspose.words.properties/builtindocumentproperties/get_thumbnail/
---
## BuiltInDocumentProperties::get_Thumbnail method


Liest oder setzt das Vorschaubild des Dokuments.

```cpp
System::ArrayPtr<uint8_t> Aspose::Words::Properties::BuiltInDocumentProperties::get_Thumbnail()
```

## Hinweise


Derzeit wird diese Eigenschaft nur verwendet, wenn ein Dokument nach ePub exportiert wird; sie wird nicht aus anderen Dokumentformaten gelesen oder in diese geschrieben.

Ein Bild beliebigen Formats kann dieser Eigenschaft zugewiesen werden, aber das Format wird beim Export geprüft.

Nur GIF-, JPEG- und PNG-Bilder können für die ePub‑Veröffentlichung verwendet werden.

## Beispiele



Zeigt, wie man einem Dokument, das wir als Epub speichern, ein Thumbnail hinzufügt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

// Wenn wir ein Dokument, dessen \"Thumbnail\"‑Eigenschaft Bilddaten enthält, die wir hinzugefügt haben, als Epub speichern,
// kann ein Reader, der dieses Dokument öffnet, das Bild vor der ersten Seite anzeigen.
System::SharedPtr<Aspose::Words::Properties::BuiltInDocumentProperties> properties = doc->get_BuiltInDocumentProperties();

System::ArrayPtr<uint8_t> thumbnailBytes = System::IO::File::ReadAllBytes(get_ImageDir() + u"Logo.jpg");
properties->set_Thumbnail(thumbnailBytes);

doc->Save(get_ArtifactsDir() + u"DocumentProperties.Thumbnail.epub");

// Wir können das Thumbnail‑Bild eines Dokuments extrahieren und im lokalen Dateisystem speichern.
System::SharedPtr<Aspose::Words::Properties::DocumentProperty> thumbnail = doc->get_BuiltInDocumentProperties()->idx_get(u"Thumbnail");
System::IO::File::WriteAllBytes(get_ArtifactsDir() + u"DocumentProperties.Thumbnail.gif", thumbnail->ToByteArray());
```

## Siehe auch

* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
