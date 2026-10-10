---
title: "Aspose::Words::Style::get_StyleIdentifier méthode"
linktitle: "get_StyleIdentifier"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Style::get_StyleIdentifier méthode. Obtient l'identifiant de style indépendant de la locale pour un style intégré en C++."
type: docs
weight: 17000
url: /fr/cpp/aspose.words/style/get_styleidentifier/
---
## Style::get_StyleIdentifier method


Obtient l'identifiant de style indépendant de la locale pour un style intégré.

```cpp
Aspose::Words::StyleIdentifier Aspose::Words::Style::get_StyleIdentifier() const
```

## Remarques


Pour les styles définis par l'utilisateur (personnalisés), cette propriété renvoie [User](../../styleidentifier/).

## Exemples



Montre comment modifier la position de l'arrêt de tabulation droit dans les paragraphes liés à la table des matières (TOC).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Table of contents.docx");

// Itérez à travers tous les paragraphes avec des styles basés sur les résultats de la TOC ; il s'agit de tout style entre TOC et TOC9.
for (auto&& para : System::IterateOver<Aspose::Words::Paragraph>(doc->GetChildNodes(Aspose::Words::NodeType::Paragraph, true)))
{
    if (para->get_ParagraphFormat()->get_Style()->get_StyleIdentifier() >= Aspose::Words::StyleIdentifier::Toc1 && para->get_ParagraphFormat()->get_Style()->get_StyleIdentifier() <= Aspose::Words::StyleIdentifier::Toc9)
    {
        // Obtenez la première tabulation utilisée dans ce paragraphe, elle devrait être la tabulation utilisée pour aligner les numéros de page.
        System::SharedPtr<Aspose::Words::TabStop> tab = para->get_ParagraphFormat()->get_TabStops()->idx_get(0);

        // Remplacez le premier arrêt de tabulation par défaut par un arrêt de tabulation personnalisé.
        para->get_ParagraphFormat()->get_TabStops()->RemoveByPosition(tab->get_Position());
        para->get_ParagraphFormat()->get_TabStops()->Add(tab->get_Position() - 50, tab->get_Alignment(), tab->get_Leader());
    }
}

doc->Save(get_ArtifactsDir() + u"Styles.ChangeTocsTabStops.docx");
```

## Voir aussi

* Enum [StyleIdentifier](../../styleidentifier/)
* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
