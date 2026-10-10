---
title: "Aspose::Words::NodeImporter class"
linktitle: "NodeImporter"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::NodeImporter class. Permet d'effectuer efficacement des importations répétées de nœuds d'un document à un autre. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 44000
url: /fr/cpp/aspose.words/nodeimporter/
---
## NodeImporter class


Permet d'effectuer efficacement des importations répétées de nœuds d'un document à un autre. Pour en savoir plus, consultez l'article de documentation [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/).

```cpp
class NodeImporter : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [ImportNode](./importnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&, bool) | Importe un nœud d'un document à un autre. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [NodeImporter](./nodeimporter/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, Aspose::Words::ImportFormatMode) | Initialise une nouvelle instance de la classe [NodeImporter](./). |
| [NodeImporter](./nodeimporter/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, Aspose::Words::ImportFormatMode, const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\&) | Initialise une nouvelle instance de la classe [NodeImporter](./). |
| static [Type](./type/)() |  |
## Remarques


Aspose.Words fournit des fonctionnalités permettant de copier et déplacer facilement des fragments entre des documents Microsoft Word. Cela s'appelle "importation de nœuds". Avant de pouvoir insérer un fragment d'un document dans un autre, vous devez l'"importer". L'importation crée un clone profond du nœud original, prêt à être inséré dans le document de destination.

La façon la plus simple d'importer un nœud est d'utiliser la méthode [ImportNode()](../) fournie par l'objet [DocumentBase](../documentbase/).

Cependant, lorsque vous devez importer des nœuds d'un document à un autre plusieurs fois, il est préférable d'utiliser la classe [NodeImporter](./). La classe [NodeImporter](./) permet de minimiser le nombre de styles et de listes créés dans le document de destination.

Copier ou déplacer des fragments d'un document Microsoft Word à un autre présente un certain nombre de défis techniques pour Aspose.Words. Dans un document Word, les styles et la mise en forme des listes sont stockés de manière centrale, séparément du texte du document. Les paragraphes et les segments de texte ne font que référencer les styles à l'aide d'identifiants uniques internes.

Les défis proviennent du fait que les styles et les listes diffèrent d'un document à l'autre. Par exemple, pour copier un paragraphe formaté avec le style Titre 1 d'un document à un autre, plusieurs éléments doivent être pris en compte : décider s'il faut copier le style Titre 1 du document source vers le document de destination, cloner le paragraphe, mettre à jour le paragraphe cloné afin qu'il fasse référence au style Titre 1 correct dans le document de destination. Si le style doit être copié, tous les styles qu'il référence (basés sur le style et le style du paragraphe suivant) doivent être analysés et éventuellement copiés également, etc. Des problèmes similaires existent lors de la copie de paragraphes à puces ou numérotés, car Microsoft Word stocke les définitions de listes séparément du texte.

La classe [NodeImporter](./) agit comme un contexte, qui conserve les "tables de traduction" pendant l'importation. Elle traduit correctement les styles et les listes entre les documents source et destination.

## Voir aussi

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
