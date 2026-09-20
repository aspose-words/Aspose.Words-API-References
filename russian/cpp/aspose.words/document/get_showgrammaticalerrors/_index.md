---
title: "Aspose::Words::Document::get_ShowGrammaticalErrors метод"
linktitle: "get_ShowGrammaticalErrors"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Document::get_ShowGrammaticalErrors. Указывает, следует ли отображать грамматические ошибки в этом документе в C++."
type: docs
weight: 50000
url: /ru/cpp/aspose.words/document/get_showgrammaticalerrors/
---
## Document::get_ShowGrammaticalErrors method


Указывает, отображать ли грамматические ошибки в этом документе.

```cpp
bool Aspose::Words::Document::get_ShowGrammaticalErrors()
```


## Примеры



Показывает, как показывать/скрывать ошибки в документе.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Вставьте два предложения с ошибками, которые будут обнаружены
// проверяющими орфографию и грамматику в Microsoft Word.
builder->Writeln(u"There is a speling error in this sentence.");
builder->Writeln(u"Their is a grammatical error in this sentence.");

// Если эти параметры включены, орфографические ошибки будут подчеркнуты
// в выходном документе пунктирной красной линией, а двойная синяя линия будет выделять грамматические ошибки.
doc->set_ShowGrammaticalErrors(showErrors);
doc->set_ShowSpellingErrors(showErrors);

doc->Save(get_ArtifactsDir() + u"Document.SpellingAndGrammarErrors.docx");
```

## См. также

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
