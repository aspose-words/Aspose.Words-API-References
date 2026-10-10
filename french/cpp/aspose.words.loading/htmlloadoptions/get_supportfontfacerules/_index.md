---
title: "Aspose::Words::Loading::HtmlLoadOptions::get_SupportFontFaceRules méthode"
linktitle: "get_SupportFontFaceRules"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Loading::HtmlLoadOptions::get_SupportFontFaceRules méthode. Obtient ou définit une valeur indiquant s'il faut prendre en charge les règles @font-face et charger les polices déclarées. La valeur par défaut est false en C++."
type: docs
weight: 6500
url: /fr/cpp/aspose.words.loading/htmlloadoptions/get_supportfontfacerules/
---
## HtmlLoadOptions::get_SupportFontFaceRules method


Obtient ou définit une valeur indiquant s'il faut prendre en charge les règles @font-face et charger les polices déclarées. La valeur par défaut est **false**.

```cpp
bool Aspose::Words::Loading::HtmlLoadOptions::get_SupportFontFaceRules() const
```

## Remarques


Si cette option est activée, les polices déclarées dans les règles @font-face sont chargées et intégrées aux définitions de polices du document résultant (voir [FontInfos](../../../aspose.words/documentbase/get_fontinfos/)). Cela rend les polices chargées disponibles pour le rendu mais n'active pas automatiquement l'intégration des polices lors de l'enregistrement. Pour enregistrer le document avec les polices chargées, la propriété [EmbedTrueTypeFonts](../../../aspose.words.fonts/fontinfocollection/get_embedtruetypefonts/) de la collection [FontInfos](../../../aspose.words/documentbase/get_fontinfos/) doit être définie sur **true**.

Les formats de police pris en charge sont TTF, EOT et WOFF.

Les règles @font-face ne sont pas prises en charge lors du chargement d'images SVG.

## Exemples



Montre comment charger les règles "@font-face" déclarées.
```cpp
auto loadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>();
loadOptions->set_SupportFontFaceRules(true);
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Html with FontFace.html", loadOptions);

ASSERT_EQ(u"Squarish Sans CT Regular", doc->get_FontInfos()->idx_get(0)->get_Name());
```

## Voir aussi

* Class [HtmlLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
