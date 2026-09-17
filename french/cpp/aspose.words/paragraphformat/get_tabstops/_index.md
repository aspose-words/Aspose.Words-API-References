---
title: "Aspose::Words::ParagraphFormat::get_TabStops méthode"
linktitle: "get_TabStops"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::ParagraphFormat::get_TabStops méthode. Obtient la collection des tabulations personnalisées définies pour cet objet en C++."
type: docs
weight: 40000
url: /fr/cpp/aspose.words/paragraphformat/get_tabstops/
---
## ParagraphFormat::get_TabStops method


Obtient la collection d’arrêts de tabulation personnalisés définis pour cet objet.

```cpp
System::SharedPtr<Aspose::Words::TabStopCollection> Aspose::Words::ParagraphFormat::get_TabStops()
```


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

* Class [TabStopCollection](../../tabstopcollection/)
* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
