---
title: Aspose::Words::Loading::TxtLoadOptions::set_DocumentDirection method
linktitle: set_DocumentDirection
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Loading::TxtLoadOptions::set_DocumentDirection method. Sets a document direction. The default value is LeftToRight in C++.'
type: docs
weight: 12000
url: /cpp/aspose.words.loading/txtloadoptions/set_documentdirection/
---
## TxtLoadOptions::set_DocumentDirection method


Sets a document direction. The default value is [LeftToRight](../../documentdirection/).

```cpp
void Aspose::Words::Loading::TxtLoadOptions::set_DocumentDirection(Aspose::Words::Loading::DocumentDirection value)
```

## Examples


Shows how to detect plaintext document text direction.

```cpp
// Create a "TxtLoadOptions" object, which we can pass to a document's constructor
// to modify how we load a plaintext document.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::TxtLoadOptions>();

// Set the "DocumentDirection" property to "DocumentDirection.Auto" automatically detects
// the direction of every paragraph of text that Aspose.Words loads from plaintext.
// Each paragraph's "Bidi" property will store its direction.
loadOptions->set_DocumentDirection(DocumentDirection::Auto);

// Detect Hebrew text as right-to-left.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Hebrew text.txt", loadOptions);

ASSERT_TRUE(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Bidi());

// Detect English text as right-to-left.
doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"English text.txt", loadOptions);

ASSERT_FALSE(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Bidi());
```
## See Also

* Class [TxtLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
