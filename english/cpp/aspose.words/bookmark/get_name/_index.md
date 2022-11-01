---
title: get_Name
second_title: Aspose.Words for C++ API Reference
description: Gets or sets the name of the bookmark.
type: docs
weight: 66
url: /cpp/aspose.words/bookmark/get_name/
---
## Bookmark.get_Name method


Gets or sets the name of the bookmark.

```cpp
System::String Aspose::Words::Bookmark::get_Name()
```


## Examples




Shows how to insert a bookmark. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// A valid bookmark has a name, a BookmarkStart, and a BookmarkEnd node.
// Any whitespace in the names of bookmarks will be converted to underscores if we open the saved document with Microsoft Word.
// If we highlight the bookmark's name in Microsoft Word via Insert -> Links -> Bookmark, and press "Go To",
// the cursor will jump to the text enclosed between the BookmarkStart and BookmarkEnd nodes.
builder->StartBookmark(u"My Bookmark");
builder->Write(u"Contents of MyBookmark.");
builder->EndBookmark(u"My Bookmark");

// Bookmarks are stored in this collection.
ASSERT_EQ(u"My Bookmark", doc->get_Range()->get_Bookmarks()->idx_get(0)->get_Name());

doc->Save(ArtifactsDir + u"Bookmarks.Insert.docx");
```


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

