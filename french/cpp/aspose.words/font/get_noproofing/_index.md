---
title: "Aspose::Words::Font::get_NoProofing méthode"
linktitle: "get_NoProofing"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Font::get_NoProofing méthode. Vrai lorsque les caractères formatés ne doivent pas être vérifiés orthographiquement en C++."
type: docs
weight: 30000
url: /fr/cpp/aspose.words/font/get_noproofing/
---
## Font::get_NoProofing method


Vrai lorsque les caractères formatés ne doivent pas être vérifiés orthographiquement.

```cpp
bool Aspose::Words::Font::get_NoProofing()
```


## Exemples



Montre comment empêcher le texte d'être vérifié orthographiquement par Microsoft Word.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Normalement, Microsoft Word souligne les fautes d'orthographe d'un trait rouge dentelé.
// Nous pouvons désactiver le drapeau "NoProofing" pour créer une portion de texte qui
// contourne le correcteur orthographique tout en le désactivant complètement.
builder->get_Font()->set_NoProofing(true);

builder->Writeln(u"Proofing has been disabled, so these spelking errrs will not display red lines underneath.");

doc->Save(get_ArtifactsDir() + u"Font.NoProofing.docx");
```

## Voir aussi

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
