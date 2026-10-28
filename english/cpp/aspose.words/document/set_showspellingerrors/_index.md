---
title: Aspose::Words::Document::set_ShowSpellingErrors method
linktitle: set_ShowSpellingErrors
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Document::set_ShowSpellingErrors method. Specifies whether to display spelling errors in this document in C++.'
type: docs
weight: 170000
url: /cpp/aspose.words/document/set_showspellingerrors/
---
## Document::set_ShowSpellingErrors method


Specifies whether to display spelling errors in this document.

```cpp
void Aspose::Words::Document::set_ShowSpellingErrors(bool value)
```

## Examples


Shows how to show/hide errors in the document.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insert two sentences with mistakes that would be picked up
// by the spelling and grammar checkers in Microsoft Word.
builder->Writeln(u"There is a speling error in this sentence.");
builder->Writeln(u"Their is a grammatical error in this sentence.");

// If these options are enabled, then spelling errors will be underlined
// in the output document by a jagged red line, and a double blue line will highlight grammatical mistakes.
doc->set_ShowGrammaticalErrors(showErrors);
doc->set_ShowSpellingErrors(showErrors);

doc->Save(get_ArtifactsDir() + u"Document.SpellingAndGrammarErrors.docx");
```
## See Also

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
