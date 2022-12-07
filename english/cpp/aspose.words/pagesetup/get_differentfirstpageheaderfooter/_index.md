---
title: get_DifferentFirstPageHeaderFooter
second_title: Aspose.Words for C++ API Reference
description: True if a different header or footer is used on the first page.
type: docs
weight: 157
url: /cpp/aspose.words/pagesetup/get_differentfirstpageheaderfooter/
---
## PageSetup::get_DifferentFirstPageHeaderFooter method


True if a different header or footer is used on the first page.

```cpp
bool Aspose::Words::PageSetup::get_DifferentFirstPageHeaderFooter()
```


## Examples



Shows how to create headers and footers in a document using [DocumentBuilder](../../documentbuilder/). 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Specify that we want different headers and footers for first, even and odd pages.
builder->get_PageSetup()->set_DifferentFirstPageHeaderFooter(true);
builder->get_PageSetup()->set_OddAndEvenPagesHeaderFooter(true);

// Create the headers, then add three pages to the document to display each header type.
builder->MoveToHeaderFooter(HeaderFooterType::HeaderFirst);
builder->Write(u"Header for the first page");
builder->MoveToHeaderFooter(HeaderFooterType::HeaderEven);
builder->Write(u"Header for even pages");
builder->MoveToHeaderFooter(HeaderFooterType::HeaderPrimary);
builder->Write(u"Header for all other pages");

builder->MoveToSection(0);
builder->Writeln(u"Page1");
builder->InsertBreak(BreakType::PageBreak);
builder->Writeln(u"Page2");
builder->InsertBreak(BreakType::PageBreak);
builder->Writeln(u"Page3");

doc->Save(ArtifactsDir + u"DocumentBuilder.HeadersAndFooters.docx");
```


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


Shows how to enable or disable primary headers/footers. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Below are two types of header/footers.
// 1 -  The "First" header/footer, which appears on the first page of the section.
builder->MoveToHeaderFooter(HeaderFooterType::HeaderFirst);
builder->Writeln(u"First page header.");

builder->MoveToHeaderFooter(HeaderFooterType::FooterFirst);
builder->Writeln(u"First page footer.");

// 2 -  The "Primary" header/footer, which appears on every page in the section.
// We can override the primary header/footer by a first and an even page header/footer.
builder->MoveToHeaderFooter(HeaderFooterType::HeaderPrimary);
builder->Writeln(u"Primary header.");

builder->MoveToHeaderFooter(HeaderFooterType::FooterPrimary);
builder->Writeln(u"Primary footer.");

builder->MoveToSection(0);
builder->Writeln(u"Page 1.");
builder->InsertBreak(BreakType::PageBreak);
builder->Writeln(u"Page 2.");
builder->InsertBreak(BreakType::PageBreak);
builder->Writeln(u"Page 3.");

// Each section has a "PageSetup" object that specifies page appearance-related properties
// such as orientation, size, and borders.
// Set the "DifferentFirstPageHeaderFooter" property to "true" to apply the first header/footer to the first page.
// Set the "DifferentFirstPageHeaderFooter" property to "false"
// to make the first page display the primary header/footer.
builder->get_PageSetup()->set_DifferentFirstPageHeaderFooter(differentFirstPageHeaderFooter);

doc->Save(ArtifactsDir + u"PageSetup.DifferentFirstPageHeaderFooter.docx");
```

## See Also

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
