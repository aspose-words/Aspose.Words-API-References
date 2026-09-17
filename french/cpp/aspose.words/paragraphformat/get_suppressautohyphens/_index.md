---
title: "Aspose::Words::ParagraphFormat::get_SuppressAutoHyphens méthode"
linktitle: "get_SuppressAutoHyphens"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::ParagraphFormat::get_SuppressAutoHyphens méthode. Spécifie si le paragraphe actuel doit être exempté de toute césure appliquée dans les paramètres du document en C++."
type: docs
weight: 38000
url: /fr/cpp/aspose.words/paragraphformat/get_suppressautohyphens/
---
## ParagraphFormat::get_SuppressAutoHyphens method


Spécifie si le paragraphe actuel doit être exempté de toute césure appliquée dans les paramètres du document.

```cpp
bool Aspose::Words::ParagraphFormat::get_SuppressAutoHyphens()
```


## Exemples



Montre comment supprimer la césure pour un paragraphe.
```cpp
Aspose::Words::Hyphenation::RegisterDictionary(u"de-CH", get_MyDir() + u"hyph_de_CH.dic");

ASSERT_TRUE(Aspose::Words::Hyphenation::IsDictionaryRegistered(u"de-CH"));

// Ouvrez un document contenant du texte dont la locale correspond à celle de notre dictionnaire.
// Lorsque nous enregistrons ce document dans un format de sauvegarde à page fixe, son texte comportera des césures.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"German text.docx");

// Nous pouvons définir la propriété "SuppressAutoHyphens" sur "true" pour désactiver la césure
// pour un paragraphe spécifique tout en la maintenant activée pour le reste du document.
// La valeur par défaut de cette propriété est "false",
// ce qui signifie que chaque paragraphe utilise la césure par défaut si elle est disponible.
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->set_SuppressAutoHyphens(suppressAutoHyphens);

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.SuppressHyphens.pdf");
```

## Voir aussi

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
