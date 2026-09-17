---
title: "Aspose::Words::TabStopCollection::Add méthode"
linktitle: "Add"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::TabStopCollection::Add méthode. Ajoute ou remplace un arrêt de tabulation dans la collection en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words/tabstopcollection/add/
---
## TabStopCollection::Add(const System::SharedPtr\<Aspose::Words::TabStop\>\&) method


Ajoute ou remplace une tabulation dans la collection.

```cpp
void Aspose::Words::TabStopCollection::Add(const System::SharedPtr<Aspose::Words::TabStop> &tabStop)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| tabStop | const System::SharedPtr\<Aspose::Words::TabStop\>\& | Un objet d'arrêt de tabulation à ajouter. |
## Remarques


Si un arrêt de tabulation existe déjà à la position spécifiée, il est remplacé.

## Exemples



Montre comment ajouter des arrêts de tabulation personnalisés à un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto paragraph = System::ExplicitCast<Aspose::Words::Paragraph>(doc->GetChild(Aspose::Words::NodeType::Paragraph, 0, true));

// Voici deux façons d'ajouter des arrêts de tabulation à la collection d'arrêts de tabulation d'un paragraphe via la propriété "ParagraphFormat".
// 1 -  Créez un objet "TabStop", puis ajoutez-le à la collection :
auto tabStop = System::MakeObject<Aspose::Words::TabStop>(Aspose::Words::ConvertUtil::InchToPoint(3), Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dashes);
paragraph->get_ParagraphFormat()->get_TabStops()->Add(tabStop);

// 2 -  Transmettez les valeurs des propriétés d'un nouvel arrêt de tabulation à la méthode "Add" :
paragraph->get_ParagraphFormat()->get_TabStops()->Add(Aspose::Words::ConvertUtil::MillimeterToPoint(100), Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dashes);

// Ajoutez des arrêts de tabulation à 5 cm à tous les paragraphes.
for (auto&& para : System::IterateOver(doc->GetChildNodes(Aspose::Words::NodeType::Paragraph, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Paragraph> >()))
{
    para->get_ParagraphFormat()->get_TabStops()->Add(Aspose::Words::ConvertUtil::MillimeterToPoint(50), Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dashes);
}

// Chaque caractère "tab" déplace le curseur du constructeur vers l'emplacement de la prochaine tabulation.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Start\tTab 1\tTab 2\tTab 3\tTab 4");

doc->Save(get_ArtifactsDir() + u"TabStopCollection.AddTabStops.docx");
```

## Voir aussi

* Class [TabStop](../../tabstop/)
* Class [TabStopCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## TabStopCollection::Add(double, Aspose::Words::TabAlignment, Aspose::Words::TabLeader) method


Ajoute ou remplace une tabulation dans la collection.

```cpp
void Aspose::Words::TabStopCollection::Add(double position, Aspose::Words::TabAlignment alignment, Aspose::Words::TabLeader leader)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| position | double | Une position (en points) où ajouter l'arrêt de tabulation. |
| alignment | Aspose::Words::TabAlignment | Une valeur [TabAlignment](../../tabalignment/) qui spécifie l'alignement du texte à l'arrêt de tabulation. |
| leader | Aspose::Words::TabLeader | Une valeur [TabLeader](../../tableader/) qui spécifie le type de ligne de repère affichée sous le caractère de tabulation. |
## Remarques


Si un arrêt de tabulation existe déjà à la position spécifiée, il est remplacé.

## Exemples



Montre comment ajouter des arrêts de tabulation personnalisés à un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto paragraph = System::ExplicitCast<Aspose::Words::Paragraph>(doc->GetChild(Aspose::Words::NodeType::Paragraph, 0, true));

// Voici deux façons d'ajouter des arrêts de tabulation à la collection d'arrêts de tabulation d'un paragraphe via la propriété "ParagraphFormat".
// 1 -  Créez un objet "TabStop", puis ajoutez-le à la collection :
auto tabStop = System::MakeObject<Aspose::Words::TabStop>(Aspose::Words::ConvertUtil::InchToPoint(3), Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dashes);
paragraph->get_ParagraphFormat()->get_TabStops()->Add(tabStop);

// 2 -  Transmettez les valeurs des propriétés d'un nouvel arrêt de tabulation à la méthode "Add" :
paragraph->get_ParagraphFormat()->get_TabStops()->Add(Aspose::Words::ConvertUtil::MillimeterToPoint(100), Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dashes);

// Ajoutez des arrêts de tabulation à 5 cm à tous les paragraphes.
for (auto&& para : System::IterateOver(doc->GetChildNodes(Aspose::Words::NodeType::Paragraph, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Paragraph> >()))
{
    para->get_ParagraphFormat()->get_TabStops()->Add(Aspose::Words::ConvertUtil::MillimeterToPoint(50), Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dashes);
}

// Chaque caractère "tab" déplace le curseur du constructeur vers l'emplacement de la prochaine tabulation.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Start\tTab 1\tTab 2\tTab 3\tTab 4");

doc->Save(get_ArtifactsDir() + u"TabStopCollection.AddTabStops.docx");
```

## Voir aussi

* Enum [TabAlignment](../../tabalignment/)
* Enum [TabLeader](../../tableader/)
* Class [TabStopCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
