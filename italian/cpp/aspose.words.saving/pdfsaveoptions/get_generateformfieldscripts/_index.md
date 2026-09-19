---
title: "Aspose::Words::Saving::PdfSaveOptions::get_GenerateFormFieldScripts metodo"
linktitle: "get_GenerateFormFieldScripts"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Saving::PdfSaveOptions::get_GenerateFormFieldScripts. Specifica se generare script che emulano il comportamento specifico dei campi modulo di Microsoft Word in PDF. Il valore predefinito è false in C++."
type: docs
weight: 18500
url: /it/cpp/aspose.words.saving/pdfsaveoptions/get_generateformfieldscripts/
---
## PdfSaveOptions::get_GenerateFormFieldScripts method


Specifica se generare script che emulano il comportamento specifico dei campi modulo di Microsoft Word nel PDF. Il valore predefinito è **false**.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_GenerateFormFieldScripts() const
```

## Note


Quando questa opzione è abilitata, l'esportatore genera azioni JavaScript PDF per emulare il comportamento dei campi modulo di Microsoft Word, come i campi data e ora con formattazione e regole di convalida.

Quando impostato su **true**, il comportamento supportato verrà esportato come azioni JavaScript PDF. Quando impostato su **false**, non verranno generati script per i campi modulo.

L'esecuzione degli script dipende dal visualizzatore PDF. Alcuni visualizzatori PDF potrebbero ignorare gli script, limitare l'esecuzione degli script o richiedere all'utente di abilitare JavaScript.

Le azioni JavaScript sono vietate dalla conformità PDF/A-1, PDF/A-2 e PDF/A-3. Il valore **false** verrà utilizzato automaticamente in questo caso.
## Vedi anche

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
