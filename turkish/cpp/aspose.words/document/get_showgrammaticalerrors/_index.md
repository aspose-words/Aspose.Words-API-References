---
title: "Aspose::Words::Document::get_ShowGrammaticalErrors yöntemi"
linktitle: "get_ShowGrammaticalErrors"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Document::get_ShowGrammaticalErrors yöntemi. C++'ta bu belgede dilbilgisi hatalarının gösterilip gösterilmeyeceğini belirtir."
type: docs
weight: 50000
url: /tr/cpp/aspose.words/document/get_showgrammaticalerrors/
---
## Document::get_ShowGrammaticalErrors method


Bu belgede dilbilgisi hatalarının gösterilip gösterilmeyeceğini belirtir.

```cpp
bool Aspose::Words::Document::get_ShowGrammaticalErrors()
```


## Örnekler



Belgedeki hataların nasıl gösterileceğini/gizleneceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Hataları yakalayacak iki cümle ekleyin
// Microsoft Word'ün yazım ve dilbilgisi denetleyicileri tarafından.
builder->Writeln(u"There is a speling error in this sentence.");
builder->Writeln(u"Their is a grammatical error in this sentence.");

// Bu seçenekler etkinleştirilirse, yazım hataları altı çizili olur
// çıktı belgesinde kırmızı dalgalı bir çizgiyle, ve çift mavi bir çizgiyle dilbilgisi hataları vurgulanır.
doc->set_ShowGrammaticalErrors(showErrors);
doc->set_ShowSpellingErrors(showErrors);

doc->Save(get_ArtifactsDir() + u"Document.SpellingAndGrammarErrors.docx");
```

## Ayrıca Bakınız

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
