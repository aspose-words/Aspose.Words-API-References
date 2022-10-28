---
title: get_Pages
second_title: Aspose.Words for C++ API Reference
description: Represents an estimate of the number of pages in the document.
type: docs
weight: 261
url: /cpp/aspose.words.properties/builtindocumentproperties/get_pages/
---
## BuiltInDocumentProperties.get_Pages method


Represents an estimate of the number of pages in the document.

```cpp
int32_t Aspose::Words::Properties::BuiltInDocumentProperties::get_Pages()
```


Aspose.Words updates this property when you call [UpdatePageLayout](../../../aspose.words/document/updatepagelayout/).

## Examples




Shows how to work with document properties in the "Content" category. 
```cpp
void Content()
{
    auto doc = MakeObject<Document>(MyDir + u"Paragraphs.docx");
    SharedPtr<BuiltInDocumentProperties> properties = doc->get_BuiltInDocumentProperties();

    // By using built in properties,
    // we can treat document statistics such as word/page/character counts as metadata that can be glanced at without opening the document
    // These properties are accessed by right clicking the file in Windows Explorer and navigating to Properties > Details > Content
    // If we want to display this data inside the document, we can use fields such as NUMPAGES, NUMWORDS, NUMCHARS etc.
    // Also, these values can also be viewed in Microsoft Word by navigating File > Properties > Advanced Properties > Statistics
    // Page count: The PageCount property shows the page count in real time and its value can be assigned to the Pages property

    // The "Pages" property stores the page count of the document.
    ASSERT_EQ(6, properties->get_Pages());

    // The "Words", "Characters", and "CharactersWithSpaces" built-in properties also display various document statistics,
    // but we need to call the "UpdateWordCount" method on the whole document before we can expect them to contain accurate values.
    doc->UpdateWordCount();

    ASSERT_EQ(1035, properties->get_Words());
    ASSERT_EQ(6026, properties->get_Characters());
    ASSERT_EQ(7041, properties->get_CharactersWithSpaces());

    // Count the number of lines in the document, and then assign the result to the "Lines" built-in property.
    auto lineCounter = MakeObject<ExDocumentProperties::LineCounter>(doc);
    properties->set_Lines(lineCounter->GetLineCount());

    ASSERT_EQ(142, properties->get_Lines());

    // Assign the number of Paragraph nodes in the document to the "Paragraphs" built-in property.
    properties->set_Paragraphs(doc->GetChildNodes(NodeType::Paragraph, true)->get_Count());
    ASSERT_EQ(29, properties->get_Paragraphs());

    // Get an estimate of the file size of our document via the "Bytes" built-in property.
    ASSERT_EQ(20310, properties->get_Bytes());

    // Set a different template for our document, and then update the "Template" built-in property manually to reflect this change.
    doc->set_AttachedTemplate(MyDir + u"Business brochure.dotx");

    ASSERT_EQ(u"Normal", properties->get_Template());

    properties->set_Template(doc->get_AttachedTemplate());

    // "ContentStatus" is a descriptive built-in property.
    properties->set_ContentStatus(u"Draft");

    // Upon saving, the "ContentType" built-in property will contain the MIME type of the output save format.
    ASSERT_EQ(String::Empty, properties->get_ContentType());

    // If the document contains links, and they are all up to date, we can set the "LinksUpToDate" property to "true".
    ASSERT_FALSE(properties->get_LinksUpToDate());

    doc->Save(ArtifactsDir + u"DocumentProperties.Content.docx");
}

class LineCounter : public System::Object
{
public:
    LineCounter(SharedPtr<Document> doc) : mLineCount(0), mScanningLineForRealText(false)
    {
        mLayoutEnumerator = MakeObject<LayoutEnumerator>(doc);

        CountLines();
    }

    int GetLineCount()
    {
        return mLineCount;
    }

private:
    SharedPtr<LayoutEnumerator> mLayoutEnumerator;
    int mLineCount;
    bool mScanningLineForRealText;

    void CountLines()
    {
        do
        {
            if (mLayoutEnumerator->get_Type() == LayoutEntityType::Line)
            {
                mScanningLineForRealText = true;
            }

            if (mLayoutEnumerator->MoveFirstChild())
            {
                if (mScanningLineForRealText && mLayoutEnumerator->get_Kind().StartsWith(u"TEXT"))
                {
                    mLineCount++;
                    mScanningLineForRealText = false;
                }
                CountLines();
                mLayoutEnumerator->MoveParent();
            }
        } while (mLayoutEnumerator->MoveNext());
    }
};
```

