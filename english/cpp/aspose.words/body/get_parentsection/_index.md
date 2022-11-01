---
title: get_ParentSection
second_title: Aspose.Words for C++ API Reference
description: Gets the parent section of this story.
type: docs
weight: 53
url: /cpp/aspose.words/body/get_parentsection/
---
## Body.get_ParentSection method


Gets the parent section of this story.

```cpp
System::SharedPtr<Aspose::Words::Section> Aspose::Words::Body::get_ParentSection()
```


**ParentSection** is equivalent to **%([Section](../../section/))ParentNode**.

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

