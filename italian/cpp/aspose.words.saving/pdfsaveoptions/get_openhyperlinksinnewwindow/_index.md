---
title: "Metodo Aspose::Words::Saving::PdfSaveOptions::get_OpenHyperlinksInNewWindow"
linktitle: "get_OpenHyperlinksInNewWindow"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Saving::PdfSaveOptions::get_OpenHyperlinksInNewWindow. Ottiene o imposta un valore che determina se i collegamenti ipertestuali nel documento Pdf di output devono essere forzati ad aprirsi in una nuova finestra (o scheda) del browser in C++."
type: docs
weight: 24000
url: /it/cpp/aspose.words.saving/pdfsaveoptions/get_openhyperlinksinnewwindow/
---
## PdfSaveOptions::get_OpenHyperlinksInNewWindow method


Ottiene o imposta un valore che determina se i collegamenti ipertestuali nel documento Pdf di output devono essere forzati ad aprirsi in una nuova finestra (o scheda) del browser.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_OpenHyperlinksInNewWindow() const
```

## Note


Il valore predefinito è **false**. Quando questo valore è impostato su **true** i collegamenti ipertestuali vengono salvati usando codice JavaScript. Il codice JavaScript è **app.launchURL(\"URL\", true);**, dove **URL** è un collegamento ipertestuale.

Nota che se questa opzione è impostata su **true** i collegamenti ipertestuali potrebbero non funzionare in alcuni lettori PDF, ad es. Chrome, Firefox.

Le azioni JavaScript sono vietate dalla conformità PDF/A-1, PDF/A-2 e PDF/A-3. Il valore **false** verrà utilizzato automaticamente in questo caso.
## Vedi anche

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
