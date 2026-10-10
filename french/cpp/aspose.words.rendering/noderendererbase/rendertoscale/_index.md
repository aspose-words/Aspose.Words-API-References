---
title: "Méthode Aspose::Words::Rendering::NodeRendererBase::RenderToScale"
linktitle: "RenderToScale"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Rendering::NodeRendererBase::RenderToScale. Rend la forme dans un objet Graphics à une échelle spécifiée en C++."
type: docs
weight: 11000
url: /fr/cpp/aspose.words.rendering/noderendererbase/rendertoscale/
---
## NodeRendererBase::RenderToScale method


Rend la forme dans un objet **Graphics** à une échelle spécifiée.

```cpp
System::Drawing::SizeF Aspose::Words::Rendering::NodeRendererBase::RenderToScale(const System::SharedPtr<System::Drawing::Graphics> &graphics, float x, float y, float scale)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| graphics | const System::SharedPtr\<System::Drawing::Graphics\>\& | L'objet où rendre. |
| x | float | La coordonnée X (en unités du monde) du coin supérieur gauche de la forme rendue. |
| y | float | La coordonnée Y (en unités du monde) du coin supérieur gauche de la forme rendue. |
| scale | float | L'échelle pour le rendu de la forme (1,0 représente 100 %). |

### ReturnValue

La largeur et la hauteur (en unités du monde) de la forme rendue.

## Voir aussi

* Class [NodeRendererBase](../)
* Namespace [Aspose::Words::Rendering](../../)
* Library [Aspose.Words for C++](../../../)
