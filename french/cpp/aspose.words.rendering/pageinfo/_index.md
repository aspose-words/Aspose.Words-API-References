---
title: "classe Aspose::Words::Rendering::PageInfo"
linktitle: "PageInfo"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "classe Aspose::Words::Rendering::PageInfo. Représente les informations concernant une page particulière du document. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 3000
url: /fr/cpp/aspose.words.rendering/pageinfo/
---
## PageInfo class


Représente les informations concernant une page de document particulière. Pour en savoir plus, consultez l'article de documentation [Rendering](https://docs.aspose.com/words/cpp/rendering/).

```cpp
class PageInfo : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_Colored](./get_colored/)() | Renvoie **true** si la page contient du contenu coloré. |
| [get_HeightInPoints](./get_heightinpoints/)() | Obtient la hauteur de la page en points. |
| [get_Landscape](./get_landscape/)() const | Renvoie **true** si l'orientation de la page spécifiée dans le document pour cette page est paysage. |
| [get_PaperSize](./get_papersize/)() | Obtient la taille du papier sous forme d'énumération. |
| [get_PaperTray](./get_papertray/)() const | Obtient le bac à papier (tray) pour cette page tel que spécifié dans le document. La valeur dépend de l'implémentation (imprimante). |
| [get_SizeInPoints](./get_sizeinpoints/)() const | Obtient la taille de la page en points. |
| [get_WidthInPoints](./get_widthinpoints/)() | Obtient la largeur de la page en points. |
| [GetSizeInPixels](./getsizeinpixels/)(float, float) | Calcule la taille de la page en pixels pour un facteur de zoom et une résolution spécifiés. |
| [GetSizeInPixels](./getsizeinpixels/)(float, float, float) | Calcule la taille de la page en pixels pour un facteur de zoom et une résolution spécifiés. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Remarques


La largeur et la hauteur de la page renvoyées par cet objet représentent la taille "finale" de la page, par ex. elles sont déjà pivotées dans la bonne orientation.

## Voir aussi

* Namespace [Aspose::Words::Rendering](../)
* Library [Aspose.Words for C++](../../)
