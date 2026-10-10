---
title: "Aspose::Words::Fields::FieldAuthor::get_AuthorName Methode"
linktitle: "get_AuthorName"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::FieldAuthor::get_AuthorName Methode. Ruft den Namen des Dokumentautors ab oder legt ihn in C++ fest."
type: docs
weight: 2000
url: /de/cpp/aspose.words.fields/fieldauthor/get_authorname/
---
## FieldAuthor::get_AuthorName method


Liest oder setzt den Namen des Dokumentautors.

```cpp
System::String Aspose::Words::Fields::FieldAuthor::get_AuthorName()
```


## Beispiele



Zeigt, wie man ein AUTHOR-Feld verwendet, um den Namen des Dokumentenerstellers anzuzeigen.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// AUTHOR-Felder beziehen ihre Ergebnisse aus der integrierten Dokumenteigenschaft "Author".
// Wenn wir ein Dokument in Microsoft Word erstellen und speichern,
// enthält es unseren Benutzernamen in dieser Eigenschaft.
// Wenn wir jedoch ein Dokument programmgesteuert mit Aspose.Words erstellen,
// Die "Author"-Eigenschaft ist standardmäßig ein leerer String.
ASSERT_EQ(System::String::Empty, doc->get_BuiltInDocumentProperties()->get_Author());

// Legen Sie einen Backup-Autorenamen fest, den AUTHOR-Felder verwenden sollen
// wenn die "Author"-Eigenschaft einen leeren String enthält.
doc->get_FieldOptions()->set_DefaultDocumentAuthor(u"Joe Bloggs");

builder->Write(u"This document was created by ");
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldAuthor>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAuthor, true));
field->Update();

ASSERT_EQ(u" AUTHOR ", field->GetFieldCode());
ASSERT_EQ(u"Joe Bloggs", field->get_Result());

// Aktualisieren eines AUTHOR-Feldes, das einen Wert enthält
// wird diesen Wert auf die integrierte "Author"-Eigenschaft anwenden.
ASSERT_EQ(u"Joe Bloggs", doc->get_BuiltInDocumentProperties()->get_Author());

// Wenn Sie diese Eigenschaft ändern und anschließend das AUTHOR-Feld aktualisieren, wird dieser Wert auf das Feld angewendet.
doc->get_BuiltInDocumentProperties()->set_Author(u"John Doe");
field->Update();

ASSERT_EQ(u" AUTHOR ", field->GetFieldCode());
ASSERT_EQ(u"John Doe", field->get_Result());

// Wenn wir ein AUTHOR-Feld aktualisieren, nachdem wir seine "Name"-Eigenschaft geändert haben,
// wird das Feld den neuen Namen anzeigen und den neuen Namen auf die integrierte Eigenschaft anwenden.
field->set_AuthorName(u"Jane Doe");
field->Update();

ASSERT_EQ(u" AUTHOR  \"Jane Doe\"", field->GetFieldCode());
ASSERT_EQ(u"Jane Doe", field->get_Result());

// AUTHOR-Felder beeinflussen die Eigenschaft DefaultDocumentAuthor nicht.
ASSERT_EQ(u"Jane Doe", doc->get_BuiltInDocumentProperties()->get_Author());
ASSERT_EQ(u"Joe Bloggs", doc->get_FieldOptions()->get_DefaultDocumentAuthor());

doc->Save(get_ArtifactsDir() + u"Field.AUTHOR.docx");
```

## Siehe auch

* Class [FieldAuthor](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
