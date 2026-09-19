---
title: "Metodo Aspose::Words::Saving::MetafileRenderingOptions::get_UseEmfEmbeddedToWmf"
linktitle: "get_UseEmfEmbeddedToWmf"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Saving::MetafileRenderingOptions::get_UseEmfEmbeddedToWmf. Ottiene o imposta un valore che determina come i metafili WMF con metafili EMF incorporati devono essere renderizzati in C++."
type: docs
weight: 7000
url: /it/cpp/aspose.words.saving/metafilerenderingoptions/get_useemfembeddedtowmf/
---
## MetafileRenderingOptions::get_UseEmfEmbeddedToWmf method


Ottiene o imposta un valore che determina come devono essere renderizzati i metafile WMF con metafile EMF incorporati.

```cpp
bool Aspose::Words::Saving::MetafileRenderingOptions::get_UseEmfEmbeddedToWmf() const
```

## Note


I file WMF potrebbero contenere dati EMF incorporati. MS Word nella maggior parte dei casi utilizza dati EMF incorporati. GDI+ utilizza sempre dati WMF.

Quando questo valore è impostato su **true**, Aspose.Words utilizza dati EMF incorporati durante il rendering.

Quando questo valore è impostato su **false**, Aspose.Words utilizza dati WMF durante il rendering.

Questa opzione è usata solo quando il metafile viene renderizzato come grafica vettoriale. Quando il metafile viene renderizzato in bitmap, i dati WMF sono sempre usati.

Il valore predefinito è **true**.
## Vedi anche

* Class [MetafileRenderingOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
