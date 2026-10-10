---
title: "Méthode Aspose::Words::Node::ToString"
linktitle: "ToString"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Node::ToString. Exporte le contenu du nœud dans une chaîne au format spécifié en C++."
type: docs
weight: 22000
url: /fr/cpp/aspose.words/node/tostring/
---
## Node::ToString(Aspose::Words::SaveFormat) method


Exporte le contenu du nœud dans une chaîne au format spécifié.

```cpp
System::String Aspose::Words::Node::ToString(Aspose::Words::SaveFormat saveFormat)
```


### ReturnValue

Le contenu du nœud dans le format spécifié.

## Exemples



Montre la différence entre l'appel des méthodes GetText et ToString sur un nœud.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->InsertField(u"MERGEFIELD Field");

// GetText récupérera le texte visible ainsi que les codes de champ et les caractères spéciaux.
ASSERT_EQ(u"\u0013MERGEFIELD Field\u0014«Field»\u0015", doc->GetText().Trim());

// ToString nous donnera l'apparence du document s'il est enregistré dans le format de sauvegarde fourni.
ASSERT_EQ(u"«Field»", doc->ToString(Aspose::Words::SaveFormat::Text).Trim());
```


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


Exporte le contenu d'un nœud en chaîne au format HTML.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

System::SharedPtr<Aspose::Words::Node> node = doc->get_LastSection()->get_Body()->get_LastParagraph();

// Lorsque nous appelons la méthode ToString en utilisant la surcharge html de SaveFormat,
// elle convertit le contenu du nœud en leur représentation HTML brute.
ASSERT_EQ(System::String(u"<p style=\"margin-top:0pt; margin-bottom:8pt; line-height:108%; font-size:12pt\">") + u"<span style=\"font-family:'Times New Roman'\">Hello World!</span>" + u"</p>", node->ToString(Aspose::Words::SaveFormat::Html));

// Nous pouvons également modifier le résultat de cette conversion en utilisant un objet SaveOptions.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
saveOptions->set_ExportRelativeFontSize(true);

ASSERT_EQ(System::String(u"<p style=\"margin-top:0pt; margin-bottom:8pt; line-height:108%\">") + u"<span style=\"font-family:'Times New Roman'\">Hello World!</span>" + u"</p>", node->ToString(saveOptions));
```

## Voir aussi

* Enum [SaveFormat](../../saveformat/)
* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Node::ToString(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) method


Exporte le contenu du nœud dans une chaîne en utilisant les options d'enregistrement spécifiées.

```cpp
System::String Aspose::Words::Node::ToString(const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Spécifie les options qui contrôlent la façon dont le nœud est enregistré. |

### ReturnValue

Le contenu du nœud dans le format spécifié.

## Exemples



Exporte le contenu d'un nœud en chaîne au format HTML.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

System::SharedPtr<Aspose::Words::Node> node = doc->get_LastSection()->get_Body()->get_LastParagraph();

// Lorsque nous appelons la méthode ToString en utilisant la surcharge html de SaveFormat,
// elle convertit le contenu du nœud en leur représentation HTML brute.
ASSERT_EQ(System::String(u"<p style=\"margin-top:0pt; margin-bottom:8pt; line-height:108%; font-size:12pt\">") + u"<span style=\"font-family:'Times New Roman'\">Hello World!</span>" + u"</p>", node->ToString(Aspose::Words::SaveFormat::Html));

// Nous pouvons également modifier le résultat de cette conversion en utilisant un objet SaveOptions.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
saveOptions->set_ExportRelativeFontSize(true);

ASSERT_EQ(System::String(u"<p style=\"margin-top:0pt; margin-bottom:8pt; line-height:108%\">") + u"<span style=\"font-family:'Times New Roman'\">Hello World!</span>" + u"</p>", node->ToString(saveOptions));
```

## Voir aussi

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
