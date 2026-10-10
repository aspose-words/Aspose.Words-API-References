---
title: "Aspose::Words::Fields::FieldInclude::get_BookmarkName Methode"
linktitle: "get_BookmarkName"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::FieldInclude::get_BookmarkName Methode. Ruft den Namen des Lesezeichens im Dokument ab oder legt ihn fest, das in C++ einzufügen ist."
type: docs
weight: 2000
url: /de/cpp/aspose.words.fields/fieldinclude/get_bookmarkname/
---
## FieldInclude::get_BookmarkName method


Liest oder setzt den Namen des Lesezeichens im Dokument, das eingefügt werden soll.

```cpp
System::String Aspose::Words::Fields::FieldInclude::get_BookmarkName() override
```


## Beispiele



Zeigt, wie man ein INCLUDE-Feld erstellt und dessen Eigenschaften setzt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Wir können ein INCLUDE-Feld verwenden, um einen Teil eines anderen Dokuments im lokalen Dateisystem zu importieren.
// Das Lesezeichen aus dem anderen Dokument, auf das wir mit diesem Feld verweisen, enthält diesen importierten Abschnitt.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldInclude>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldInclude, true));
field->set_SourceFullName(get_MyDir() + u"Bookmarks.docx");
field->set_BookmarkName(u"MyBookmark1");
field->set_LockFields(false);
field->set_TextConverter(u"Microsoft Word");

ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(field->GetFieldCode(), u" INCLUDE .* MyBookmark1 \\\\c \"Microsoft Word\"")->get_Success());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.INCLUDE.docx");
```

## Siehe auch

* Class [FieldInclude](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
