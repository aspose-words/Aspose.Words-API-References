---
title: "Metodo Aspose::Words::Saving::PdfSaveOptions::get_InterpolateImages"
linktitle: "get_InterpolateImages"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Saving::PdfSaveOptions::get_InterpolateImages. Un flag che indica se l'interpolazione delle immagini deve essere eseguita da un lettore conforme. Quando viene specificato **false**, il flag non viene scritto nel documento di output e viene utilizzato il comportamento predefinito del lettore in C++."
type: docs
weight: 22000
url: /it/cpp/aspose.words.saving/pdfsaveoptions/get_interpolateimages/
---
## PdfSaveOptions::get_InterpolateImages method


Un flag che indica se l'interpolazione delle immagini deve essere eseguita da un lettore conforme. Quando viene specificato **false**, il flag non viene scritto nel documento di output e viene utilizzato il comportamento predefinito del lettore.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_InterpolateImages() const
```

## Note


Quando la risoluzione di un'immagine di origine è significativamente inferiore a quella del dispositivo di output, ogni campione di origine copre molti pixel del dispositivo. Di conseguenza, le immagini possono apparire seghettate o a blocchi. Questi artefatti visivi possono essere ridotti applicando un algoritmo di interpolazione delle immagini durante il rendering. Invece di dipingere tutti i pixel coperti da un campione di origine con lo stesso colore, l'interpolazione delle immagini tenta di produrre una transizione fluida tra i valori dei campioni adiacenti.

Un lettore conforme può scegliere di non implementare questa funzionalità del PDF, oppure può utilizzare qualsiasi implementazione specifica di interpolazione desideri.

Il valore predefinito è **false**.

Il flag di interpolazione è vietato dalla conformità PDF/A. Verrà utilizzato automaticamente il valore **false** quando si salva in PDF/A.
## Vedi anche

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
