---
title: "Aspose::Words::Layout::PageLayoutCallbackArgs class"
linktitle: "PageLayoutCallbackArgs"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Layout::PageLayoutCallbackArgs classe. Un argument passé à Notify() Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words.layout/pagelayoutcallbackargs/
---
## PageLayoutCallbackArgs class


Un argument passé à [Notify()](../ipagelayoutcallback/notify/) Pour en savoir plus, consultez l'article de documentation [Conversion au format à page fixe](https://docs.aspose.com/words/cpp/converting-to-fixed-page-format/).

```cpp
class PageLayoutCallbackArgs : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_Document](./get_document/)() const | Obtient le document. |
| [get_Event](./get_event/)() const | Obtient l'événement. |
| [get_PageIndex](./get_pageindex/)() | Obtient l'index basé sur 0 de la page du document à laquelle cet événement se rapporte. Retourne une valeur négative s'il n'y a pas de page associée, ou si la page a été supprimée lors du reflow. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Voir aussi

* Namespace [Aspose::Words::Layout](../)
* Library [Aspose.Words for C++](../../)
