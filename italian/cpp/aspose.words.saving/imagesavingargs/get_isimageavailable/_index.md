---
title: "Metodo Aspose::Words::Saving::ImageSavingArgs::get_IsImageAvailable"
linktitle: "get_IsImageAvailable"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Saving::ImageSavingArgs::get_IsImageAvailable. Restituisce true se l'immagine corrente è disponibile per l'esportazione in C++."
type: docs
weight: 6000
url: /it/cpp/aspose.words.saving/imagesavingargs/get_isimageavailable/
---
## ImageSavingArgs::get_IsImageAvailable method


Restituisce **true** se l'immagine corrente è disponibile per l'esportazione.

```cpp
bool Aspose::Words::Saving::ImageSavingArgs::get_IsImageAvailable() const
```

## Note


Alcune immagini nel documento possono non essere disponibili, ad esempio perché l'immagine è collegata e il collegamento è inaccessibile o non punta a un'immagine valida. In questo caso Aspose.Words esporta un'icona con una croce rossa. Questa proprietà restituisce **true** se l'immagine originale è disponibile; restituisce **false** se l'immagine originale non è disponibile e verrà offerta un'icona \"nessuna immagine\" per il salvataggio.

Durante il salvataggio di una forma di gruppo o di una forma che non richiede alcuna immagine, questa proprietà è sempre **true**.

## Vedi anche

* Class [ImageSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
