---
title: "Metodo Aspose::Words::Saving::PdfSaveOptions::get_UseCoreFonts"
linktitle: "get_UseCoreFonts"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Saving::PdfSaveOptions::get_UseCoreFonts. Ottiene o imposta un valore che determina se sostituire o meno i font TrueType Arial, Times New Roman, Courier New e Symbol con i font PDF Type 1 di base in C++."
type: docs
weight: 32000
url: /it/cpp/aspose.words.saving/pdfsaveoptions/get_usecorefonts/
---
## PdfSaveOptions::get_UseCoreFonts method


Ottiene o imposta un valore che determina se sostituire o meno i font TrueType Arial, Times New Roman, Courier New e Symbol con i font PDF Type 1 di base.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_UseCoreFonts() const
```

## Note


Il valore predefinito è **false**. Quando questo valore è impostato a **true**, i font Arial, Times New Roman, Courier New e Symbol vengono sostituiti nel documento PDF con il corrispondente font Type 1 di base.

I font PDF di base, o le loro metriche e i font di sostituzione appropriati, devono essere disponibili per qualsiasi applicazione di visualizzazione PDF.

Questa impostazione funziona solo per il testo codificato in ANSI (Windows-1252). Il testo non ANSI verrà scritto con font TrueType incorporato indipendentemente da questa impostazione.

La conformità a PDF/A e PDF/UA richiede che tutti i font siano incorporati. Il valore **false** verrà usato automaticamente durante il salvataggio in PDF/A e PDF/UA.

I font di base non sono supportati durante il salvataggio nel formato PDF 2.0. Il valore **false** verrà usato automaticamente durante il salvataggio in PDF 2.0.

Questa opzione ha una priorità più alta rispetto all'opzione [FontEmbeddingMode](../get_fontembeddingmode/).
## Vedi anche

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
