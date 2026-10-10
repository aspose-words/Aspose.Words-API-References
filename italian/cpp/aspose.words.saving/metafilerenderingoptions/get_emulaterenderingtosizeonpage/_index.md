---
title: "Aspose::Words::Saving::MetafileRenderingOptions::get_EmulateRenderingToSizeOnPage method"
linktitle: "get_EmulateRenderingToSizeOnPage"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::MetafileRenderingOptions::get_EmulateRenderingToSizeOnPage method. Ottiene o imposta un valore che determina se il rendering del metafile emula la visualizzazione del metafile in base alle dimensioni sulla pagina o la visualizzazione del metafile nella sua dimensione predefinita in C++."
type: docs
weight: 4334
url: /it/cpp/aspose.words.saving/metafilerenderingoptions/get_emulaterenderingtosizeonpage/
---
## MetafileRenderingOptions::get_EmulateRenderingToSizeOnPage method


Ottiene o imposta un valore che determina se il rendering del metafile emula la visualizzazione del metafile in base alle dimensioni sulla pagina o la visualizzazione del metafile nella sua dimensione predefinita.

```cpp
bool Aspose::Words::Saving::MetafileRenderingOptions::get_EmulateRenderingToSizeOnPage() const
```

## Note


Quando i metafile sono visualizzati in MS Word, alcune grafiche possono essere scalate in base alle dimensioni effettive del metafile in pixel. Cioè, anche lo zoom può influire sulla visualizzazione del metafile.

Quando questo valore è impostato su **true**, Aspose.Words emula il rendering in base alle dimensioni del metafile sulla pagina. Le dimensioni in pixel sono calcolate dalle dimensioni del metafile sulla pagina e dalla [EmulateRenderingToSizeOnPageResolution](../get_emulaterenderingtosizeonpageresolution/) specificata.

Quando questo valore è impostato su **false**, Aspose.Words emula il rendering del metafile nella sua dimensione predefinita in pixel.

Questa opzione è usata solo quando il metafile viene renderizzato come grafica vettoriale.

Il valore predefinito è **true**.
## Vedi anche

* Class [MetafileRenderingOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
