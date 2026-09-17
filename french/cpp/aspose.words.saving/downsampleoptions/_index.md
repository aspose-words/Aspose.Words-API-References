---
title: "Aspose::Words::Saving::DownsampleOptions class"
linktitle: "DownsampleOptions"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::DownsampleOptions class. Permet de spécifier les options de sous-échantillonnage. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 6000
url: /fr/cpp/aspose.words.saving/downsampleoptions/
---
## DownsampleOptions class


Permet de spécifier les options de sous‑échantillonnage. Pour en savoir plus, consultez l'article de documentation [Save a Document](https://docs.aspose.com/words/cpp/save-a-document/).

```cpp
class DownsampleOptions : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [DownsampleOptions](./downsampleoptions/)() |  |
| [get_DownsampleImages](./get_downsampleimages/)() const | Spécifie si les images doivent être sous-échantillonnées. |
| [get_Resolution](./get_resolution/)() const | Spécifie la résolution en pixels par pouce à laquelle les images doivent être sous-échantillonnées. |
| [get_ResolutionThreshold](./get_resolutionthreshold/)() const | Spécifie la résolution seuil en pixels par pouce. Si la résolution d'une image dans le document est inférieure à la valeur seuil, l'algorithme de sous-échantillonnage ne sera pas appliqué. Une valeur de 0 signifie que la vérification du seuil n'est pas utilisée et que toutes les images pouvant être réduites en taille sont sous-échantillonnées. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_DownsampleImages](./set_downsampleimages/)(bool) | Spécifie si les images doivent être sous-échantillonnées. |
| [set_Resolution](./set_resolution/)(int32_t) | Spécifie la résolution en pixels par pouce à laquelle les images doivent être sous-échantillonnées. |
| [set_ResolutionThreshold](./set_resolutionthreshold/)(int32_t) | Mutateur pour [Aspose::Words::Saving::DownsampleOptions::get_ResolutionThreshold](./get_resolutionthreshold/). |
| static [Type](./type/)() |  |
## Voir aussi

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
