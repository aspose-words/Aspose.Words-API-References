---
title: Aspose::Words::ParagraphFormat::get_SuppressAutoHyphens method
linktitle: get_SuppressAutoHyphens
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::ParagraphFormat::get_SuppressAutoHyphens method. Specifies whether the current paragraph should be exempted from any hyphenation which is applied in the document settings in C++.'
type: docs
weight: 38000
url: /cpp/aspose.words/paragraphformat/get_suppressautohyphens/
---
## ParagraphFormat::get_SuppressAutoHyphens method


Specifies whether the current paragraph should be exempted from any hyphenation which is applied in the document settings.

```cpp
bool Aspose::Words::ParagraphFormat::get_SuppressAutoHyphens()
```


## Examples



Shows how to suppress hyphenation for a paragraph. 
```cpp
Aspose::Words::Hyphenation::RegisterDictionary(u"de-CH", get_MyDir() + u"hyph_de_CH.dic");

ASSERT_TRUE(Aspose::Words::Hyphenation::IsDictionaryRegistered(u"de-CH"));

// Open a document containing text with a locale matching that of our dictionary.
// When we save this document to a fixed page save format, its text will have hyphenation.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"German text.docx");

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
