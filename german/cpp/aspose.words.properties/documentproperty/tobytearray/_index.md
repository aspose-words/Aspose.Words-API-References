---
title: "Aspose::Words::Properties::DocumentProperty::ToByteArray Methode"
linktitle: "ToByteArray"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Properties::DocumentProperty::ToByteArray-Methode. Gibt den Eigenschaftswert als Byte-Array in C++ zurück."
type: docs
weight: 11000
url: /de/cpp/aspose.words.properties/documentproperty/tobytearray/
---
## DocumentProperty::ToByteArray method


Gibt den Eigenschaftswert als Byte‑Array zurück.

```cpp
System::ArrayPtr<uint8_t> Aspose::Words::Properties::DocumentProperty::ToByteArray()
```

## Hinweise


Wirft eine Ausnahme, wenn der Eigenschaftstyp nicht [ByteArray](../../propertytype/) ist.

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

* Class [DocumentProperty](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
