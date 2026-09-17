---
title: "Aspose::Words::Loading::DocumentDirection enum"
linktitle: "DocumentDirection"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Loading::DocumentDirection enum. Permet de spécifier la direction du flux de texte dans un document en C++."
type: docs
weight: 13000
url: /fr/cpp/aspose.words.loading/documentdirection/
---
## DocumentDirection enum


Permet de spécifier la direction du flux du texte dans un document.

```cpp
enum class DocumentDirection
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| LeftToRight | 0 | Direction de gauche à droite. |
| RightToLeft | 1 | Direction de droite à gauche. |
| Auto | 2 | Détection automatique de la direction. |


## Exemples



Montre comment détecter la direction du texte d'un document texte brut.
```cpp
// Créez un objet "TxtLoadOptions", que nous pouvons passer au constructeur d'un document
// pour modifier la façon dont nous chargeons un document texte brut.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::TxtLoadOptions>();

// Définissez la propriété "DocumentDirection" sur "DocumentDirection.Auto" détecte automatiquement
// la direction de chaque paragraphe de texte que Aspose.Words charge à partir d'un texte brut.
// La propriété "Bidi" de chaque paragraphe stockera sa direction.
loadOptions->set_DocumentDirection(Aspose::Words::Loading::DocumentDirection::Auto);

// Détecter le texte hébreu comme de droite à gauche.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Hebrew text.txt", loadOptions);

ASSERT_TRUE(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Bidi());

// Détecter le texte anglais comme de droite à gauche.
doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"English text.txt", loadOptions);

ASSERT_FALSE(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Bidi());
```

## Voir aussi

* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
