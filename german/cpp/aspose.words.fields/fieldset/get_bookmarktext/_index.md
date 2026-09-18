---
title: "Aspose::Words::Fields::FieldSet::get_BookmarkText Methode"
linktitle: "get_BookmarkText"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::FieldSet::get_BookmarkText Methode. Liest oder setzt den neuen Text des Lesezeichens in C++."
type: docs
weight: 3000
url: /de/cpp/aspose.words.fields/fieldset/get_bookmarktext/
---
## FieldSet::get_BookmarkText method


Liest oder setzt den neuen Text des Lesezeichens.

```cpp
System::String Aspose::Words::Fields::FieldSet::get_BookmarkText()
```


## Beispiele



Zeigt, wie man mit einem SET-Feld markierten Text erstellt und diesen dann im Dokument mit einem REF-Feld anzeigt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Benennen Sie markierten Text mit einem SET-Feld.
// Dieses Feld bezieht sich auf das "bookmark", nicht auf eine Lesezeichenstruktur, die im Text erscheint, sondern auf eine benannte Variable.
auto fieldSet = System::ExplicitCast<Aspose::Words::Fields::FieldSet>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSet, false));
fieldSet->set_BookmarkName(u"MyBookmark");
fieldSet->set_BookmarkText(u"Hello world!");
fieldSet->Update();

ASSERT_EQ(u" SET  MyBookmark \"Hello world!\"", fieldSet->GetFieldCode());

// Verweisen Sie im REF-Feld per Namen auf das Lesezeichen und zeigen Sie dessen Inhalt an.
auto fieldRef = System::ExplicitCast<Aspose::Words::Fields::FieldRef>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldRef, true));
fieldRef->set_BookmarkName(u"MyBookmark");
fieldRef->Update();

ASSERT_EQ(u" REF  MyBookmark", fieldRef->GetFieldCode());
ASSERT_EQ(u"Hello world!", fieldRef->get_Result());

doc->Save(get_ArtifactsDir() + u"Field.SET.REF.docx");
```

## Siehe auch

* Class [FieldSet](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
