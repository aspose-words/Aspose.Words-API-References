---
title: "Aspose::Words::DocumentBuilder::EndBookmark‑metod"
linktitle: "EndBookmark"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::DocumentBuilder::EndBookmark‑metod. Markerar den aktuella positionen i dokumentet som ett bokmärkesavslut i C++."
type: docs
weight: 4000
url: /sv/cpp/aspose.words/documentbuilder/endbookmark/
---
## DocumentBuilder::EndBookmark method


Markerar den aktuella positionen i dokumentet som ett bokmärkes slut.

```cpp
System::SharedPtr<Aspose::Words::BookmarkEnd> Aspose::Words::DocumentBuilder::EndBookmark(const System::String &bookmarkName)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| bookmarkName | const System::String\& | Namnet på bokmärket. |

### ReturnValue

Bokmärkesavslutsnod som just har skapats.
## Anmärkningar


Bokmärken i ett dokument kan överlappa och sträcka sig över vilket område som helst. För att skapa ett giltigt bokmärke måste du anropa både [StartBookmark()](../) och [EndBookmark()](../) med samma *bookmarkName*-parameter.

Felaktigt formade bokmärken eller bokmärken med duplicerade namn kommer att ignoreras när dokumentet sparas.

## Exempel



Visar hur man skapar ett bokmärke.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Ett giltigt bokmärke måste ha dokumentets brödtext omsluten av
// BookmarkStart- och BookmarkEnd‑noder som skapats med ett matchande bokmärkesnamn.
builder->StartBookmark(u"MyBookmark");
builder->Writeln(u"Hello world!");
builder->EndBookmark(u"MyBookmark");

ASSERT_EQ(1, doc->get_Range()->get_Bookmarks()->get_Count());
ASSERT_EQ(u"MyBookmark", doc->get_Range()->get_Bookmarks()->idx_get(0)->get_Name());
ASSERT_EQ(u"Hello world!", doc->get_Range()->get_Bookmarks()->idx_get(0)->get_Text().Trim());
```


Visar hur man infogar en hyperlänk som refererar till ett lokalt bokmärke.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->StartBookmark(u"Bookmark1");
builder->Write(u"Bookmarked text. ");
builder->EndBookmark(u"Bookmark1");
builder->Writeln(u"Text outside of the bookmark.");

// Infoga ett HYPERLINK‑fält som länkar till bokmärket. Vi kan skicka fältväxlar
// till metoden "InsertHyperlink" som en del av argumentet som innehåller det refererade bokmärkets namn.
builder->get_Font()->set_Color(System::Drawing::Color::get_Blue());
builder->get_Font()->set_Underline(Aspose::Words::Underline::Single);
auto hyperlink = System::ExplicitCast<Aspose::Words::Fields::FieldHyperlink>(builder->InsertHyperlink(u"Link to Bookmark1", u"Bookmark1", true));
hyperlink->set_ScreenTip(u"Hyperlink Tip");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertHyperlinkToLocalBookmark.docx");
```

## Se även

* Class [BookmarkEnd](../../bookmarkend/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
