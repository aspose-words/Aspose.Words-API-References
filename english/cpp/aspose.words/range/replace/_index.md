---
title: Replace
second_title: Aspose.Words for C++ API Reference
description: Replaces all occurrences of a character pattern specified by a regular expression with another string.
type: docs
weight: 92
url: /cpp/aspose.words/range/replace/
---
## Range.Replace(const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) method


Replaces all occurrences of a character pattern specified by a regular expression with another string.

```cpp
int32_t Aspose::Words::Range::Replace(const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement)
```


| Parameter | Type | Description |
| --- | --- | --- |
| pattern | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | A regular expression pattern used to find matches. |
| replacement | const System::String\& | A string to replace all occurrences of pattern. |

### ReturnValue


The number of replacements made.

Replaces the whole match captured by the regular expression.

Method is able to process breaks in both pattern and replacement strings.

You should use special meta-characters if you need to work with breaks:

* **%&p** - paragraph break
* **%&b** - section break
* **%&m** - page break
* **%&l** - manual line break



## Examples




Shows how to replace all occurrences of a regular expression pattern with other text. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->Writeln(u"I decided to get the curtains in gray, ideal for the grey-accented room.");

doc->get_Range()->Replace(MakeObject<System::Text::RegularExpressions::Regex>(u"gr(a|e)y"), u"lavender");

ASSERT_EQ(u"I decided to get the curtains in lavender, ideal for the lavender-accented room.", doc->GetText().Trim());
```

## Range.Replace(const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


Replaces all occurrences of a character pattern specified by a regular expression with another string.

```cpp
int32_t Aspose::Words::Range::Replace(const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| Parameter | Type | Description |
| --- | --- | --- |
| pattern | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | A regular expression pattern used to find matches. |
| replacement | const System::String\& | A string to replace all occurrences of pattern. |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) object to specify additional options. |

### ReturnValue


The number of replacements made.

Replaces the whole match captured by the regular expression.

Method is able to process breaks in both pattern and replacement strings.

You should use special meta-characters if you need to work with breaks:

* **%&p** - paragraph break
* **%&b** - section break
* **%&m** - page break
* **%&l** - manual line break
* **%&&** - & character



## Examples




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

## Range.Replace(const System::String\&, const System::String\&) method


Replaces all occurrences of a specified character string pattern with a replacement string.

```cpp
int32_t Aspose::Words::Range::Replace(const System::String &pattern, const System::String &replacement)
```


| Parameter | Type | Description |
| --- | --- | --- |
| pattern | const System::String\& | A string to be replaced. |
| replacement | const System::String\& | A string to replace all occurrences of pattern. |

### ReturnValue


The number of replacements made.

The pattern will not be used as regular expression. Please use **Replace()** if you need regular expressions.

Used case-insensitive comparison.

Method is able to process breaks in both pattern and replacement strings.

You should use special meta-characters if you need to work with breaks:

* **%&p** - paragraph break
* **%&b** - section break
* **%&m** - page break
* **%&l** - manual line break



## Examples




Shows how to perform a find-and-replace text operation on the contents of a document. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->Writeln(u"Greetings, _FullName_!");

// Perform a find-and-replace operation on our document's contents and verify the number of replacements that took place.
int replacementCount = doc->get_Range()->Replace(u"_FullName_", u"John Doe");

ASSERT_EQ(1, replacementCount);
ASSERT_EQ(u"Greetings, John Doe!", doc->GetText().Trim());
```


Shows how to add formatting to paragraphs in which a find-and-replace operation has found matches. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->Writeln(u"Every paragraph that ends with a full stop like this one will be right aligned.");
builder->Writeln(u"This one will not!");
builder->Write(u"This one also will.");

SharedPtr<ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();

ASSERT_EQ(ParagraphAlignment::Left, paragraphs->idx_get(0)->get_ParagraphFormat()->get_Alignment());
ASSERT_EQ(ParagraphAlignment::Left, paragraphs->idx_get(1)->get_ParagraphFormat()->get_Alignment());
ASSERT_EQ(ParagraphAlignment::Left, paragraphs->idx_get(2)->get_ParagraphFormat()->get_Alignment());

// We can use a "FindReplaceOptions" object to modify the find-and-replace process.
auto options = MakeObject<FindReplaceOptions>();

// Set the "Alignment" property to "ParagraphAlignment.Right" to right-align every paragraph
// that contains a match that the find-and-replace operation finds.
options->get_ApplyParagraphFormat()->set_Alignment(ParagraphAlignment::Right);

// Replace every full stop that is right before a paragraph break with an exclamation point.
int count = doc->get_Range()->Replace(u".&p", u"!&p", options);

ASSERT_EQ(2, count);
ASSERT_EQ(ParagraphAlignment::Right, paragraphs->idx_get(0)->get_ParagraphFormat()->get_Alignment());
ASSERT_EQ(ParagraphAlignment::Left, paragraphs->idx_get(1)->get_ParagraphFormat()->get_Alignment());
ASSERT_EQ(ParagraphAlignment::Right, paragraphs->idx_get(2)->get_ParagraphFormat()->get_Alignment());
ASSERT_EQ(String(u"Every paragraph that ends with a full stop like this one will be right aligned!\r") + u"This one will not!\r" +
              u"This one also will!",
          doc->GetText().Trim());
```

