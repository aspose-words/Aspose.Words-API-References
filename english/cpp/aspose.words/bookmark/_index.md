---
title: Bookmark
second_title: Aspose.Words for C++ API Reference
description: Represents a single bookmark. To learn more, visit the  documentation article.
type: docs
weight: 27
url: /cpp/aspose.words/bookmark/
---
## Bookmark class


Represents a single bookmark. To learn more, visit the [Working with Bookmarks](https://docs.aspose.com/words/cpp/working-with-bookmarks/) documentation article.

```cpp
class Bookmark : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [get_BookmarkEnd](./get_bookmarkend/)() | Gets the node that represents the end of the bookmark. |
| [get_BookmarkStart](./get_bookmarkstart/)() const | Gets the node that represents the start of the bookmark. |
| [get_FirstColumn](./get_firstcolumn/)() | Gets the zero-based index of the first column of the table column range associated with the bookmark. |
| [get_IsColumn](./get_iscolumn/)() | Returns **true** if this bookmark is a table column bookmark. |
| [get_LastColumn](./get_lastcolumn/)() | Gets the zero-based index of the last column of the table column range associated with the bookmark. |
| [get_Name](./get_name/)() | Gets or sets the name of the bookmark. |
| [get_Text](./get_text/)() | Gets or sets the text enclosed in the bookmark. |
| [Remove](./remove/)() | Removes the bookmark from the document. Does not remove text inside the bookmark. |
| [set_Name](./set_name/)(const System::String\&) | Setter for [Aspose::Words::Bookmark::get_Name](./get_name/). |
| [set_Text](./set_text/)(const System::String\&) | Setter for [Aspose::Words::Bookmark::get_Text](./get_text/). |
## Remarks


[Bookmark](./) is a "facade" object that encapsulates two nodes [BookmarkStart](./get_bookmarkstart/) and [BookmarkEnd](./get_bookmarkend/) in a document tree and allows to work with a bookmark as a single object.

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
