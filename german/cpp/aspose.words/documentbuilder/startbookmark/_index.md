---
title: "Aspose::Words::DocumentBuilder::StartBookmark Methode"
linktitle: "StartBookmark"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::DocumentBuilder::StartBookmark Methode. Markiert die aktuelle Position im Dokument als Lesezeichenanfang in C++."
type: docs
weight: 68000
url: /de/cpp/aspose.words/documentbuilder/startbookmark/
---
## DocumentBuilder::StartBookmark method


Markiert die aktuelle Position im Dokument als Lesezeichen‑Start.

```cpp
System::SharedPtr<Aspose::Words::BookmarkStart> Aspose::Words::DocumentBuilder::StartBookmark(const System::String &bookmarkName)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| bookmarkName | const System::String\& | Name des Lesezeichens. |

### ReturnValue

Der Lesezeichen-Startknoten, der gerade erstellt wurde.
## Hinweise


Lesezeichen in einem Dokument können sich überschneiden und beliebige Bereiche umfassen. Um ein gültiges Lesezeichen zu erstellen, müssen Sie sowohl [StartBookmark()](../) als auch [EndBookmark()](../) mit demselben *bookmarkName*-Parameter aufrufen.

Fehlerhaft gebildete Lesezeichen oder Lesezeichen mit doppelten Namen werden beim Speichern des Dokuments ignoriert.

## Beispiele



Zeigt, wie man ein Lesezeichen erstellt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Ein gültiges Lesezeichen muss den Dokumenten-Body-Text umschließen, der von
// BookmarkStart- und BookmarkEnd-Knoten, die mit einem passenden Lesezeichennamen erstellt wurden.
builder->StartBookmark(u"MyBookmark");
builder->Writeln(u"Hello world!");
builder->EndBookmark(u"MyBookmark");

ASSERT_EQ(1, doc->get_Range()->get_Bookmarks()->get_Count());
ASSERT_EQ(u"MyBookmark", doc->get_Range()->get_Bookmarks()->idx_get(0)->get_Name());
ASSERT_EQ(u"Hello world!", doc->get_Range()->get_Bookmarks()->idx_get(0)->get_Text().Trim());
```


Zeigt, wie man einen Hyperlink einfügt, der auf ein lokales Lesezeichen verweist.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->StartBookmark(u"Bookmark1");
builder->Write(u"Bookmarked text. ");
builder->EndBookmark(u"Bookmark1");
builder->Writeln(u"Text outside of the bookmark.");

// Fügen Sie ein HYPERLINK-Feld ein, das auf das Lesezeichen verweist. Wir können Feldschalter übergeben
// zur "InsertHyperlink"-Methode als Teil des Arguments, das den Namen des referenzierten Lesezeichens enthält.
builder->get_Font()->set_Color(System::Drawing::Color::get_Blue());
builder->get_Font()->set_Underline(Aspose::Words::Underline::Single);
auto hyperlink = System::ExplicitCast<Aspose::Words::Fields::FieldHyperlink>(builder->InsertHyperlink(u"Link to Bookmark1", u"Bookmark1", true));
hyperlink->set_ScreenTip(u"Hyperlink Tip");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertHyperlinkToLocalBookmark.docx");
```

## Siehe auch

* Class [BookmarkStart](../../bookmarkstart/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
