---
title: "Méthode Aspose::Words::Settings::HyphenationOptions::get_AutoHyphenation"
linktitle: "get_AutoHyphenation"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Settings::HyphenationOptions::get_AutoHyphenation. Obtient ou définit la valeur déterminant si l'hyphénation automatique est activée pour le document. La valeur par défaut de cette propriété est false en C++."
type: docs
weight: 3000
url: /fr/cpp/aspose.words.settings/hyphenationoptions/get_autohyphenation/
---
## HyphenationOptions::get_AutoHyphenation method


Obtient ou définit la valeur déterminant si la césure automatique est activée pour le document. La valeur par défaut pour cette propriété est **false**.

```cpp
bool Aspose::Words::Settings::HyphenationOptions::get_AutoHyphenation() const
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
