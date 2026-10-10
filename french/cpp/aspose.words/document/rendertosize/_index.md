---
title: "Méthode Aspose::Words::Document::RenderToSize"
linktitle: "RenderToSize"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Document::RenderToSize. Rend une page de document dans un objet Graphics à une taille spécifiée en C++."
type: docs
weight: 71000
url: /fr/cpp/aspose.words/document/rendertosize/
---
## Document::RenderToSize method


Rend une page de document dans un objet **Graphics** à une taille spécifiée.

```cpp
float Aspose::Words::Document::RenderToSize(int32_t pageIndex, const System::SharedPtr<System::Drawing::Graphics> &graphics, float x, float y, float width, float height)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| pageIndex | int32_t | L'index de page basé sur zéro. |
| graphics | const System::SharedPtr\<System::Drawing::Graphics\>\& | L'objet où rendre. |
| x | float | La coordonnée X (en unités du monde) du coin supérieur gauche de la page rendue. |
| y | float | La coordonnée Y (en unités du monde) du coin supérieur gauche de la page rendue. |
| largeur | float | La largeur maximale (en unités du monde) qui peut être occupée par la page rendue. |
| hauteur | float | La hauteur maximale (en unités du monde) qui peut être occupée par la page rendue. |

### ReturnValue

L'échelle qui a été calculée automatiquement pour la page rendue afin de s'adapter à la taille spécifiée.

## Voir aussi

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
