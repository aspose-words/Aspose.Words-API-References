---
title: "Aspose::Words::DocumentBuilder::EndColumnBookmark metod"
linktitle: "EndColumnBookmark"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::DocumentBuilder::EndColumnBookmark metod. Markerar den aktuella positionen i dokumentet som ett kolumnbokmärkes slut. Positionen måste vara i en tabellcell i C++."
type: docs
weight: 5000
url: /sv/cpp/aspose.words/documentbuilder/endcolumnbookmark/
---
## DocumentBuilder::EndColumnBookmark method


Markerar den aktuella positionen i dokumentet som ett kolumnbokmärkes slut. Positionen måste vara i en tabellcell.

```cpp
System::SharedPtr<Aspose::Words::BookmarkEnd> Aspose::Words::DocumentBuilder::EndColumnBookmark(const System::String &bookmarkName)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| bookmarkName | const System::String\& | Namnet på bokmärket. |

### ReturnValue

Bokmärkesavslutsnod som just har skapats.
## Anmärkningar


Ett kolumnbokmärke täcker en eller flera kolumner i ett radintervall. För att skapa ett giltigt bokmärke måste du anropa både [StartColumnBookmark()](../) och [EndColumnBookmark()](../) med samma *bookmarkName*-parameter.

Felaktigt formade bokmärken eller bokmärken med duplicerade namn kommer att ignoreras när dokumentet sparas.

Den faktiska positionen för den infogade [BookmarkEnd](../../bookmarkend/)‑noden kan skilja sig från den aktuella dokumentbyggarens position.

## Exempel



Visar hur man skapar ett kolumnbokmärke.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->StartTable();

builder->InsertCell();
// Cellerna 1,2,4,5 kommer att bokmärkas.
builder->StartColumnBookmark(u"MyBookmark_1");
// Felaktigt formade bokmärken eller bokmärken med duplicerade namn kommer att ignoreras när dokumentet sparas.
builder->StartColumnBookmark(u"MyBookmark_1");
builder->StartColumnBookmark(u"BadStartBookmark");
builder->Write(u"Cell 1");

builder->InsertCell();
builder->Write(u"Cell 2");

builder->InsertCell();
builder->Write(u"Cell 3");

builder->EndRow();

builder->InsertCell();
builder->Write(u"Cell 4");

builder->InsertCell();
builder->Write(u"Cell 5");
builder->EndColumnBookmark(u"MyBookmark_1");
builder->EndColumnBookmark(u"MyBookmark_1");

ASSERT_THROW(static_cast<std::function<void()>>([&builder]() -> void
{
    builder->EndColumnBookmark(u"BadEndBookmark");

builder->InsertCell();
builder->Write(u"Cell 6");

builder->EndRow();
builder->EndTable();

doc->Save(get_ArtifactsDir() + u"Bookmarks.CreateColumnBookmark.docx");
```

## Se även

* Class [BookmarkEnd](../../bookmarkend/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
