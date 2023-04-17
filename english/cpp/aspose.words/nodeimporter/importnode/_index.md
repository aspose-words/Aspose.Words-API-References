---
title: Aspose::Words::NodeImporter::ImportNode method
linktitle: ImportNode
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::NodeImporter::ImportNode method. Imports a node from one document into another in C++.'
type: docs
weight: 4000
url: /cpp/aspose.words/nodeimporter/importnode/
---
## NodeImporter::ImportNode method


Imports a node from one document into another.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::NodeImporter::ImportNode(const System::SharedPtr<Aspose::Words::Node> &srcNode, bool isImportChildren)
```


| Parameter | Type | Description |
| --- | --- | --- |
| srcNode | const System::SharedPtr\<Aspose::Words::Node\>\& | The node to import. |
| isImportChildren | bool | **true** to import all child nodes recursively; otherwise, **false**. |

### ReturnValue

The cloned, imported node. The node belongs to the destination document, but has no parent.
## Remarks


Importing a node creates a copy of the source node belonging to the importing document. The returned node has no parent. The source node is not altered or removed from the original document.

Before a node from another document can be inserted into this document, it must be imported. During import, document-specific properties such as references to styles and lists are translated from the original to the importing document. After the node was imported, it can be inserted into the appropriate place in the document using [InsertBefore()](../) or [InsertAfter()](../).

If the source node already belongs to the destination document, then simply a deep clone of the source node is created.

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

* Class [Node](../../node/)
* Class [NodeImporter](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
