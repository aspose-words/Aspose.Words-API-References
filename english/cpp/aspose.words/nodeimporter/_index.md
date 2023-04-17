---
title: Aspose::Words::NodeImporter class
linktitle: NodeImporter
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::NodeImporter class. Allows to efficiently perform repeated import of nodes from one document to another. To learn more, visit the  documentation article in C++.'
type: docs
weight: 44000
url: /cpp/aspose.words/nodeimporter/
---
## NodeImporter class


Allows to efficiently perform repeated import of nodes from one document to another. To learn more, visit the [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/) documentation article.

```cpp
class NodeImporter : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [ImportNode](./importnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&, bool) | Imports a node from one document into another. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [NodeImporter](./nodeimporter/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, Aspose::Words::ImportFormatMode) | Initializes a new instance of the [NodeImporter](./) class. |
| [NodeImporter](./nodeimporter/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, Aspose::Words::ImportFormatMode, const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\&) | Initializes a new instance of the [NodeImporter](./) class. |
| static [Type](./type/)() |  |
## Remarks


Aspose.Words provides functionality for easy copying and moving fragments between Microsoft Word documents. This is known as "importing nodes". Before you can insert a fragment from one document into another, you need to "import" it. Importing creates a deep clone of the original node, ready to be inserted into the destination document.

The simplest way to import a node is to use the [ImportNode()](../) method provided by the [DocumentBase](../documentbase/) object.

However, when you need to import nodes from one document to another multiple times, it is better to use the [NodeImporter](./) class. The [NodeImporter](./) class allows to minimize the number of styles and lists created in the destination document.

Copying or moving fragments from one Microsoft Word document to another presents a number of technical challenges for Aspose.Words. In a Word document, styles and list formatting are stored centrally, separately from the text of the document. The paragraphs and runs of text merely reference the styles by internal unique identifiers.

The challenges arise from the fact that styles and lists are different in different documents. For example, to copy a paragraph formatted with the Heading 1 style from one document to another, a number of things must be taken into account: decide whether to copy the Heading 1 style from the source document to the destination document, clone the paragraph, update the cloned paragraph so it refers to the correct Heading 1 style in the destination document. If the style had to be copied, all the styles that it references (based on style and next paragraph style) should be analyzed and possibly copied too and so on. Similar issues exist when copying bulleted or numbered paragraphs because Microsoft Word stores list definitions separately from text.

The [NodeImporter](./) class is like a context, that holds the "translation tables" during the import. It correctly translates between styles and lists in the source and destination documents.

## Examples



Shows how to insert the contents of one document to a bookmark in another document. 
```cpp
void InsertAtBookmark()
{
    auto doc = MakeObject<Document>();
    auto builder = MakeObject<DocumentBuilder>(doc);

    builder->StartBookmark(u"InsertionPoint");
    builder->Write(u"We will insert a document here: ");
    builder->EndBookmark(u"InsertionPoint");

    auto docToInsert = MakeObject<Document>();
    builder = MakeObject<DocumentBuilder>(docToInsert);

    builder->Write(u"Hello world!");

    docToInsert->Save(ArtifactsDir + u"NodeImporter.InsertAtMergeField.docx");

    SharedPtr<Bookmark> bookmark = doc->get_Range()->get_Bookmarks()->idx_get(u"InsertionPoint");
    InsertDocument(bookmark->get_BookmarkStart()->get_ParentNode(), docToInsert);

    ASSERT_EQ(String(u"We will insert a document here: ") + u"\rHello world!", doc->GetText().Trim());
}

static void InsertDocument(SharedPtr<Node> insertionDestination, SharedPtr<Document> docToInsert)
{
    if (insertionDestination->get_NodeType() == NodeType::Paragraph || insertionDestination->get_NodeType() == NodeType::Table)
    {
        SharedPtr<CompositeNode> destinationParent = insertionDestination->get_ParentNode();

        auto importer = MakeObject<NodeImporter>(docToInsert, insertionDestination->get_Document(), ImportFormatMode::KeepSourceFormatting);

        // Loop through all block-level nodes in the section's body,
        // then clone and insert every node that is not the last empty paragraph of a section.
        for (const auto& srcSection : System::IterateOver(docToInsert->get_Sections()->LINQ_OfType<SharedPtr<Section>>()))
        {
            for (const auto& srcNode : System::IterateOver(srcSection->get_Body()))
            {
                if (srcNode->get_NodeType() == NodeType::Paragraph)
                {
                    auto para = System::DynamicCast<Paragraph>(srcNode);
                    if (para->get_IsEndOfSection() && !para->get_HasChildNodes())
                    {
                        continue;
                    }
                }

                SharedPtr<Node> newNode = importer->ImportNode(srcNode, true);

                destinationParent->InsertAfter(newNode, insertionDestination);
                insertionDestination = newNode;
            }
        }
    }
    else
    {
        throw System::ArgumentException(u"The destination node should be either a paragraph or table.");
    }
}
```

## See Also

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
