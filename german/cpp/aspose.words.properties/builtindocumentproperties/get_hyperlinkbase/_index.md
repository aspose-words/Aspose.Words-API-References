---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::get_HyperlinkBase Methode"
linktitle: "get_HyperlinkBase"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Properties::BuiltInDocumentProperties::get_HyperlinkBase Methode. Gibt die Basiszeichenfolge an, die zur Auswertung relativer Hyperlinks in diesem Dokument in C++ verwendet wird."
type: docs
weight: 13000
url: /de/cpp/aspose.words.properties/builtindocumentproperties/get_hyperlinkbase/
---
## BuiltInDocumentProperties::get_HyperlinkBase method


Gibt die Basiszeichenfolge an, die für die Bewertung relativer Hyperlinks in diesem Dokument verwendet wird.

```cpp
System::String Aspose::Words::Properties::BuiltInDocumentProperties::get_HyperlinkBase()
```

## Hinweise


Aspose.Words verwendet diese Eigenschaft nicht.

## Beispiele



Zeigt, wie man den Basisanteil eines Hyperlinks in den Dokumenteneigenschaften speichert.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Fügen Sie einen relativen Hyperlink zu einem Dokument im lokalen Dateisystem mit dem Namen "Document.docx" ein.
// Ein Klick auf den Link in Microsoft Word öffnet das bezeichnete Dokument, falls es verfügbar ist.
builder->InsertHyperlink(u"Relative hyperlink", u"Document.docx", false);

// Dieser Link ist relativ. Wenn es keine "Document.docx" im selben Ordner gibt
// wie das Dokument, das diesen Link enthält, wird der Link defekt sein.
ASSERT_FALSE(System::IO::File::Exists(get_ArtifactsDir() + u"Document.docx"));
doc->Save(get_ArtifactsDir() + u"DocumentProperties.HyperlinkBase.BrokenLink.docx");

// Das Dokument, zu dem wir verlinken möchten, befindet sich in einem anderen Verzeichnis als dem, in dem wir das Dokument speichern wollen.
// Wir könnten solche Links beheben, indem wir in jedem einen absoluten Dateinamen einfügen.
// Alternativ könnten wir einen Basislink bereitstellen, den jeder Hyperlink mit einem relativen Dateinamen
// vor seinem Link anhängt, wenn wir darauf klicken.
System::SharedPtr<Aspose::Words::Properties::BuiltInDocumentProperties> properties = doc->get_BuiltInDocumentProperties();
properties->set_HyperlinkBase(get_MyDir());

ASSERT_TRUE(System::IO::File::Exists(properties->get_HyperlinkBase() + (System::ExplicitCast<Aspose::Words::Fields::FieldHyperlink>(doc->get_Range()->get_Fields()->idx_get(0)))->get_Address()));

doc->Save(get_ArtifactsDir() + u"DocumentProperties.HyperlinkBase.WorkingLink.docx");
```

## Siehe auch

* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
