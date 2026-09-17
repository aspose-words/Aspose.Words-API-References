---
title: "Aspose::Words::Document::RenderToScale méthode"
linktitle: "RenderToScale"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Document::RenderToScale méthode. Rend une page de document dans un objet Graphics à une échelle spécifiée en C++."
type: docs
weight: 70000
url: /fr/cpp/aspose.words/document/rendertoscale/
---
## Document::RenderToScale method


Rend une page de document dans un objet **Graphics** à une échelle spécifiée.

```cpp
System::Drawing::SizeF Aspose::Words::Document::RenderToScale(int32_t pageIndex, const System::SharedPtr<System::Drawing::Graphics> &graphics, float x, float y, float scale)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| pageIndex | int32_t | L'index de page basé sur zéro. |
| graphics | const System::SharedPtr\<System::Drawing::Graphics\>\& | L'objet où rendre. |
| x | float | La coordonnée X (en unités du monde) du coin supérieur gauche de la page rendue. |
| y | float | La coordonnée Y (en unités du monde) du coin supérieur gauche de la page rendue. |
| scale | float | L'échelle pour le rendu de la page (1,0 représente 100 %). |

### ReturnValue

La largeur et la hauteur (en unités du monde) de la page rendue.

## Voir aussi

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
