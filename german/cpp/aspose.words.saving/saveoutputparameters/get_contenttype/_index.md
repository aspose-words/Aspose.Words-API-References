---
title: "Aspose::Words::Saving::SaveOutputParameters::get_ContentType Methode"
linktitle: "get_ContentType"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::SaveOutputParameters::get_ContentType Methode. Gibt die Content-Type-Zeichenkette (Internet Media Type) zurück, die den Typ des gespeicherten Dokuments in C++ identifiziert."
type: docs
weight: 2000
url: /de/cpp/aspose.words.saving/saveoutputparameters/get_contenttype/
---
## SaveOutputParameters::get_ContentType method


Gibt die Content-Type-Zeichenkette (Internet Media Type) zurück, die den Typ des gespeicherten Dokuments identifiziert.

```cpp
System::String Aspose::Words::Saving::SaveOutputParameters::get_ContentType() const
```


## Beispiele



Zeigt, wie auf die Ausgabparameter eines Dokumentspeichervorgangs zugegriffen wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

// Nachdem wir ein Dokument gespeichert haben, können wir auf den Internet Media Type (MIME-Typ) des neu erstellten Ausgabedokuments zugreifen.
System::SharedPtr<Aspose::Words::Saving::SaveOutputParameters> parameters = doc->Save(get_ArtifactsDir() + u"Document.SaveOutputParameters.doc");

ASSERT_EQ(u"application/msword", parameters->get_ContentType());

// Diese Eigenschaft ändert sich je nach Speicherformat.
parameters = doc->Save(get_ArtifactsDir() + u"Document.SaveOutputParameters.pdf");

ASSERT_EQ(u"application/pdf", parameters->get_ContentType());
```

## Siehe auch

* Class [SaveOutputParameters](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
