---
title: "Aspose::Words::DocumentBuilder::StartColumnBookmark Methode"
linktitle: "StartColumnBookmark"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::DocumentBuilder::StartColumnBookmark Methode. Markiert die aktuelle Position im Dokument als Beginn eines Spalten-Lesezeichens. Die Position muss sich in einer Tabellenzelle in C++ befinden."
type: docs
weight: 69000
url: /de/cpp/aspose.words/documentbuilder/startcolumnbookmark/
---
## DocumentBuilder::StartColumnBookmark method


Markiert die aktuelle Position im Dokument als Spalten‑Lesezeichen‑Start. Die Position muss sich in einer Tabellenzelle befinden.

```cpp
System::SharedPtr<Aspose::Words::BookmarkStart> Aspose::Words::DocumentBuilder::StartColumnBookmark(const System::String &bookmarkName)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| bookmarkName | const System::String\& | Name des Lesezeichens. |

### ReturnValue

Der Lesezeichen-Startknoten, der gerade erstellt wurde.
## Hinweise


Ein Spalten-Lesezeichen erstreckt sich über eine oder mehrere Spalten in einem Zeilenbereich. Um ein gültiges Lesezeichen zu erstellen, müssen Sie sowohl [StartColumnBookmark()](../) als auch [EndColumnBookmark()](../) mit demselben *bookmarkName*-Parameter aufrufen.

Fehlerhaft gebildete Lesezeichen oder Lesezeichen mit doppelten Namen werden beim Speichern des Dokuments ignoriert.

Die tatsächliche Position des eingefügten [BookmarkStart](../../bookmarkstart/) Knotens kann von der aktuellen Position des Document Builders abweichen.

## Beispiele



Zeigt, wie man ein Spalten-Lesezeichen erstellt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->StartTable();

builder->InsertCell();
// Die Zellen 1,2,4,5 werden als Lesezeichen markiert.
builder->StartColumnBookmark(u"MyBookmark_1");
// Fehlerhaft gebildete Lesezeichen oder Lesezeichen mit doppelten Namen werden beim Speichern des Dokuments ignoriert.
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

## Siehe auch

* Class [BookmarkStart](../../bookmarkstart/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
