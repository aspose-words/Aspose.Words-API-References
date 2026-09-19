---
title: "Metodo Aspose::Words::BookmarkCollection::RemoveAt"
linktitle: "RemoveAt"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::BookmarkCollection::RemoveAt. Rimuove un segnalibro all'indice specificato in C++."
type: docs
weight: 9000
url: /it/cpp/aspose.words/bookmarkcollection/removeat/
---
## BookmarkCollection::RemoveAt method


Rimuove un segnalibro all'indice specificato.

```cpp
void Aspose::Words::BookmarkCollection::RemoveAt(int32_t index)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| index | int32_t | L'indice basato su zero del segnalibro da rimuovere. |

## Esempi



Mostra come rimuovere i segnalibri da un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserisci cinque segnalibri con testo all'interno dei loro confini.
for (int32_t i = 1; i <= 5; i++)
{
    System::String bookmarkName = System::String(u"MyBookmark_") + i;

    builder->StartBookmark(bookmarkName);
    builder->Write(System::String::Format(u"Text inside {0}.", bookmarkName));
    builder->EndBookmark(bookmarkName);
    builder->InsertBreak(Aspose::Words::BreakType::ParagraphBreak);
}

// Questa collezione memorizza i segnalibri.
System::SharedPtr<Aspose::Words::BookmarkCollection> bookmarks = doc->get_Range()->get_Bookmarks();

ASSERT_EQ(5, bookmarks->get_Count());

// Esistono diversi modi per rimuovere i segnalibri.
// 1 -  Chiamata al metodo Remove del segnalibro:
bookmarks->idx_get(u"MyBookmark_1")->Remove();

ASSERT_FALSE(bookmarks->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Bookmark>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Bookmark> b)>>([](System::SharedPtr<Aspose::Words::Bookmark> b) -> bool
{
    return b->get_Name() == u"MyBookmark_1";
}))));

// 2 -  Passaggio del segnalibro al metodo Remove della collezione:
System::SharedPtr<Aspose::Words::Bookmark> bookmark = doc->get_Range()->get_Bookmarks()->idx_get(0);
doc->get_Range()->get_Bookmarks()->Remove(bookmark);

ASSERT_FALSE(bookmarks->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Bookmark>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Bookmark> b)>>([](System::SharedPtr<Aspose::Words::Bookmark> b) -> bool
{
    return b->get_Name() == u"MyBookmark_2";
}))));

// 3 -  Rimozione di un segnalibro dalla collezione per nome:
doc->get_Range()->get_Bookmarks()->Remove(u"MyBookmark_3");

ASSERT_FALSE(bookmarks->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Bookmark>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Bookmark> b)>>([](System::SharedPtr<Aspose::Words::Bookmark> b) -> bool
{
    return b->get_Name() == u"MyBookmark_3";
}))));

// 4 -  Rimozione di un segnalibro a un indice nella collezione di segnalibri:
doc->get_Range()->get_Bookmarks()->RemoveAt(0);

ASSERT_FALSE(bookmarks->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Bookmark>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Bookmark> b)>>([](System::SharedPtr<Aspose::Words::Bookmark> b) -> bool
{
    return b->get_Name() == u"MyBookmark_4";
}))));

// Possiamo svuotare l'intera collezione di segnalibri.
bookmarks->Clear();

// Il testo che era all'interno dei segnalibri è ancora presente nel documento.
ASSERT_EQ(0, bookmarks->get_Count());
ASSERT_EQ(System::String(u"Text inside MyBookmark_1.\r") + u"Text inside MyBookmark_2.\r" + u"Text inside MyBookmark_3.\r" + u"Text inside MyBookmark_4.\r" + u"Text inside MyBookmark_5.", doc->GetText().Trim());
```

## Vedi anche

* Class [BookmarkCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
