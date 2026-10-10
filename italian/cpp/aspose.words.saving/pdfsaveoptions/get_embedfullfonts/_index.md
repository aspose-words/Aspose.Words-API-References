---
title: "Aspose::Words::Saving::PdfSaveOptions::get_EmbedFullFonts metodo"
linktitle: "get_EmbedFullFonts"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::PdfSaveOptions::get_EmbedFullFonts metodo. Controlla come i caratteri vengono incorporati nei documenti PDF risultanti in C++."
type: docs
weight: 14000
url: /it/cpp/aspose.words.saving/pdfsaveoptions/get_embedfullfonts/
---
## PdfSaveOptions::get_EmbedFullFonts method


Controlla come i caratteri vengono incorporati nei documenti PDF risultanti.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_EmbedFullFonts() const
```

## Note


Il valore predefinito è **false**, il che significa che i caratteri vengono sottocampionati prima dell'incorporamento. Il sottocampionamento è utile se si desidera mantenere più piccolo il file di output. Il sottocampionamento rimuove tutti i glifi non utilizzati da un carattere.

Quando questo valore è impostato su **true**, un file di carattere completo viene incorporato nel PDF senza sottocampionamento. Ciò comporterà file di output più grandi, ma può essere un'opzione utile quando si desidera modificare il PDF risultante in seguito (ad es. aggiungere più testo).

Alcuni caratteri sono grandi (diversi megabyte) e incorporarli senza sottocampionamento produrrà documenti di output di grandi dimensioni.
## Vedi anche

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
