---
title: IReplacingCallback
second_title: Aspose.Words for C++ API Reference
description: Implement this interface if you want to have your own custom method called during a find and replace operation.
type: docs
weight: 27
url: /cpp/aspose.words.replacing/ireplacingcallback/
---
## IReplacingCallback interface


Implement this interface if you want to have your own custom method called during a find and replace operation.

```cpp
class IReplacingCallback : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| virtual [Replacing](./replacing/)(System::SharedPtr\<Aspose::Words::Replacing::ReplacingArgs\>) | A user defined method that is called during a replace operation for each match found just before a replace is made. |

## Examples



Shows how to track the order in which a text replacement operation traverses nodes. 
```cpp
void Order(bool differentFirstPageHeaderFooter)
{
    auto doc = MakeObject<Document>(MyDir + u"Header and footer types.docx");

    SharedPtr<Section> firstPageSection = doc->get_FirstSection();

    auto logger = MakeObject<ExHeaderFooter::ReplaceLog>();
    auto options = MakeObject<FindReplaceOptions>();
    options->set_ReplacingCallback(logger);

    // Using a different header/footer for the first page will affect the search order.
    firstPageSection->get_PageSetup()->set_DifferentFirstPageHeaderFooter(differentFirstPageHeaderFooter);
    doc->get_Range()->Replace(MakeObject<System::Text::RegularExpressions::Regex>(u"(header|footer)"), u"", options);

    if (differentFirstPageHeaderFooter)
    {
        ASSERT_EQ(u"First header\nFirst footer\nSecond header\nSecond footer\nThird header\nThird footer\n", logger->get_Text().Replace(u"\r", u""));
    }
    else
    {
        ASSERT_EQ(u"Third header\nFirst header\nThird footer\nFirst footer\nSecond header\nSecond footer\n", logger->get_Text().Replace(u"\r", u""));
    }
}

class ReplaceLog : public IReplacingCallback
{
public:
    String get_Text()
    {
        return mTextBuilder->ToString();
    }

    ReplaceAction Replacing(SharedPtr<ReplacingArgs> args) override
    {
        mTextBuilder->AppendLine(args->get_MatchNode()->GetText());
        return ReplaceAction::Skip;
    }

    ReplaceLog() : mTextBuilder(MakeObject<System::Text::StringBuilder>())
    {
    }

private:
    SharedPtr<System::Text::StringBuilder> mTextBuilder;
};
```


Shows how to replace all occurrences of a regular expression pattern with another string, while tracking all such replacements. 
```cpp
void ReplaceWithCallback()
{
    auto doc = MakeObject<Document>();
    auto builder = MakeObject<DocumentBuilder>(doc);

    builder->Writeln(String(u"Our new location in New York City is opening tomorrow. ") + u"Hope to see all our NYC-based customers at the opening!");

    // We can use a "FindReplaceOptions" object to modify the find-and-replace process.
    auto options = MakeObject<FindReplaceOptions>();

    // Set a callback that tracks any replacements that the "Replace" method will make.
    auto logger = MakeObject<ExRange::TextFindAndReplacementLogger>();
    options->set_ReplacingCallback(logger);

    doc->get_Range()->Replace(MakeObject<System::Text::RegularExpressions::Regex>(u"New York City|NYC"), u"Washington", options);

    ASSERT_EQ(String(u"Our new location in (Old value:\"New York City\") Washington is opening tomorrow. ") +
                  u"Hope to see all our (Old value:\"NYC\") Washington-based customers at the opening!",
              doc->GetText().Trim());

    ASSERT_EQ(String(u"\"New York City\" converted to \"Washington\" 20 characters into a Run node.\r\n") +
                  u"\"NYC\" converted to \"Washington\" 42 characters into a Run node.",
              logger->GetLog().Trim());
}

class TextFindAndReplacementLogger : public IReplacingCallback
{
public:
    String GetLog()
    {
        return mLog->ToString();
    }

    TextFindAndReplacementLogger() : mLog(MakeObject<System::Text::StringBuilder>())
    {
    }

private:
    SharedPtr<System::Text::StringBuilder> mLog;

    ReplaceAction Replacing(SharedPtr<ReplacingArgs> args) override
    {
        mLog->AppendLine(String::Format(u"\"{0}\" converted to \"{1}\" ", args->get_Match()->get_Value(), args->get_Replacement()) +
                         String::Format(u"{0} characters into a {1} node.", args->get_MatchOffset(), args->get_MatchNode()->get_NodeType()));

        args->set_Replacement(String::Format(u"(Old value:\"{0}\") {1}", args->get_Match()->get_Value(), args->get_Replacement()));
        return ReplaceAction::Replace;
    }
};
```


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

## See Also

* Namespace [Aspose::Words::Replacing](../)
* Library [Aspose.Words](../../)
