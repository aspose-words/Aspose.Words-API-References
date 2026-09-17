---
title: "Méthode Aspose::Words::Fields::FormField::get_TextInputDefault"
linktitle: "get_TextInputDefault"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Fields::FormField::get_TextInputDefault. Obtient ou définit la chaîne par défaut ou une expression de calcul d'un champ de formulaire texte en C++."
type: docs
weight: 21000
url: /fr/cpp/aspose.words.fields/formfield/get_textinputdefault/
---
## FormField::get_TextInputDefault method


Obtient ou définit la chaîne par défaut ou une expression de calcul d'un champ de formulaire texte.

```cpp
System::String Aspose::Words::Fields::FormField::get_TextInputDefault()
```

## Remarques


La signification de cette propriété dépend de la valeur de la propriété [TextInputType](../get_textinputtype/).

Lorsque [TextInputType](../get_textinputtype/) est [Regular](../../textformfieldtype/) ou [Number](../../textformfieldtype/), cette chaîne spécifie la chaîne par défaut pour le champ de formulaire texte. Cette chaîne est le contenu que Microsoft Word affichera dans le document lorsque le champ de formulaire est vide.

Lorsque [TextInputType](../get_textinputtype/) est [Calculated](../../textformfieldtype/), cette chaîne contient l'expression à calculer. L'expression doit être une formule valide selon les exigences du champ de formule de Microsoft Word. Lorsque vous définissez une nouvelle expression à l'aide de cette propriété, Aspose.Words calcule automatiquement le résultat de la formule et l'insère dans le champ de formulaire.

Microsoft Word autorise des chaînes d'au plus 255 caractères.
## Voir aussi

* Class [FormField](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
