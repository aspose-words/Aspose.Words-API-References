---
title: "Aspose::Words::Fields::Field::get_DisplayResult Methode"
linktitle: "get_DisplayResult"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::Field::get_DisplayResult Methode. Gibt den Text zurück, der das angezeigte Feldresultat in C++ darstellt."
type: docs
weight: 2000
url: /de/cpp/aspose.words.fields/field/get_displayresult/
---
## Field::get_DisplayResult method


Liefert den Text, der das angezeigte Feldresultat darstellt.

```cpp
System::String Aspose::Words::Fields::Field::get_DisplayResult()
```


## Beispiele



Zeigt, wie man den tatsächlichen Text erhält, den ein Feld im Dokument anzeigt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"This document was written by ");
auto fieldAuthor = System::ExplicitCast<Aspose::Words::Fields::FieldAuthor>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAuthor, true));
fieldAuthor->set_AuthorName(u"John Doe");

// Wir können die DisplayResult‑Eigenschaft verwenden, um den genauen Text zu überprüfen
// den ein Feld an seiner Stelle im Dokument anzeigen würde.
ASSERT_EQ(System::String::Empty, fieldAuthor->get_DisplayResult());

// Felder halten keine genauen Ergebniswerte in Echtzeit.
// Um sicherzustellen, dass unsere Felder jederzeit genaue Ergebnisse anzeigen,
// wie etwa unmittelbar vor einem Speichervorgang, müssen wir sie manuell aktualisieren.
fieldAuthor->Update();

ASSERT_EQ(u"John Doe", fieldAuthor->get_DisplayResult());

doc->Save(get_ArtifactsDir() + u"Field.DisplayResult.docx");
```

## Siehe auch

* Class [Field](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
