---
title: "Метод Aspose::Words::Document::get_SpellingChecked"
linktitle: "get_SpellingChecked"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Document::get_SpellingChecked. Возвращает true, если документ был проверен на орфографию в C++."
type: docs
weight: 52000
url: /ru/cpp/aspose.words/document/get_spellingchecked/
---
## Document::get_SpellingChecked method


Возвращает **true**, если документ был проверен на орфографию.

```cpp
bool Aspose::Words::Document::get_SpellingChecked()
```


## Примеры



Показывает, как установить проверку орфографии или грамматики.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Строка с орфографическими ошибками.
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->Add(System::MakeObject<Aspose::Words::Run>(doc, u"The speeling in this documentz is all broked."));

// Проверка орфографии/грамматики начинается, если мы установим свойства в false.
// Мы можем увидеть все ошибки в Microsoft Word через Review -> Spelling & Grammar.
// Обратите внимание, что Microsoft Word не запускает проверку грамматики/орфографии автоматически для форматов документов DOC и RTF.
doc->set_SpellingChecked(checkSpellingGrammar);
doc->set_GrammarChecked(checkSpellingGrammar);

doc->Save(get_ArtifactsDir() + u"Document.SpellingOrGrammar.docx");
```

## См. также

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
