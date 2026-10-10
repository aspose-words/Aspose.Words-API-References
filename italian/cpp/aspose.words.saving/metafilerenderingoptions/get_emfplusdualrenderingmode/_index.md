---
title: "Metodo Aspose::Words::Saving::MetafileRenderingOptions::get_EmfPlusDualRenderingMode"
linktitle: "get_EmfPlusDualRenderingMode"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Saving::MetafileRenderingOptions::get_EmfPlusDualRenderingMode. Ottiene o imposta un valore che determina come i metafili EMF+ Dual devono essere renderizzati in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words.saving/metafilerenderingoptions/get_emfplusdualrenderingmode/
---
## MetafileRenderingOptions::get_EmfPlusDualRenderingMode method


Ottiene o imposta un valore che determina come devono essere renderizzati i metafile EMF+ Dual.

```cpp
Aspose::Words::Saving::EmfPlusDualRenderingMode Aspose::Words::Saving::MetafileRenderingOptions::get_EmfPlusDualRenderingMode() const
```

## Note


I metafili EMF+ Dual contengono sia parti EMF+ sia parti EMF. MS Word e GDI+ rendono sempre la parte EMF+. Aspose.Words attualmente non supporta completamente tutti i record EMF+ e in alcuni casi il risultato del rendering della parte EMF appare migliore rispetto al risultato del rendering della parte EMF+.

Questa opzione è utilizzata solo quando il metafile viene renderizzato come grafica vettoriale. Quando il metafile viene renderizzato in bitmap, la parte EMF+ è sempre utilizzata.

Il valore predefinito è [EmfPlusWithFallback](../../emfplusdualrenderingmode/).
## Vedi anche

* Enum [EmfPlusDualRenderingMode](../../emfplusdualrenderingmode/)
* Class [MetafileRenderingOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
