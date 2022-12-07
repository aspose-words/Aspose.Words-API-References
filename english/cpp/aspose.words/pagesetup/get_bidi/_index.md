---
title: get_Bidi
second_title: Aspose.Words for C++ API Reference
description: Specifies that this section contains bidirectional (complex scripts) text.
type: docs
weight: 27
url: /cpp/aspose.words/pagesetup/get_bidi/
---
## PageSetup::get_Bidi method


Specifies that this section contains bidirectional (complex scripts) text.

```cpp
bool Aspose::Words::PageSetup::get_Bidi()
```

## Remarks


When **true**, the columns in this section are laid out from right to left.

## Examples



Shows how to set the order of text columns in a section. 
```cpp
auto doc = MakeObject<Document>();

SharedPtr<PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();
pageSetup->get_TextColumns()->SetCount(3);

auto builder = MakeObject<DocumentBuilder>(doc);
builder->Write(u"Column 1.");
builder->InsertBreak(BreakType::ColumnBreak);
builder->Write(u"Column 2.");
builder->InsertBreak(BreakType::ColumnBreak);
builder->Write(u"Column 3.");

// Set the "Bidi" property to "true" to arrange the columns starting from the page's right side.
// The order of the columns will match the direction of the right-to-left text.
// Set the "Bidi" property to "false" to arrange the columns starting from the page's left side.
// The order of the columns will match the direction of the left-to-right text.
pageSetup->set_Bidi(reverseColumns);

doc->Save(ArtifactsDir + u"PageSetup.Bidi.docx");
```

## See Also

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
