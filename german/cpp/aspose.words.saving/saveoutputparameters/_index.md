---
title: "Aspose::Words::Saving::SaveOutputParameters class"
linktitle: "SaveOutputParameters"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::SaveOutputParameters class. Dieses Objekt wird an den Aufrufer zurückgegeben, nachdem ein Dokument gespeichert wurde, und enthält zusätzliche Informationen, die während des Speichervorgangs erzeugt oder berechnet wurden. Der Aufrufer kann dieses Objekt verwenden oder ignorieren. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 30000
url: /de/cpp/aspose.words.saving/saveoutputparameters/
---
## SaveOutputParameters class


Dieses Objekt wird nach dem Speichern eines Dokuments an den Aufrufer zurückgegeben und enthält zusätzliche Informationen, die während des Speicher‑Vorgangs erzeugt oder berechnet wurden. Der Aufrufer kann dieses Objekt verwenden oder ignorieren. Weitere Informationen finden Sie im Dokumentationsartikel [Save a Document](https://docs.aspose.com/words/cpp/save-a-document/).

```cpp
class SaveOutputParameters : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_ContentType](./get_contenttype/)() const | Gibt die Content-Type-Zeichenkette (Internet Media Type) zurück, die den Typ des gespeicherten Dokuments identifiziert. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
