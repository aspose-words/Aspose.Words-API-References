---
title: "Espace de noms Aspose::Words::Layout"
linktitle: "Aspose::Words::Layout"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Espace de noms Aspose::Words::Layout. L'espace de noms Aspose.Words.Layout fournit des classes qui permettent d'accéder à des informations telles que la page sur laquelle et l'emplacement sur la page de certains éléments du document, lorsque le document est formaté en pages en C++."
type: docs
weight: 10000
url: /fr/cpp/aspose.words.layout/
---

L'espace de noms **Aspose.Words.Layout** fournit des classes qui permettent d'accéder à des informations telles que la page où se trouvent les éléments du document et leur position sur la page, lorsque le document est formaté en pages.

## Classes

| Classe | Description |
| --- | --- |
| [LayoutCollector](./layoutcollector/) | Cette classe permet de calculer les numéros de page des nœuds du document. Pour en savoir plus, consultez l'article de documentation [Converting to Fixed-page Format](https://docs.aspose.com/words/cpp/converting-to-fixed-page-format/). |
| [LayoutEnumerator](./layoutenumerator/) | Énumère les entités de mise en page d'un document. Vous pouvez utiliser cette classe pour parcourir le modèle de mise en page. Les propriétés disponibles sont le type, la géométrie, le texte et l'index de page où l'entité est rendue, ainsi que la structure globale et les relations. Utilisez la combinaison de [GetEntity()](../) et [Current](./layoutenumerator/get_current/) pour vous déplacer vers l'entité correspondant à un nœud du document. Pour en savoir plus, consultez l'article de documentation [Converting to Fixed-page Format](https://docs.aspose.com/words/cpp/converting-to-fixed-page-format/). |
| [LayoutOptions](./layoutoptions/) | Contient les options qui permettent de contrôler le processus de mise en page du document. Pour en savoir plus, consultez l'article de documentation [Converting to Fixed-page Format](https://docs.aspose.com/words/cpp/converting-to-fixed-page-format/). |
| [PageLayoutCallbackArgs](./pagelayoutcallbackargs/) | Un argument passé à [Notify()](./ipagelayoutcallback/notify/). Pour en savoir plus, consultez l'article de documentation [Converting to Fixed-page Format](https://docs.aspose.com/words/cpp/converting-to-fixed-page-format/). |
| [RevisionOptions](./revisionoptions/) | Permet de contrôler la façon dont les révisions du document sont gérées pendant le processus de mise en page. Pour en savoir plus, consultez l'article de documentation [Converting to Fixed-page Format](https://docs.aspose.com/words/cpp/converting-to-fixed-page-format/). |
## Interfaces

| Interface | Description |
| --- | --- |
| [IPageLayoutCallback](./ipagelayoutcallback/) | Implémentez cette interface si vous souhaitez disposer de votre propre méthode personnalisée appelée pendant la construction et le rendu du modèle de mise en page. |
## Enums

| Enum | Description |
| --- | --- |
| [CommentDisplayMode](./commentdisplaymode/) | Spécifie le mode de rendu pour les commentaires du document. |
| [ContinuousSectionRestart](./continuoussectionrestart/) | Représente différents comportements lors du calcul des numéros de page dans une section continue qui redémarre la numérotation des pages. |
| [LayoutEntityType](./layoutentitytype/) | Types des entités de mise en page. |
| [PageLayoutEvent](./pagelayoutevent/) | Un code d'événement déclenché lors de la construction et du rendu du modèle de mise en page. Le modèle de mise en page est construit en deux étapes. D'abord, l'« étape de conversion », où la mise en page extrait le contenu du document et crée le graphe d'objets. Ensuite, l'« étape de reflow », où les structures sont divisées, fusionnées et organisées en pages. Selon l'opération qui a déclenché la construction, le modèle de mise en page peut ou non être rendu ultérieurement au format de page fixe. Par exemple, le calcul du nombre de pages du document ou la mise à jour des champs ne nécessite pas de rendu, alors que l'exportation vers PDF le nécessite. |
| [RevisionColor](./revisioncolor/) | Permet de spécifier la couleur des révisions du document. |
| [RevisionTextEffect](./revisiontexteffect/) | Permet de spécifier l'effet de décoration pour les révisions du texte du document. |
| [ShowInBalloons](./showinballoons/) | Spécifie quelles révisions sont rendues sous forme de bulles. |
