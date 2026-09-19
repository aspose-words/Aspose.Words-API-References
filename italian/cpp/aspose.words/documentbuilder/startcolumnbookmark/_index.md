---
title: "Metodo Aspose::Words::DocumentBuilder::StartColumnBookmark"
linktitle: "StartColumnBookmark"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::DocumentBuilder::StartColumnBookmark. Contrassegna la posizione corrente nel documento come inizio di un segnalibro di colonna. La posizione deve trovarsi in una cella di tabella in C++."
type: docs
weight: 69000
url: /it/cpp/aspose.words/documentbuilder/startcolumnbookmark/
---
## DocumentBuilder::StartColumnBookmark method


Segna la posizione corrente nel documento come inizio di segnalibro di colonna. La posizione deve trovarsi in una cella di tabella.

```cpp
System::SharedPtr<Aspose::Words::BookmarkStart> Aspose::Words::DocumentBuilder::StartColumnBookmark(const System::String &bookmarkName)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| bookmarkName | const System::String\& | Nome del segnalibro. |

### ReturnValue

Il nodo di inizio segnalibro appena creato.
## Note


Un segnalibro di colonna copre una o più colonne in un intervallo di righe. Per creare un segnalibro valido è necessario chiamare sia [StartColumnBookmark()](../) sia [EndColumnBookmark()](../) con lo stesso parametro *bookmarkName*.

I segnalibri malformati o i segnalibri con nomi duplicati verranno ignorati quando il documento viene salvato.

La posizione effettiva del nodo [BookmarkStart](../../bookmarkstart/) inserito può differire dalla posizione corrente del document builder.

## Esempi



Mostra come creare un segnalibro di colonna.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->StartTable();

builder->InsertCell();
// Le celle 1,2,4,5 saranno contrassegnate con un segnalibro.
builder->StartColumnBookmark(u"MyBookmark_1");
// I segnalibri malformati o i segnalibri con nomi duplicati verranno ignorati quando il documento viene salvato.
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

## Vedi anche

* Class [BookmarkStart](../../bookmarkstart/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
