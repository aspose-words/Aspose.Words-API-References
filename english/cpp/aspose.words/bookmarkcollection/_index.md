---
title: BookmarkCollection
second_title: Aspose.Words for C++ API Reference
description: A collection of Bookmark objects that represent the bookmarks in the specified range.
type: docs
weight: 40
url: /cpp/aspose.words/bookmarkcollection/
---
## BookmarkCollection class


A collection of [Bookmark](../bookmark/) objects that represent the bookmarks in the specified range.

```cpp
class BookmarkCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Bookmark>>
```

## Methods

| Method | Description |
| --- | --- |
| [Clear](./clear/)() | Removes all bookmarks from this collection and from the document. |
| [get_Count](./get_count/)() | Returns the number of bookmarks in the collection. |
| [GetEnumerator](./getenumerator/)() override | Returns an enumerator object. |
| [idx_get](./idx_get/)(int32_t) | Returns a bookmark at the specified index. |
| [idx_get](./idx_get/)(const System::String\&) | Returns a bookmark by name. |
| [Remove](./remove/)(const System::SharedPtr\<Aspose::Words::Bookmark\>\&) | Removes the specified bookmark from the document. |
| [Remove](./remove/)(const System::String\&) | Removes a bookmark with the specified name. |
| [RemoveAt](./removeat/)(int32_t) | Removes a bookmark at the specified index. |

## Examples



Shows how to add bookmarks and update their contents. 
```cpp
void CreateUpdateAndPrintBookmarks()
{
    // Create a document with three bookmarks, then use a custom document visitor implementation to print their contents.
    SharedPtr<Document> doc = CreateDocumentWithBookmarks(3);
    SharedPtr<BookmarkCollection> bookmarks = doc->get_Range()->get_Bookmarks();

    PrintAllBookmarkInfo(bookmarks);

    // Bookmarks can be accessed in the bookmark collection by index or name, and their names can be updated.
    bookmarks->idx_get(0)->set_Name(String::Format(u"{0}_NewName", bookmarks->idx_get(0)->get_Name()));
    bookmarks->idx_get(u"MyBookmark_2")->set_Text(String::Format(u"Updated text contents of {0}", bookmarks->idx_get(1)->get_Name()));

    // Print all bookmarks again to see updated values.
    PrintAllBookmarkInfo(bookmarks);
}

static SharedPtr<Document> CreateDocumentWithBookmarks(int numberOfBookmarks)
{
    auto doc = MakeObject<Document>();
    auto builder = MakeObject<DocumentBuilder>(doc);

    for (int i = 1; i <= numberOfBookmarks; i++)
    {
        String bookmarkName = String(u"MyBookmark_") + i;

        builder->Write(u"Text before bookmark.");
        builder->StartBookmark(bookmarkName);
        builder->Write(String::Format(u"Text inside {0}.", bookmarkName));
        builder->EndBookmark(bookmarkName);
        builder->Writeln(u"Text after bookmark.");
    }

    return doc;
}

static void PrintAllBookmarkInfo(SharedPtr<BookmarkCollection> bookmarks)
{
    auto bookmarkVisitor = MakeObject<ExBookmarks::BookmarkInfoPrinter>();

    // Get each bookmark in the collection to accept a visitor that will print its contents.
    {
        SharedPtr<System::Collections::Generic::IEnumerator<SharedPtr<Bookmark>>> enumerator = bookmarks->GetEnumerator();
        while (enumerator->MoveNext())
        {
            SharedPtr<Bookmark> currentBookmark = enumerator->get_Current();

            if (currentBookmark != nullptr)
            {
                currentBookmark->get_BookmarkStart()->Accept(bookmarkVisitor);
                currentBookmark->get_BookmarkEnd()->Accept(bookmarkVisitor);

                std::cout << currentBookmark->get_BookmarkStart()->GetText() << std::endl;
            }
        }
    }
}

class BookmarkInfoPrinter : public DocumentVisitor
{
public:
    VisitorAction VisitBookmarkStart(SharedPtr<BookmarkStart> bookmarkStart) override
    {
        std::cout << "BookmarkStart name: \"" << bookmarkStart->get_Name() << "\", Contents: \"" << bookmarkStart->get_Bookmark()->get_Text() << "\""
                  << std::endl;
        return VisitorAction::Continue;
    }

    VisitorAction VisitBookmarkEnd(SharedPtr<BookmarkEnd> bookmarkEnd) override
    {
        std::cout << "BookmarkEnd name: \"" << bookmarkEnd->get_Name() << "\"" << std::endl;
        return VisitorAction::Continue;
    }
};
```

## See Also

* Namespace [Aspose::Words](../)
* Library [Aspose.Words](../../)
