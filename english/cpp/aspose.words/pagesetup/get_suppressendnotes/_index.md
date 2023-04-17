---
title: Aspose::Words::PageSetup::get_SuppressEndnotes method
linktitle: get_SuppressEndnotes
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::PageSetup::get_SuppressEndnotes method. True if endnotes are printed at the end of the next section that doesn''t suppress endnotes. Suppressed endnotes are printed before the endnotes in that section in C++.'
type: docs
weight: 43000
url: /cpp/aspose.words/pagesetup/get_suppressendnotes/
---
## PageSetup::get_SuppressEndnotes method


True if endnotes are printed at the end of the next section that doesn't suppress endnotes. Suppressed endnotes are printed before the endnotes in that section.

```cpp
bool Aspose::Words::PageSetup::get_SuppressEndnotes()
```


## Examples



Shows how to store endnotes at the end of each section, and modify their positions. 
```cpp
void SuppressEndnotes()
{
    auto doc = MakeObject<Document>();
    doc->RemoveAllChildren();

    // By default, a document compiles all endnotes at its end.
    ASSERT_EQ(EndnotePosition::EndOfDocument, doc->get_EndnoteOptions()->get_Position());

    // We use the "Position" property of the document's "EndnoteOptions" object
    // to collect endnotes at the end of each section instead.
    doc->get_EndnoteOptions()->set_Position(EndnotePosition::EndOfSection);

    InsertSectionWithEndnote(doc, u"Section 1", u"Endnote 1, will stay in section 1");
    InsertSectionWithEndnote(doc, u"Section 2", u"Endnote 2, will be pushed down to section 3");
    InsertSectionWithEndnote(doc, u"Section 3", u"Endnote 3, will stay in section 3");

    // While getting sections to display their respective endnotes, we can set the "SuppressEndnotes" flag
    // of a section's "PageSetup" object to "true" to revert to the default behavior and pass its endnotes
    // onto the next section.
    SharedPtr<PageSetup> pageSetup = doc->get_Sections()->idx_get(1)->get_PageSetup();
    pageSetup->set_SuppressEndnotes(true);

    doc->Save(ArtifactsDir + u"PageSetup.SuppressEndnotes.docx");
}

static void InsertSectionWithEndnote(SharedPtr<Document> doc, String sectionBodyText, String endnoteText)
{
    auto section = MakeObject<Section>(doc);

    doc->AppendChild(section);

    auto body = MakeObject<Body>(doc);
    section->AppendChild(body);

    ASPOSE_ASSERT_EQ(section, body->get_ParentNode());

    auto para = MakeObject<Paragraph>(doc);
    body->AppendChild(para);

    ASPOSE_ASSERT_EQ(body, para->get_ParentNode());

    auto builder = MakeObject<DocumentBuilder>(doc);
    builder->MoveTo(para);
    builder->Write(sectionBodyText);
    builder->InsertFootnote(FootnoteType::Endnote, endnoteText);
}
```

## See Also

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
