---
title: "Aspose::Words::Saving::MetafileRenderingMode enum"
linktitle: "MetafileRenderingMode"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::MetafileRenderingMode enum. Specifica come Aspose.Words deve renderizzare i metafili WMF ed EMF in C++."
type: docs
weight: 69000
url: /it/cpp/aspose.words.saving/metafilerenderingmode/
---
## MetafileRenderingMode enum


Specifica come Aspose.Words dovrebbe renderizzare i metafili WMF ed EMF.

```cpp
enum class MetafileRenderingMode
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| VectorWithFallback | 0 | Aspose.Words tenta di renderizzare un metafile come grafica vettoriale. Se Aspose.Words non riesce a renderizzare correttamente alcuni dei record del metafile come grafica vettoriale, allora Aspose.Words renderizza questo metafile in una bitmap. |
| Vector | 1 | Aspose.Words rende un metafile come grafica vettoriale. |
| Bitmap | 2 | Aspose.Words richiama GDI+ per rendere un metafile in un bitmap e quindi salva il bitmap nel documento di output. |

## Vedi anche

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
