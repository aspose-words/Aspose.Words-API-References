---
title: "Aspose::Words::Style::get_Priority méthode"
linktitle: "get_Priority"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Style::get_Priority méthode. Obtient/definit la valeur entière qui représente la priorité pour trier les styles dans le volet des tâches Styles en C++."
type: docs
weight: 16334
url: /fr/cpp/aspose.words/style/get_priority/
---
## Style::get_Priority method


Obtient/definit la valeur entière qui représente la priorité de tri des styles dans le volet des tâches Styles.

```cpp
int32_t Aspose::Words::Style::get_Priority() const
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
