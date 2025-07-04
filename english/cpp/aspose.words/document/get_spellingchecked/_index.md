---
title: Aspose::Words::Document::get_SpellingChecked method
linktitle: get_SpellingChecked
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Document::get_SpellingChecked method. Returns true if the document has been checked for spelling in C++.'
type: docs
weight: 52000
url: /cpp/aspose.words/document/get_spellingchecked/
---
## Document::get_SpellingChecked method


Returns **true** if the document has been checked for spelling.

```cpp
bool Aspose::Words::Document::get_SpellingChecked()
```


## Examples



Shows how to set spelling or grammar verifying. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// The string with spelling errors.
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->Add(System::MakeObject<Aspose::Words::Run>(doc, u"The speeling in this documentz is all broked."));

// Spelling/Grammar check start if we set properties to false.
// We can see all errors in Microsoft Word via Review -> Spelling & Grammar.
// Note that Microsoft Word does not start grammar/spell check automatically for DOC and RTF document format.
doc->set_SpellingChecked(checkSpellingGrammar);
doc->set_GrammarChecked(checkSpellingGrammar);

doc->Save(get_ArtifactsDir() + u"Document.SpellingOrGrammar.docx");
```

## See Also

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
