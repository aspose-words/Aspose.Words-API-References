---
title: "Méthode Aspose::Words::Settings::HyphenationOptions::get_ConsecutiveHyphenLimit"
linktitle: "get_ConsecutiveHyphenLimit"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Settings::HyphenationOptions::get_ConsecutiveHyphenLimit. Obtient ou définit le nombre maximal de lignes consécutives pouvant se terminer par un trait d'union. La valeur par défaut de cette propriété est 0 en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words.settings/hyphenationoptions/get_consecutivehyphenlimit/
---
## HyphenationOptions::get_ConsecutiveHyphenLimit method


Obtient ou définit le nombre maximal de lignes consécutives pouvant se terminer par des traits d'union. La valeur par défaut de cette propriété est 0.

```cpp
int32_t Aspose::Words::Settings::HyphenationOptions::get_ConsecutiveHyphenLimit() const
```

## Remarques


Si la valeur de cette propriété est définie à 0, un nombre quelconque de lignes consécutives peut se terminer par des traits d'union.

La propriété n'a aucun effet lors de l'enregistrement aux formats de page fixe, par ex. PDF.

## Exemples



Montre comment configurer la césure automatique.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Size(24);
builder->Writeln(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, ") + u"sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc->get_HyphenationOptions()->set_AutoHyphenation(true);
doc->get_HyphenationOptions()->set_ConsecutiveHyphenLimit(2);
doc->get_HyphenationOptions()->set_HyphenationZone(720);
doc->get_HyphenationOptions()->set_HyphenateCaps(true);

doc->Save(get_ArtifactsDir() + u"Document.HyphenationOptions.docx");
```

## Voir aussi

* Class [HyphenationOptions](../)
* Namespace [Aspose::Words::Settings](../../)
* Library [Aspose.Words for C++](../../../)
