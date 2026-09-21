---
title: "Aspose::Words::DocumentBuilder::StartColumnBookmark metod"
linktitle: "StartColumnBookmark"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::DocumentBuilder::StartColumnBookmark metod. Markerar den aktuella positionen i dokumentet som en kolumnbokmärkesstart. Positionen måste vara i en tabellcell i C++."
type: docs
weight: 69000
url: /sv/cpp/aspose.words/documentbuilder/startcolumnbookmark/
---
## DocumentBuilder::StartColumnBookmark method


Markerar den aktuella positionen i dokumentet som en kolumnbokmärkestart. Positionen måste vara i en tabellcell.

```cpp
System::SharedPtr<Aspose::Words::BookmarkStart> Aspose::Words::DocumentBuilder::StartColumnBookmark(const System::String &bookmarkName)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| bookmarkName | const System::String\& | Namnet på bokmärket. |

### ReturnValue

Bokmärkesstartnoden som just skapades.
## Anmärkningar


Ett kolumnbokmärke täcker en eller flera kolumner i ett radintervall. För att skapa ett giltigt bokmärke måste du anropa både [StartColumnBookmark()](../) och [EndColumnBookmark()](../) med samma *bookmarkName*-parameter.

Felaktigt formade bokmärken eller bokmärken med duplicerade namn kommer att ignoreras när dokumentet sparas.

Den faktiska positionen för den infogade [BookmarkStart](../../bookmarkstart/) noden kan skilja sig från den aktuella dokumentbyggarens position.

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

* Class [BookmarkStart](../../bookmarkstart/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
