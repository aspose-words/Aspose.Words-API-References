---
title: ReplaceAction
second_title: Aspose.Words for C++ API Reference
description: Allows the user to specify what happens to the current match during a replace operation.
type: docs
weight: 53
url: /cpp/aspose.words.replacing/replaceaction/
---
## ReplaceAction enum


Allows the user to specify what happens to the current match during a replace operation.

### Values

| Name | Value | Description |
| --- | --- | --- |
| Replace | 0 | Replace the current match. |
| Skip | 1 | Skip the current match. |
| Stop | 2 | Terminate the replace operation. |


## Examples




Shows how to insert an entire document's contents as a replacement of a match in a find-and-replace operation. 
```cpp
void InsertDocumentAtReplace()
{
    auto mainDoc = MakeObject<Document>(MyDir + u"Document insertion destination.docx");

    // We can use a "FindReplaceOptions" object to modify the find-and-replace process.
    auto options = MakeObject<FindReplaceOptions>();
    options->set_ReplacingCallback(MakeObject<ExRange::InsertDocumentAtReplaceHandler>());

    mainDoc->get_Range()->Replace(MakeObject<System::Text::RegularExpressions::Regex>(u"\\[MY_DOCUMENT\\]"), u"", options);
    mainDoc->Save(ArtifactsDir + u"InsertDocument.InsertDocumentAtReplace.docx");

}

class InsertDocumentAtReplaceHandler : public IReplacingCallback
{
private:
    ReplaceAction Replacing(SharedPtr<ReplacingArgs> args) override
    {
        auto subDoc = MakeObject<Document>(MyDir + u"Document.docx");

        // Insert a document after the paragraph containing the matched text.
        auto para = System::DynamicCast<Paragraph>(args->get_MatchNode()->get_ParentNode());
        InsertDocument(para, subDoc);

        // Remove the paragraph with the matched text.
        para->Remove();

        return ReplaceAction::Skip;
    }
};

static void InsertDocument(SharedPtr<Node> insertionDestination, SharedPtr<Document> docToInsert)
{
    if (insertionDestination->get_NodeType() == NodeType::Paragraph || insertionDestination->get_NodeType() == NodeType::Table)
    {
        SharedPtr<CompositeNode> dstStory = insertionDestination->get_ParentNode();

        auto importer = MakeObject<NodeImporter>(docToInsert, insertionDestination->get_Document(), ImportFormatMode::KeepSourceFormatting);

        for (const auto& srcSection : System::IterateOver(docToInsert->get_Sections()->LINQ_OfType<SharedPtr<Section>>()))
        {
            for (const auto& srcNode : System::IterateOver(srcSection->get_Body()))
            {
                // Skip the node if it is the last empty paragraph in a section.
                if (srcNode->get_NodeType() == NodeType::Paragraph)
                {
                    auto para = System::DynamicCast<Paragraph>(srcNode);
                    if (para->get_IsEndOfSection() && !para->get_HasChildNodes())
                    {
                        continue;
                    }
                }

                SharedPtr<Node> newNode = importer->ImportNode(srcNode, true);

                dstStory->InsertAfter(newNode, insertionDestination);
                insertionDestination = newNode;
            }
        }
    }
    else
    {
        throw System::ArgumentException(u"The destination node must be either a paragraph or table.");
    }
}
```