## Range.Replace(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


Replaces all occurrences of a specified character string pattern with a replacement string.

```cpp
int32_t Aspose::Words::Range::Replace(const System::String &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| Parameter | Type | Description |
| --- | --- | --- |
| pattern | const System::String\& | A string to be replaced. |
| replacement | const System::String\& | A string to replace all occurrences of pattern. |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) object to specify additional options. |

### ReturnValue


The number of replacements made.

The pattern will not be used as regular expression. Please use **Replace()** if you need regular expressions.

Method is able to process breaks in both pattern and replacement strings.

You should use special meta-characters if you need to work with breaks:

* **%&p** - paragraph break
* **%&b** - section break
* **%&m** - page break
* **%&l** - manual line break
* **%&&** - & character



## Examples




Shows how to replace text in a document's footer. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Footer.docx");

SharedPtr<HeaderFooterCollection> headersFooters = doc->get_FirstSection()->get_HeadersFooters();
SharedPtr<HeaderFooter> footer = headersFooters->idx_get(HeaderFooterType::FooterPrimary);

auto options = MakeObject<FindReplaceOptions>();
options->set_MatchCase(false);
options->set_FindWholeWordsOnly(false);

int currentYear = System::DateTime::get_Now().get_Year();
footer->get_Range()->Replace(u"(C) 2006 Aspose Pty Ltd.", String::Format(u"Copyright (C) {0} by Aspose Pty Ltd.", currentYear), options);

doc->Save(ArtifactsDir + u"HeaderFooter.ReplaceText.docx");
```


Shows how to toggle case sensitivity when performing a find-and-replace operation. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->Writeln(u"Ruby bought a ruby necklace.");

// We can use a "FindReplaceOptions" object to modify the find-and-replace process.
auto options = MakeObject<FindReplaceOptions>();

// Set the "MatchCase" flag to "true" to apply case sensitivity while finding strings to replace.
// Set the "MatchCase" flag to "false" to ignore character case while searching for text to replace.
options->set_MatchCase(matchCase);

doc->get_Range()->Replace(u"Ruby", u"Jade", options);

ASSERT_EQ(matchCase ? String(u"Jade bought a ruby necklace.") : String(u"Jade bought a Jade necklace."), doc->GetText().Trim());
```


Shows how to toggle standalone word-only find-and-replace operations. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->Writeln(u"Jackson will meet you in Jacksonville.");

// We can use a "FindReplaceOptions" object to modify the find-and-replace process.
auto options = MakeObject<FindReplaceOptions>();

// Set the "FindWholeWordsOnly" flag to "true" to replace the found text if it is not a part of another word.
// Set the "FindWholeWordsOnly" flag to "false" to replace all text regardless of its surroundings.
options->set_FindWholeWordsOnly(findWholeWordsOnly);

doc->get_Range()->Replace(u"Jackson", u"Louis", options);

ASSERT_EQ(findWholeWordsOnly ? String(u"Louis will meet you in Jacksonville.") : String(u"Louis will meet you in Louisville."), doc->GetText().Trim());
```


Shows how to replace all instances of String of text in a table and cell. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

SharedPtr<Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Carrots");
builder->InsertCell();
builder->Write(u"50");
builder->EndRow();
builder->InsertCell();
builder->Write(u"Potatoes");
builder->InsertCell();
builder->Write(u"50");
builder->EndTable();

auto options = MakeObject<FindReplaceOptions>();
options->set_MatchCase(true);
options->set_FindWholeWordsOnly(true);

// Perform a find-and-replace operation on an entire table.
table->get_Range()->Replace(u"Carrots", u"Eggs", options);

// Perform a find-and-replace operation on the last cell of the last row of the table.
table->get_LastRow()->get_LastCell()->get_Range()->Replace(u"50", u"20", options);

ASSERT_EQ(String(u"Eggs\a50\a\a") + u"Potatoes\a20\a\a", table->GetText().Trim());
```

