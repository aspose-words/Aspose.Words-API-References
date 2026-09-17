---
title: "Méthode Aspose::Words::Settings::HyphenationOptions::get_HyphenateCaps"
linktitle: "get_HyphenateCaps"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Settings::HyphenationOptions::get_HyphenateCaps. Obtient ou définit la valeur déterminant si les mots écrits en majuscules sont hyphénés. La valeur par défaut de cette propriété est true en C++."
type: docs
weight: 5000
url: /fr/cpp/aspose.words.settings/hyphenationoptions/get_hyphenatecaps/
---
## HyphenationOptions::get_HyphenateCaps method


Obtient ou définit la valeur déterminant si les mots écrits en majuscules sont hyphénés. La valeur par défaut de cette propriété est **true**.

```cpp
bool Aspose::Words::Settings::HyphenationOptions::get_HyphenateCaps() const
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
