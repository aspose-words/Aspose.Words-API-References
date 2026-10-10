---
title: "Aspose::Words::TabStop::get_Alignment méthode"
linktitle: "get_Alignment"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::TabStop::get_Alignment méthode. Obtient ou définit l'alignement du texte à cette tabulation en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words/tabstop/get_alignment/
---
## TabStop::get_Alignment method


Obtient ou définit l'alignement du texte à cet arrêt de tabulation.

```cpp
Aspose::Words::TabAlignment Aspose::Words::TabStop::get_Alignment() const
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

* Enum [TabAlignment](../../tabalignment/)
* Class [TabStop](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
