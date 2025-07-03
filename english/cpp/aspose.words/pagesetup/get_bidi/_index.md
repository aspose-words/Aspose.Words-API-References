---
title: Aspose::Words::PageSetup::get_Bidi method
linktitle: get_Bidi
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::PageSetup::get_Bidi method. Specifies that this section contains bidirectional (complex scripts) text in C++.'
type: docs
weight: 3000
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
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();
pageSetup->get_TextColumns()->SetCount(3);

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Write(u"Column 1.");
builder->InsertBreak(Aspose::Words::BreakType::ColumnBreak);
builder->Write(u"Column 2.");
builder->InsertBreak(Aspose::Words::BreakType::ColumnBreak);
builder->Write(u"Column 3.");

// Set the "Bidi" property to "true" to arrange the columns starting from the page's right side.
// The order of the columns will match the direction of the right-to-left text.
// Set the "Bidi" property to "false" to arrange the columns starting from the page's left side.
// The order of the columns will match the direction of the left-to-right text.
pageSetup->set_Bidi(reverseColumns);

doc->Save(get_ArtifactsDir() + u"PageSetup.Bidi.docx");
```

## See Also

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
