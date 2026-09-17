---
title: "Méthode Aspose::Words::Loading::TxtLoadOptions::get_DocumentDirection"
linktitle: "get_DocumentDirection"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Loading::TxtLoadOptions::get_DocumentDirection. Obtient ou définit la direction du document. La valeur par défaut est LeftToRight en C++."
type: docs
weight: 5000
url: /fr/cpp/aspose.words.loading/txtloadoptions/get_documentdirection/
---
## TxtLoadOptions::get_DocumentDirection method


Obtient ou définit la direction du document. La valeur par défaut est [LeftToRight](../../documentdirection/).

```cpp
Aspose::Words::Loading::DocumentDirection Aspose::Words::Loading::TxtLoadOptions::get_DocumentDirection() const
```


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

* Enum [DocumentDirection](../../documentdirection/)
* Class [TxtLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
