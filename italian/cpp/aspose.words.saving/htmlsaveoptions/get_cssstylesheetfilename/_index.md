---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_CssStyleSheetFileName metodo"
linktitle: "get_CssStyleSheetFileName"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_CssStyleSheetFileName metodo. Specifica il percorso e il nome del file Cascading Style Sheet (CSS) scritto quando un documento viene esportato in HTML. Il valore predefinito è una stringa vuota in C++."
type: docs
weight: 6000
url: /it/cpp/aspose.words.saving/htmlsaveoptions/get_cssstylesheetfilename/
---
## HtmlSaveOptions::get_CssStyleSheetFileName method


Specifica il percorso e il nome del file Cascading [Style](../../../aspose.words/style/) Sheet (CSS) scritto quando un documento viene esportato in HTML. Il valore predefinito è una stringa vuota.

```cpp
System::String Aspose::Words::Saving::HtmlSaveOptions::get_CssStyleSheetFileName() const
```

## Note


Questa proprietà ha effetto solo quando si salva un documento in formato HTML e viene richiesto un foglio di stile CSS esterno utilizzando [CssStyleSheetType](../get_cssstylesheettype/).

Se questa proprietà è vuota, il file CSS verrà salvato nella stessa cartella e con lo stesso nome del documento HTML ma con l'estensione ".css".

Se in questa proprietà è specificato solo il percorso ma nessun nome file, il file CSS verrà salvato nella cartella specificata e avrà lo stesso nome del documento HTML ma con l'estensione ".css".

Se la cartella specificata da questa proprietà non esiste, verrà creata automaticamente prima di salvare il file CSS.

Un altro modo per specificare una cartella in cui salvare il file CSS esterno è utilizzare [ResourceFolder](../get_resourcefolder/).

## Vedi anche

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
