---
title: "interface Aspose::Words::Layout::IPageLayoutCallback"
linktitle: "IPageLayoutCallback"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "interface Aspose::Words::Layout::IPageLayoutCallback. Implémentez cette interface si vous souhaitez disposer de votre propre méthode personnalisée appelée pendant la construction et le rendu du modèle de mise en page dans C++."
type: docs
weight: 6000
url: /fr/cpp/aspose.words.layout/ipagelayoutcallback/
---
## IPageLayoutCallback interface


Implémentez cette interface si vous souhaitez disposer de votre propre méthode personnalisée appelée pendant la construction et le rendu du modèle de mise en page.

```cpp
class IPageLayoutCallback : public virtual System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Notify](./notify/)(System::SharedPtr\<Aspose::Words::Layout::PageLayoutCallbackArgs\>) | Ceci est appelé pour notifier de la progression de la construction et du rendu de la mise en page. |
| static [Type](./type/)() |  |
## Remarques


L'utilisation principale de cette interface est de permettre au code de l'application d'interrompre le processus de construction.

Il est possible de construire le modèle de mise en page pour seulement quelques pages au début du document, puis d'interrompre le processus et de rendre uniquement ce qui a déjà été construit.

Notez toutefois que les résultats du rendu peuvent ne pas correspondre à ce qui aurait été rendu pour chaque page si le processus s'était terminé.

Cette technique peut ne pas fonctionner pour chaque document ou échouer complètement.

## Voir aussi

* Namespace [Aspose::Words::Layout](../)
* Library [Aspose.Words for C++](../../)
