---
title: "Aspose::Words::Saving::DownsampleOptions class"
linktitle: "DownsampleOptions"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::DownsampleOptions class. Consente di specificare le opzioni di downsample. Per saperne di più, visita l'articolo della documentazione in C++."
type: docs
weight: 6000
url: /it/cpp/aspose.words.saving/downsampleoptions/
---
## DownsampleOptions class


Consente di specificare le opzioni di downsample. Per saperne di più, visita l'articolo di documentazione [Save a Document](https://docs.aspose.com/words/cpp/save-a-document/).

```cpp
class DownsampleOptions : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [DownsampleOptions](./downsampleoptions/)() |  |
| [get_DownsampleImages](./get_downsampleimages/)() const | Specifica se le immagini devono essere sottocampioniate. |
| [get_Resolution](./get_resolution/)() const | Specifica la risoluzione in pixel per pollice a cui le immagini devono essere sottocampioniate. |
| [get_ResolutionThreshold](./get_resolutionthreshold/)() const | Specifica la risoluzione soglia in pixel per pollice. Se la risoluzione di un'immagine nel documento è inferiore al valore soglia, l'algoritmo di sottocampionamento non verrà applicato. Un valore pari a 0 indica che il controllo soglia non è utilizzato e tutte le immagini che possono essere ridotte di dimensione vengono sottocampionate. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_DownsampleImages](./set_downsampleimages/)(bool) | Specifica se le immagini devono essere sottocampioniate. |
| [set_Resolution](./set_resolution/)(int32_t) | Specifica la risoluzione in pixel per pollice a cui le immagini devono essere sottocampioniate. |
| [set_ResolutionThreshold](./set_resolutionthreshold/)(int32_t) | Setter per [Aspose::Words::Saving::DownsampleOptions::get_ResolutionThreshold](./get_resolutionthreshold/). |
| static [Type](./type/)() |  |
## Vedi anche

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
