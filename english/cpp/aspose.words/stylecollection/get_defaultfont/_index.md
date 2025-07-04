---
title: Aspose::Words::StyleCollection::get_DefaultFont method
linktitle: get_DefaultFont
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::StyleCollection::get_DefaultFont method. Gets document default text formatting in C++.'
type: docs
weight: 6000
url: /cpp/aspose.words/stylecollection/get_defaultfont/
---
## StyleCollection::get_DefaultFont method


Gets document default text formatting.

```cpp
System::SharedPtr<Aspose::Words::Font> Aspose::Words::StyleCollection::get_DefaultFont()
```

## Remarks


Note that document-wide defaults were introduced in Microsoft Word 2007 and are fully supported in OOXML formats ([Docx](../../loadformat/)) only. Earlier document formats have limited support for this feature and only font names can be stored.

## Examples



Shows how to add a [Style](../../style/) to a document's styles collection. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::StyleCollection> styles = doc->get_Styles();
// Set default parameters for new styles that we may later add to this collection.
styles->get_DefaultFont()->set_Name(u"Courier New");
// If we add a style of the "StyleType.Paragraph", the collection will apply the values of
// its "DefaultParagraphFormat" property to the style's "ParagraphFormat" property.
styles->get_DefaultParagraphFormat()->set_FirstLineIndent(15.0);
// Add a style, and then verify that it has the default settings.
styles->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle");

ASSERT_EQ(u"Courier New", styles->idx_get(4)->get_Font()->get_Name());
ASPOSE_ASSERT_EQ(15.0, styles->idx_get(u"MyStyle")->get_ParagraphFormat()->get_FirstLineIndent());
```

## See Also

* Class [Font](../../font/)
* Class [StyleCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
