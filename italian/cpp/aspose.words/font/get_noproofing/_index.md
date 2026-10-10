---
title: "Metodo Aspose::Words::Font::get_NoProofing"
linktitle: "get_NoProofing"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Font::get_NoProofing. Vero quando i caratteri formattati non devono essere controllati ortograficamente in C++."
type: docs
weight: 30000
url: /it/cpp/aspose.words/font/get_noproofing/
---
## Font::get_NoProofing method


True quando i caratteri formattati non devono essere controllati ortograficamente.

```cpp
bool Aspose::Words::Font::get_NoProofing()
```


## Esempi



Mostra come impedire che il testo venga controllato ortograficamente da Microsoft Word.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Normalmente, Microsoft Word evidenzia gli errori di ortografia con una sottolineatura rossa irregolare.
// Possiamo annullare l'impostazione del flag "NoProofing" per creare una porzione di testo che
// aggira il correttore ortografico disattivandolo completamente.
builder->get_Font()->set_NoProofing(true);

builder->Writeln(u"Proofing has been disabled, so these spelking errrs will not display red lines underneath.");

doc->Save(get_ArtifactsDir() + u"Font.NoProofing.docx");
```

## Vedi anche

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
