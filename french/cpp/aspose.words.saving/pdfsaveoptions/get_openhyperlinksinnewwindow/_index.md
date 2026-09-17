---
title: "Aspose::Words::Saving::PdfSaveOptions::get_OpenHyperlinksInNewWindow méthode"
linktitle: "get_OpenHyperlinksInNewWindow"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::PdfSaveOptions::get_OpenHyperlinksInNewWindow méthode. Obtient ou définit une valeur déterminant si les hyperliens dans le document Pdf de sortie sont forcés de s'ouvrir dans une nouvelle fenêtre (ou onglet) du navigateur en C++."
type: docs
weight: 24000
url: /fr/cpp/aspose.words.saving/pdfsaveoptions/get_openhyperlinksinnewwindow/
---
## PdfSaveOptions::get_OpenHyperlinksInNewWindow method


Obtient ou définit une valeur déterminant si les hyperliens dans le document Pdf de sortie sont forcés de s'ouvrir dans une nouvelle fenêtre (ou onglet) du navigateur.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_OpenHyperlinksInNewWindow() const
```

## Remarques


La valeur par défaut est **false**. Lorsque cette valeur est définie sur **true**, les hyperliens sont enregistrés à l'aide du code JavaScript. Le code JavaScript est **app.launchURL(\"URL\", true);**, où **URL** est un hyperlien.

Notez que si cette option est définie sur **true**, les hyperliens ne fonctionnent pas dans certains lecteurs PDF, par exemple Chrome, Firefox.

Les actions JavaScript sont interdites par la conformité PDF/A-1, PDF/A-2 et PDF/A-3. La valeur **false** sera utilisée automatiquement dans ce cas.
## Voir aussi

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
