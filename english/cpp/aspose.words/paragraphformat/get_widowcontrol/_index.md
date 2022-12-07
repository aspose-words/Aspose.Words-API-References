---
title: get_WidowControl
second_title: Aspose.Words for C++ API Reference
description: True if the first and last lines in the paragraph are to remain on the same page as the rest of the paragraph.
type: docs
weight: 521
url: /cpp/aspose.words/paragraphformat/get_widowcontrol/
---
## ParagraphFormat::get_WidowControl method


True if the first and last lines in the paragraph are to remain on the same page as the rest of the paragraph.

```cpp
bool Aspose::Words::ParagraphFormat::get_WidowControl()
```


## Examples



Shows how to enable widow/orphan control for a paragraph. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// When we write the text that does not fit onto one page, one line may spill over onto the next page.
// The single line that ends up on the next page is called an "Orphan",
// and the previous line where the orphan broke off is called a "Widow".
// We can fix orphans and widows by rearranging text via font size, spacing, or page margins.
// If we wish to preserve our document's dimensions, we can set this flag to "true"
// to push widows onto the same page as their respective orphans.
// Leave this flag as "false" will leave widow/orphan pairs in text.
// Every paragraph has this setting accessible in Microsoft Word via Home -> Paragraph -> Paragraph Settings
// (button on bottom right hand corner of "Paragraph" tab) -> "Widow/Orphan control".
builder->get_ParagraphFormat()->set_WidowControl(widowControl);

// Insert text that produces an orphan and a widow.
builder->get_Font()->set_Size(68);
builder->Write(String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, ") +
               u"sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc->Save(ArtifactsDir + u"ParagraphFormat.WidowControl.docx");
```

## See Also

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
