---
title: "Aspose::Words::Saving::MetafileRenderingOptions::get_EmulateRasterOperations method"
linktitle: "get_EmulateRasterOperations"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::MetafileRenderingOptions::get_EmulateRasterOperations method. Ottiene o imposta un valore che determina se le operazioni raster devono essere emulate in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words.saving/metafilerenderingoptions/get_emulaterasteroperations/
---
## MetafileRenderingOptions::get_EmulateRasterOperations method


Ottiene o imposta un valore che determina se le operazioni raster devono essere emulate.

```cpp
bool Aspose::Words::Saving::MetafileRenderingOptions::get_EmulateRasterOperations() const
```

## Note


Operazioni raster specifiche potrebbero essere usate nei metafile. Non possono essere renderizzate direttamente come grafica vettoriale. L'emulazione delle operazioni raster richiede una rasterizzazione parziale della grafica vettoriale risultante, il che può influire sulle prestazioni del rendering del metafile.

Quando questo valore è impostato su **true**, Aspose.Words emula le operazioni raster. L'output risultante potrebbe essere parzialmente rasterizzato e le prestazioni potrebbero essere più lente.

Quando questo valore è impostato su **false**, Aspose.Words non emula le operazioni raster. Quando [Aspose.Words](../../../aspose.words/) incontra un'operazione raster in un metafile, ricade nel rendering del metafile in una bitmap utilizzando il sistema operativo.

Questa opzione è usata solo quando il metafile viene renderizzato come grafica vettoriale.

Il valore predefinito è **true**.
## Vedi anche

* Class [MetafileRenderingOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
