---
title: "Méthode Aspose::Words::Settings::HyphenationOptions::get_HyphenationZone"
linktitle: "get_HyphenationZone"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Settings::HyphenationOptions::get_HyphenationZone. Obtient ou définit la distance en 1/20 de point depuis la marge droite dans laquelle vous ne souhaitez pas hyphéner les mots. La valeur par défaut de cette propriété est 360 (0,25 pouce) en C++."
type: docs
weight: 6000
url: /fr/cpp/aspose.words.settings/hyphenationoptions/get_hyphenationzone/
---
## HyphenationOptions::get_HyphenationZone method


Obtient ou définit la distance, en 1/20 de point, depuis la marge droite dans laquelle vous ne souhaitez pas hyphéner les mots. La valeur par défaut de cette propriété est 360 (0,25 pouce).

```cpp
int32_t Aspose::Words::Settings::HyphenationOptions::get_HyphenationZone() const
```


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
