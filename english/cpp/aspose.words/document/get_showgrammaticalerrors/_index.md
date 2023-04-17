---
title: Aspose::Words::Document::get_ShowGrammaticalErrors method
linktitle: get_ShowGrammaticalErrors
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Document::get_ShowGrammaticalErrors method. Specifies whether to display grammar errors in this document in C++.'
type: docs
weight: 50000
url: /cpp/aspose.words/document/get_showgrammaticalerrors/
---
## Document::get_ShowGrammaticalErrors method


Specifies whether to display grammar errors in this document.

```cpp
bool Aspose::Words::Document::get_ShowGrammaticalErrors()
```


## Examples



Shows how to show/hide errors in the document. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Insert two sentences with mistakes that would be picked up
// by the spelling and grammar checkers in Microsoft Word.
builder->Writeln(u"There is a speling error in this sentence.");
builder->Writeln(u"Their is a grammatical error in this sentence.");

// If these options are enabled, then spelling errors will be underlined
// in the output document by a jagged red line, and a double blue line will highlight grammatical mistakes.
doc->set_ShowGrammaticalErrors(showErrors);
doc->set_ShowSpellingErrors(showErrors);

doc->Save(ArtifactsDir + u"Document.SpellingAndGrammarErrors.docx");
```

## See Also

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
