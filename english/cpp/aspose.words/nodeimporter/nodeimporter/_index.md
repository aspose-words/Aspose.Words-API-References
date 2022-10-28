---
title: NodeImporter
second_title: Aspose.Words for C++ API Reference
description: Initializes a new instance of the NodeImporter class.
type: docs
weight: 1
url: /cpp/aspose.words/nodeimporter/nodeimporter/
---
## NodeImporter.NodeImporter(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, Aspose::Words::ImportFormatMode) method


Initializes a new instance of the [NodeImporter](../) class.

```cpp
Aspose::Words::NodeImporter::NodeImporter(const System::SharedPtr<Aspose::Words::DocumentBase> &srcDoc, const System::SharedPtr<Aspose::Words::DocumentBase> &dstDoc, Aspose::Words::ImportFormatMode importFormatMode)
```


| Parameter | Type | Description |
| --- | --- | --- |
| srcDoc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | The source document. |
| dstDoc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | The destination document that will be the owner of imported nodes. |
| importFormatMode | Aspose::Words::ImportFormatMode | Specifies how to merge style formatting that clashes. |

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

## NodeImporter.NodeImporter(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, Aspose::Words::ImportFormatMode, const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\&) method


Initializes a new instance of the [NodeImporter](../) class.

```cpp
Aspose::Words::NodeImporter::NodeImporter(const System::SharedPtr<Aspose::Words::DocumentBase> &srcDoc, const System::SharedPtr<Aspose::Words::DocumentBase> &dstDoc, Aspose::Words::ImportFormatMode importFormatMode, const System::SharedPtr<Aspose::Words::ImportFormatOptions> &importFormatOptions)
```


| Parameter | Type | Description |
| --- | --- | --- |
| srcDoc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | The source document. |
| dstDoc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | The destination document that will be the owner of imported nodes. |
| importFormatMode | Aspose::Words::ImportFormatMode | Specifies how to merge style formatting that clashes. |
| importFormatOptions | const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\& | Specifies various options to format imported node. |

## Examples




Shows how resolve a clash when importing documents that have lists with the same list definition identifier. 
```cpp
auto srcDoc = MakeObject<Document>(MyDir + u"List with the same definition identifier - source.docx");
auto dstDoc = MakeObject<Document>(MyDir + u"List with the same definition identifier - destination.docx");

// Set the "KeepSourceNumbering" property to "true" to apply a different list definition ID
// to identical styles as Aspose.Words imports them into destination documents.
auto importFormatOptions = MakeObject<ImportFormatOptions>();
importFormatOptions->set_KeepSourceNumbering(true);

dstDoc->AppendDocument(srcDoc, ImportFormatMode::UseDestinationStyles, importFormatOptions);
dstDoc->UpdateListLabels();
```


Shows how to resolve list numbering clashes in source and destination documents. 
```cpp
// Open a document with a custom list numbering scheme, and then clone it.
// Since both have the same numbering format, the formats will clash if we import one document into the other.
auto srcDoc = MakeObject<Document>(MyDir + u"Custom list numbering.docx");
SharedPtr<Document> dstDoc = srcDoc->Clone();

// When we import the document's clone into the original and then append it,
// then the two lists with the same list format will join.
// If we set the "KeepSourceNumbering" flag to "false", then the list from the document clone
// that we append to the original will carry on the numbering of the list we append it to.
// This will effectively merge the two lists into one.
// If we set the "KeepSourceNumbering" flag to "true", then the document clone
// list will preserve its original numbering, making the two lists appear as separate lists.
auto importFormatOptions = MakeObject<ImportFormatOptions>();
importFormatOptions->set_KeepSourceNumbering(keepSourceNumbering);

auto importer = MakeObject<NodeImporter>(srcDoc, dstDoc, ImportFormatMode::KeepDifferentStyles, importFormatOptions);
for (const auto& paragraph : System::IterateOver<Paragraph>(srcDoc->get_FirstSection()->get_Body()->get_Paragraphs()))
{
    SharedPtr<Node> importedNode = importer->ImportNode(paragraph, true);
    dstDoc->get_FirstSection()->get_Body()->AppendChild(importedNode);
}

dstDoc->UpdateListLabels();

if (keepSourceNumbering)
{
    ASSERT_EQ(String(u"6. Item 1\r\n") + u"7. Item 2 \r\n" + u"8. Item 3\r\n" + u"9. Item 4\r\n" + u"6. Item 1\r\n" + u"7. Item 2 \r\n" +
                  u"8. Item 3\r\n" + u"9. Item 4",
              dstDoc->get_FirstSection()->get_Body()->ToString(SaveFormat::Text).Trim());
}
else
{
    ASSERT_EQ(String(u"6. Item 1\r\n") + u"7. Item 2 \r\n" + u"8. Item 3\r\n" + u"9. Item 4\r\n" + u"10. Item 1\r\n" + u"11. Item 2 \r\n" +
                  u"12. Item 3\r\n" + u"13. Item 4",
              dstDoc->get_FirstSection()->get_Body()->ToString(SaveFormat::Text).Trim());
}
```

