---
title: "Aspose::Words::Style::get_SemiHidden méthode"
linktitle: "get_SemiHidden"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Style::get_SemiHidden méthode. Obtient/definit si le style est masqué dans la galerie Styles et dans le volet des tâches Styles en C++."
type: docs
weight: 16667
url: /fr/cpp/aspose.words/style/get_semihidden/
---
## Style::get_SemiHidden method


Obtient/definit si le style est masqué dans la galerie des Styles et dans le volet des Styles.

```cpp
bool Aspose::Words::Style::get_SemiHidden() const
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
