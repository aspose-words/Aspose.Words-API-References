---
title: Aspose::Words::ParagraphFormat::set_SuppressAutoHyphens method
linktitle: set_SuppressAutoHyphens
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::ParagraphFormat::set_SuppressAutoHyphens method. Specifies whether the current paragraph should be exempted from any hyphenation which is applied in the document settings in C++.'
type: docs
weight: 76000
url: /cpp/aspose.words/paragraphformat/set_suppressautohyphens/
---
## ParagraphFormat::set_SuppressAutoHyphens method


Specifies whether the current paragraph should be exempted from any hyphenation which is applied in the document settings.

```cpp
void Aspose::Words::ParagraphFormat::set_SuppressAutoHyphens(bool value)
```

## Examples


Shows how to suppress hyphenation for a paragraph.

```cpp
Hyphenation::RegisterDictionary(u"de-CH", get_MyDir() + u"hyph_de_CH.dic");

ASSERT_TRUE(Hyphenation::IsDictionaryRegistered(u"de-CH"));

// Open a document containing text with a locale matching that of our dictionary.
// When we save this document to a fixed page save format, its text will have hyphenation.
auto doc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"German text.docx"));

// We can set the "SuppressAutoHyphens" property to "true" to disable hyphenation
// for a specific paragraph while keeping it enabled for the rest of the document.
// The default value for this property is "false",
// which means every paragraph by default uses hyphenation if any is available.
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->set_SuppressAutoHyphens(suppressAutoHyphens);

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.SuppressHyphens.pdf");
```
## See Also

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
