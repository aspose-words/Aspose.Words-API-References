---
title: get_SuppressAutoHyphens
second_title: Aspose.Words for C++ API Reference
description: Specifies whether the current paragraph should be exempted from any hyphenation which is applied in the document settings.
type: docs
weight: 469
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
Hyphenation::RegisterDictionary(u"de-CH", MyDir + u"hyph_de_CH.dic");

ASSERT_TRUE(Hyphenation::IsDictionaryRegistered(u"de-CH"));

// Open a document containing text with a locale matching that of our dictionary.
// When we save this document to a fixed page save format, its text will have hyphenation.
auto doc = MakeObject<Document>(MyDir + u"German text.docx");

// We can set the "SuppressAutoHyphens" property to "true" to disable hyphenation
// for a specific paragraph while keeping it enabled for the rest of the document.
// The default value for this property is "false",
// which means every paragraph by default uses hyphenation if any is available.
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->set_SuppressAutoHyphens(suppressAutoHyphens);

doc->Save(ArtifactsDir + u"ParagraphFormat.SuppressHyphens.pdf");
```

## See Also

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
