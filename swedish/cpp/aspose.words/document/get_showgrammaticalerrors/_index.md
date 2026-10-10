---
title: "Aspose::Words::Document::get_ShowGrammaticalErrors metod"
linktitle: "get_ShowGrammaticalErrors"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Document::get_ShowGrammaticalErrors metod. Anger om grammatikfel ska visas i detta dokument i C++."
type: docs
weight: 50000
url: /sv/cpp/aspose.words/document/get_showgrammaticalerrors/
---
## Document::get_ShowGrammaticalErrors method


Anger om grammatikfel ska visas i detta dokument.

```cpp
bool Aspose::Words::Document::get_ShowGrammaticalErrors()
```


## Exempel



Visar hur man visar/döljer fel i dokumentet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Infoga två meningar med fel som skulle upptäckas
// av stavnings- och grammatikkontrollerna i Microsoft Word.
builder->Writeln(u"There is a speling error in this sentence.");
builder->Writeln(u"Their is a grammatical error in this sentence.");

// Om dessa alternativ är aktiverade kommer stavfel att understrykas
// i utdokumentet med en ojämn röd linje, och en dubbel blå linje kommer att markera grammatiska fel.
doc->set_ShowGrammaticalErrors(showErrors);
doc->set_ShowSpellingErrors(showErrors);

doc->Save(get_ArtifactsDir() + u"Document.SpellingAndGrammarErrors.docx");
```

## Se även

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
