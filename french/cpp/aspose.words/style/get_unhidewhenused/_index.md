---
title: "Méthode Aspose::Words::Style::get_UnhideWhenUsed"
linktitle: "get_UnhideWhenUsed"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Style::get_UnhideWhenUsed. Obtient/definit si le style utilisé dans le document actuel est affiché dans la galerie des styles et dans le volet des tâches Styles. Vrai lorsque le style utilisé doit être affiché dans la galerie des styles en C++."
type: docs
weight: 19500
url: /fr/cpp/aspose.words/style/get_unhidewhenused/
---
## Style::get_UnhideWhenUsed method


Obtient/definit si le style utilisé dans le document actuel se dévoile dans la galerie des Styles et dans le volet des Styles. Vrai lorsque le style utilisé doit être affiché dans la galerie des Styles.

```cpp
bool Aspose::Words::Style::get_UnhideWhenUsed() const
```


## Exemples



Montre comment prioriser et masquer un style.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Style> styleTitle = doc->get_Styles()->idx_get(Aspose::Words::StyleIdentifier::Subtitle);

if (styleTitle->get_Priority() == 9)
{
    styleTitle->set_Priority(10);
}

if (!styleTitle->get_UnhideWhenUsed())
{
    styleTitle->set_UnhideWhenUsed(true);
}

if (styleTitle->get_SemiHidden())
{
    styleTitle->set_SemiHidden(true);
}

doc->Save(get_ArtifactsDir() + u"Styles.StylePriority.docx");
```

## Voir aussi

* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
