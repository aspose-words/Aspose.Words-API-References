---
title: "Aspose::Words::Rendering::NodeRendererBase::RenderToSize method"
linktitle: "RenderToSize"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Rendering::NodeRendererBase::RenderToSize method. Rend la forme dans un objet Graphics à une taille spécifiée en C++."
type: docs
weight: 12000
url: /fr/cpp/aspose.words.rendering/noderendererbase/rendertosize/
---
## NodeRendererBase::RenderToSize method


Rend la forme dans un objet **Graphics** à une taille spécifiée.

```cpp
float Aspose::Words::Rendering::NodeRendererBase::RenderToSize(const System::SharedPtr<System::Drawing::Graphics> &graphics, float x, float y, float width, float height)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| graphics | const System::SharedPtr\<System::Drawing::Graphics\>\& | L'objet où rendre. |
| x | float | La coordonnée X (en unités du monde) du coin supérieur gauche de la forme rendue. |
| y | float | La coordonnée Y (en unités du monde) du coin supérieur gauche de la forme rendue. |
| largeur | float | La largeur maximale (en unités du monde) qui peut être occupée par la forme rendue. |
| hauteur | float | La hauteur maximale (en unités du monde) qui peut être occupée par la forme rendue. |

### ReturnValue

L'échelle qui a été calculée automatiquement pour la forme rendue afin de correspondre à la taille spécifiée.

## Voir aussi

* Class [NodeRendererBase](../)
* Namespace [Aspose::Words::Rendering](../../)
* Library [Aspose.Words for C++](../../../)
