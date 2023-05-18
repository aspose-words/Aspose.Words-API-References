---
title: Aspose::Words::BookmarkEnd class
linktitle: BookmarkEnd
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::BookmarkEnd class. Represents an end of a bookmark in a Word document. To learn more, visit the  documentation article in C++.'
type: docs
weight: 5000
url: /cpp/aspose.words/bookmarkend/
---
## BookmarkEnd class


Represents an end of a bookmark in a Word document. To learn more, visit the [Working with Bookmarks](https://docs.aspose.com/words/cpp/working-with-bookmarks/) documentation article.

```cpp
class BookmarkEnd : public Aspose::Words::Node,
                    public Aspose::Words::IBookmarkNode,
                    public Aspose::Words::IDisplaceableByCustomXml
```

## Methods

| Method | Description |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepts a visitor. |
| [BookmarkEnd](./bookmarkend/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, const System::String\&) | Initializes a new instance of the [BookmarkEnd](./) class. |
| [Clone](../node/clone/)(bool) | Creates a duplicate of the node. |
| [get_CustomNodeId](../node/get_customnodeid/)() const | Specifies custom node identifier. |
| virtual [get_Document](../node/get_document/)() const | Gets the document to which this node belongs. |
| virtual [get_IsComposite](../node/get_iscomposite/)() | Returns **true** if this node can contain other nodes. |
| [get_Name](./get_name/)() override | Gets or sets the bookmark name. |
| [get_NextSibling](../node/get_nextsibling/)() | Gets the node immediately following this node. |
| [get_NodeType](./get_nodetype/)() const override | Returns [BookmarkEnd](../nodetype/). |
| [get_ParentNode](../node/get_parentnode/)() | Gets the immediate parent of this node. |
| [get_PreviousSibling](../node/get_previoussibling/)() | Gets the node immediately preceding this node. |
| [get_Range](../node/get_range/)() | Returns a [Range](../range/) object that represents the portion of a document that is contained in this node. |
| [GetAncestor](../node/getancestor/)(Aspose::Words::NodeType) | Gets the first ancestor of the specified [NodeType](../nodetype/). |
| [GetAncestorOf](../node/getancestorof/)() |  |
| virtual [GetText](../node/gettext/)() | Gets the text of this node and of all its children. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [NextPreOrder](../node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Gets next node according to the pre-order tree traversal algorithm. |
| static [NodeTypeToString](../node/nodetypetostring/)(Aspose::Words::NodeType) | A utility method that converts a node type enum value into a user friendly string. |
| [PreviousPreOrder](../node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Gets the previous node according to the pre-order tree traversal algorithm. |
| [Remove](../node/remove/)() | Removes itself from the parent. |
| [set_CustomNodeId](../node/set_customnodeid/)(int32_t) | Setter for [Aspose::Words::Node::get_CustomNodeId](../node/get_customnodeid/). |
| [set_Name](./set_name/)(System::String) override | Setter for [Aspose::Words::BookmarkEnd::get_Name](./get_name/). |
| [ToString](../node/tostring/)(Aspose::Words::SaveFormat) | Exports the content of the node into a string in the specified format. |
| [ToString](../node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Exports the content of the node into a string using the specified save options. |
| static [Type](./type/)() |  |
## Remarks


A complete bookmark in a Word document consists of a [BookmarkStart](../bookmarkstart/) and a matching [BookmarkEnd](./) with the same bookmark name.

[BookmarkStart](../bookmarkstart/) and [BookmarkEnd](./) are just markers inside a document that specify where the bookmark starts and ends.

Use the [Bookmark](../bookmark/) class as a "facade" to work with a bookmark as a single object.

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

* Class [Node](../node/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
