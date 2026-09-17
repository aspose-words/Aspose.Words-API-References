---
title: "Aspose::Words::Layout::PageLayoutEvent enum"
linktitle: "PageLayoutEvent"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Layout::PageLayoutEvent enum. Un code d'événement déclenché lors de la construction et du rendu du modèle de mise en page. Le modèle de mise en page est construit en deux étapes. Premièrement, l'\"étape de conversion\", qui consiste à extraire le contenu du document et à créer le graphe d'objets. Deuxièmement, l'\"étape de reflow\", où les structures sont divisées, fusionnées et organisées en pages. Selon l'opération qui a déclenché la construction, le modèle de mise en page peut ou non être rendu davantage au format de page fixe. Par exemple, le calcul du nombre de pages du document ou la mise à jour des champs ne nécessite pas de rendu, alors que l'exportation vers PDF le nécessite en C++."
type: docs
weight: 10000
url: /fr/cpp/aspose.words.layout/pagelayoutevent/
---
## PageLayoutEvent enum


Un code d'événement déclenché lors de la construction et du rendu du modèle de mise en page. Le modèle de mise en page est construit en deux étapes. D'abord, l'« étape de conversion », où la mise en page extrait le contenu du document et crée le graphe d'objets. Ensuite, l'« étape de reflow », où les structures sont divisées, fusionnées et organisées en pages. Selon l'opération qui a déclenché la construction, le modèle de mise en page peut ou non être rendu ultérieurement au format de page fixe. Par exemple, le calcul du nombre de pages du document ou la mise à jour des champs ne nécessite pas de rendu, alors que l'exportation vers PDF le nécessite.

```cpp
enum class PageLayoutEvent
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| None | 0 | Valeur par défaut. |
| WatchDog | 1 | Correspond à un point de contrôle dans le code qui est souvent atteint et qui convient pour interrompre le processus. Lorsqu'on est à l'intérieur de [Notify()](../ipagelayoutcallback/notify/), lancez une exception personnalisée pour interrompre le processus. Vous pouvez lancer l'exception lors du traitement de tout événement de rappel pour interrompre le processus. Notez que si le processus est interrompu, le modèle de mise en page reste dans un état indéfini. Si le processus est interrompu lors du reflow d'une page complète, il devrait toutefois être possible d'utiliser le modèle de mise en page jusqu'à la fin de cette page. |
| BuildStarted | 2 | La construction de la mise en page a commencé. Déclenché une fois. C'est le premier événement qui se produit lorsque [UpdatePageLayout](../../aspose.words/document/updatepagelayout/) est appelé. |
| BuildFinished | 3 | La construction de la mise en page est terminée. Déclenché une fois. C'est le dernier événement qui se produit lorsque [UpdatePageLayout](../../aspose.words/document/updatepagelayout/) est appelé. |
| ConversionStarted | 4 | La conversion du modèle de document en mise en page a commencé. Déclenché une fois. Cela se produit lorsque le modèle de mise en page commence à extraire le contenu du document. |
| ConversionFinished | 5 | La conversion du modèle de document en mise en page est terminée. Déclenché une fois. Cela se produit lorsque le modèle de mise en page cesse d'extraire le contenu du document. |
| ReflowStarted | 6 | Le reflow de la mise en page a commencé. Déclenché une fois. Cela se produit lorsque le modèle de mise en page commence le reflow du contenu du document. |
| ReflowFinished | 7 | Le reflow de la mise en page est terminé. Déclenché une fois. Cela se produit lorsque le modèle de mise en page cesse le reflow du contenu du document. |
| PartReflowStarted | 8 | Le reflow de la page a commencé. Notez que la page peut être reflowée plusieurs fois et que le reflow peut redémarrer avant d'être terminé. |
| PartReflowFinished | 9 | Le reflow de la page est terminé. Notez que la page peut être reflowée plusieurs fois et que le reflow peut redémarrer avant d'être terminé. |
| PartRenderingStarted | 10 | [Rendering](../../aspose.words.rendering/) de la page a commencé. Ceci est déclenché une fois par page. |
| PartRenderingFinished | 11 | [Rendering](../../aspose.words.rendering/) de la page est terminé. Ceci est déclenché une fois par page. |

## Voir aussi

* Namespace [Aspose::Words::Layout](../)
* Library [Aspose.Words for C++](../../)
