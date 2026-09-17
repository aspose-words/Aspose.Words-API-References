---
title: "classe Aspose::Words::Lists::ListLabel"
linktitle: "ListLabel"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "classe Aspose::Words::Lists::ListLabel. Définit les propriétés spécifiques à une étiquette de liste. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words.lists/listlabel/
---
## ListLabel class


Définit les propriétés spécifiques à une étiquette de liste. Pour en savoir plus, consultez l’article de documentation [Working with Lists](https://docs.aspose.com/words/cpp/working-with-lists/).

```cpp
class ListLabel : public Aspose::Words::IRunAttrSource
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_Font](./get_font/)() | Obtient la police de l'étiquette de liste. |
| [get_LabelString](./get_labelstring/)() | Obtient une représentation sous forme de chaîne de l'étiquette de liste. |
| [get_LabelValue](./get_labelvalue/)() | Obtient une valeur numérique pour cette étiquette. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

## Exemples



Montre comment extraire les étiquettes de liste de tous les paragraphes qui sont des éléments de liste.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");
doc->UpdateListLabels();

System::SharedPtr<Aspose::Words::NodeCollection> paras = doc->GetChildNodes(Aspose::Words::NodeType::Paragraph, true);

// Trouver si nous avons la liste de paragraphes. Dans notre document, notre liste utilise des nombres arabes simples,
// qui commencent à trois et se terminent à six.
for (auto&& paragraph : paras->LINQ_OfType<System::SharedPtr<Aspose::Words::Paragraph> >()->LINQ_Where(static_cast<System::Func<System::SharedPtr<Aspose::Words::Paragraph>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Paragraph> p)>>([](System::SharedPtr<Aspose::Words::Paragraph> p) -> bool
{
    return p->get_ListFormat()->get_IsListItem();
})))->LINQ_ToList())
{
    std::cout << System::String::Format(u"List item paragraph #{0}", paras->IndexOf(paragraph)) << std::endl;

    // Voici le texte que nous obtenons lorsque nous exportons ce nœud au format texte.
    // Cette sortie texte omettra les étiquettes de liste. Supprimez tout caractère de formatage de paragraphe.
    System::String paragraphText = paragraph->ToString(Aspose::Words::SaveFormat::Text).Trim();
    std::cout << System::String::Format(u"\tExported Text: {0}", paragraphText) << std::endl;

    System::SharedPtr<Aspose::Words::Lists::ListLabel> label = paragraph->get_ListLabel();

    // Cela obtient la position du paragraphe dans le niveau actuel de la liste. Si nous avons une liste avec plusieurs niveaux,
    // cela nous indiquera quelle position il occupe à ce niveau.
    std::cout << System::String::Format(u"\tNumerical Id: {0}", label->get_LabelValue()) << std::endl;

    // Combinez-les pour inclure l'étiquette de liste avec le texte dans la sortie.
    std::cout << System::String::Format(u"\tList label combined with text: {0} {1}", label->get_LabelString(), paragraphText) << std::endl;
}
```

## Voir aussi

* Namespace [Aspose::Words::Lists](../)
* Library [Aspose.Words for C++](../../)
