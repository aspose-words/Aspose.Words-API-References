---
title: "Aspose::Words::Bookmark::Remove Methode"
linktitle: "Remove"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Bookmark::Remove Methode. Entfernt das Lesezeichen aus dem Dokument. Entfernt den Text innerhalb des Lesezeichens in C++ nicht."
type: docs
weight: 11000
url: /de/cpp/aspose.words/bookmark/remove/
---
## Bookmark::Remove method


Entfernt das Lesezeichen aus dem Dokument. Entfernt nicht den Text innerhalb des Lesezeichens.

```cpp
void Aspose::Words::Bookmark::Remove()
```


## Beispiele



Zeigt, wie Lesezeichen aus einem Dokument entfernt werden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Fügen Sie fünf Lesezeichen mit Text innerhalb ihrer Grenzen ein.
for (int32_t i = 1; i <= 5; i++)
{
    System::String bookmarkName = System::String(u"MyBookmark_") + i;

    builder->StartBookmark(bookmarkName);
    builder->Write(System::String::Format(u"Text inside {0}.", bookmarkName));
    builder->EndBookmark(bookmarkName);
    builder->InsertBreak(Aspose::Words::BreakType::ParagraphBreak);
}

// Diese Sammlung speichert Lesezeichen.
System::SharedPtr<Aspose::Words::BookmarkCollection> bookmarks = doc->get_Range()->get_Bookmarks();

ASSERT_EQ(5, bookmarks->get_Count());

// Es gibt mehrere Möglichkeiten, Lesezeichen zu entfernen.
// 1 -  Aufruf der Remove-Methode des Lesezeichens:
bookmarks->idx_get(u"MyBookmark_1")->Remove();

ASSERT_FALSE(bookmarks->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Bookmark>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Bookmark> b)>>([](System::SharedPtr<Aspose::Words::Bookmark> b) -> bool
{
    return b->get_Name() == u"MyBookmark_1";
}))));

// 2 -  Übergabe des Lesezeichens an die Remove-Methode der Sammlung:
System::SharedPtr<Aspose::Words::Bookmark> bookmark = doc->get_Range()->get_Bookmarks()->idx_get(0);
doc->get_Range()->get_Bookmarks()->Remove(bookmark);

ASSERT_FALSE(bookmarks->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Bookmark>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Bookmark> b)>>([](System::SharedPtr<Aspose::Words::Bookmark> b) -> bool
{
    return b->get_Name() == u"MyBookmark_2";
}))));

// 3 -  Entfernen eines Lesezeichens aus der Sammlung nach Name:
doc->get_Range()->get_Bookmarks()->Remove(u"MyBookmark_3");

ASSERT_FALSE(bookmarks->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Bookmark>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Bookmark> b)>>([](System::SharedPtr<Aspose::Words::Bookmark> b) -> bool
{
    return b->get_Name() == u"MyBookmark_3";
}))));

// 4 -  Entfernen eines Lesezeichens an einem Index in der Lesezeichensammlung:
doc->get_Range()->get_Bookmarks()->RemoveAt(0);

ASSERT_FALSE(bookmarks->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Bookmark>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Bookmark> b)>>([](System::SharedPtr<Aspose::Words::Bookmark> b) -> bool
{
    return b->get_Name() == u"MyBookmark_4";
}))));

// Wir können die gesamte Lesezeichensammlung leeren.
bookmarks->Clear();

// Der Text, der sich in den Lesezeichen befand, ist weiterhin im Dokument vorhanden.
ASSERT_EQ(0, bookmarks->get_Count());
ASSERT_EQ(System::String(u"Text inside MyBookmark_1.\r") + u"Text inside MyBookmark_2.\r" + u"Text inside MyBookmark_3.\r" + u"Text inside MyBookmark_4.\r" + u"Text inside MyBookmark_5.", doc->GetText().Trim());
```

## Siehe auch

* Class [Bookmark](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
