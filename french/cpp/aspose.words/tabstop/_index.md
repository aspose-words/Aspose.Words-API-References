---
title: "Aspose::Words::TabStop class"
linktitle: "TabStop"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::TabStop class. Représente un arrêt de tabulation personnalisé unique. L'objet TabStop est un membre de la collection TabStopCollection. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 68000
url: /fr/cpp/aspose.words/tabstop/
---
## TabStop class


Représente un arrêt de tabulation personnalisé unique. L'objet [TabStop](./) est un membre de la collection [TabStopCollection](../tabstopcollection/). Pour en savoir plus, consultez l'article de documentation [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/).

```cpp
class TabStop : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [Equals](./equals/)(const System::SharedPtr\<Aspose::Words::TabStop\>\&) | Compare avec le [TabStop](./) spécifié. |
| [get_Alignment](./get_alignment/)() const | Obtient ou définit l'alignement du texte à cet arrêt de tabulation. |
| [get_IsClear](./get_isclear/)() | Renvoie **true** si cet arrêt de tabulation supprime tous les arrêts de tabulation existants à cette position. |
| [get_Leader](./get_leader/)() const | Obtient ou définit le type de la ligne de repère affichée sous le caractère de tabulation. |
| [get_Position](./get_position/)() | Obtient la position de l'arrêt de tabulation en points. |
| [GetHashCode](./gethashcode/)() const override | Calcule le code de hachage pour cet objet. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Alignment](./set_alignment/)(Aspose::Words::TabAlignment) | Définisseur pour [Aspose::Words::TabStop::get_Alignment](./get_alignment/). |
| [set_Leader](./set_leader/)(Aspose::Words::TabLeader) | Définisseur pour [Aspose::Words::TabStop::get_Leader](./get_leader/). |
| [TabStop](./tabstop/)(double) | Initialise une nouvelle instance de cette classe. |
| [TabStop](./tabstop/)(double, Aspose::Words::TabAlignment, Aspose::Words::TabLeader) | Initialise une nouvelle instance de cette classe. |
| static [Type](./type/)() |  |
## Remarques


Normalement, un arrêt de tabulation spécifie une position où un arrêt de tabulation existe. Mais comme les arrêts de tabulation peuvent être hérités des styles parents, il peut être nécessaire que l'objet enfant définisse explicitement qu'il n'y a aucun arrêt de tabulation à une position donnée. Pour supprimer un arrêt de tabulation hérité à une position donnée, créez un objet [TabStop](./) et définissez [Alignment](./get_alignment/) sur [Clear](../tabalignment/).

Pour plus d'informations, voir [TabStopCollection](../tabstopcollection/).

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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
