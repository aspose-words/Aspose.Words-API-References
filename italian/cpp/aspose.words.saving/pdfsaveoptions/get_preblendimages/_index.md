---
title: "Aspose::Words::Saving::PdfSaveOptions::get_PreblendImages metodo"
linktitle: "get_PreblendImages"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::PdfSaveOptions::get_PreblendImages metodo. Ottiene o imposta un valore che determina se pre‑mescolare o meno le immagini trasparenti con colore di sfondo nero in C++."
type: docs
weight: 27000
url: /it/cpp/aspose.words.saving/pdfsaveoptions/get_preblendimages/
---
## PdfSaveOptions::get_PreblendImages method


Ottiene o imposta un valore che determina se pre‑mescolare le immagini trasparenti con il colore di sfondo nero.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_PreblendImages() const
```

## Note


Il pre‑mescolare le immagini può migliorare l'aspetto visivo del documento PDF in Adobe Reader e rimuovere gli artefatti di anti‑aliasing.

Per visualizzare correttamente le immagini pre‑mescolate, l'applicazione di visualizzazione PDF deve supportare la voce /Matte nel dizionario delle immagini soft‑mask. Inoltre, il pre‑mescolare le immagini può ridurre le prestazioni di rendering del PDF.

Il valore predefinito è **false**.
## Vedi anche

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
