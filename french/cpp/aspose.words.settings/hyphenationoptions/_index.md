---
title: "Aspose::Words::Settings::HyphenationOptions class"
linktitle: "HyphenationOptions"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Settings::HyphenationOptions class. Permet de configurer les options de césure du document. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words.settings/hyphenationoptions/
---
## HyphenationOptions class


Permet de configurer les options de césure du document. Pour en savoir plus, consultez l'article de documentation [Working with Hyphenation](https://docs.aspose.com/words/cpp/working-with-hyphenation/).

```cpp
class HyphenationOptions : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_AutoHyphenation](./get_autohyphenation/)() const | Obtient ou définit la valeur déterminant si la césure automatique est activée pour le document. La valeur par défaut pour cette propriété est **false**. |
| [get_ConsecutiveHyphenLimit](./get_consecutivehyphenlimit/)() const | Obtient ou définit le nombre maximal de lignes consécutives pouvant se terminer par des traits d'union. La valeur par défaut de cette propriété est 0. |
| [get_HyphenateCaps](./get_hyphenatecaps/)() const | Obtient ou définit la valeur déterminant si les mots écrits en majuscules sont hyphénés. La valeur par défaut de cette propriété est **true**. |
| [get_HyphenationZone](./get_hyphenationzone/)() const | Obtient ou définit la distance, en 1/20 de point, depuis la marge droite dans laquelle vous ne souhaitez pas hyphéner les mots. La valeur par défaut de cette propriété est 360 (0,25 pouce). |
| [GetType](./gettype/)() const override |  |
| [HyphenationOptions](./hyphenationoptions/)() |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AutoHyphenation](./set_autohyphenation/)(bool) | Définisseur pour [Aspose::Words::Settings::HyphenationOptions::get_AutoHyphenation](./get_autohyphenation/). |
| [set_ConsecutiveHyphenLimit](./set_consecutivehyphenlimit/)(int32_t) | Définisseur pour [Aspose::Words::Settings::HyphenationOptions::get_ConsecutiveHyphenLimit](./get_consecutivehyphenlimit/). |
| [set_HyphenateCaps](./set_hyphenatecaps/)(bool) | Définisseur pour [Aspose::Words::Settings::HyphenationOptions::get_HyphenateCaps](./get_hyphenatecaps/). |
| [set_HyphenationZone](./set_hyphenationzone/)(int32_t) | Définisseur pour [Aspose::Words::Settings::HyphenationOptions::get_HyphenationZone](./get_hyphenationzone/). |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
