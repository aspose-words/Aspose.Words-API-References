---
title: "Aspose::Words::Saving::PdfSaveOptions::get_OpenHyperlinksInNewWindow Methode"
linktitle: "get_OpenHyperlinksInNewWindow"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::PdfSaveOptions::get_OpenHyperlinksInNewWindow Methode. Gibt einen Wert zurück oder legt ihn fest, der bestimmt, ob Hyperlinks im ausgegebenen Pdf-Dokument gezwungen werden, in einem neuen Fenster (oder Tab) eines Browsers in C++ geöffnet zu werden."
type: docs
weight: 24000
url: /de/cpp/aspose.words.saving/pdfsaveoptions/get_openhyperlinksinnewwindow/
---
## PdfSaveOptions::get_OpenHyperlinksInNewWindow method


Liest oder legt einen Wert fest, der bestimmt, ob Hyperlinks im Ausgabepdf‑Dokument gezwungen werden, in einem neuen Fenster (oder Tab) des Browsers geöffnet zu werden.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_OpenHyperlinksInNewWindow() const
```

## Hinweise


Der Standardwert ist **false**. Wenn dieser Wert auf **true** gesetzt wird, werden Hyperlinks mit JavaScript‑Code gespeichert. Der JavaScript‑Code lautet **app.launchURL(\"URL\", true);**, wobei **URL** ein Hyperlink ist.

Beachten Sie, dass Hyperlinks, wenn diese Option auf **true** gesetzt ist, in einigen PDF‑Readern, z. B. Chrome, Firefox, nicht funktionieren können.

JavaScript‑Aktionen sind durch die PDF/A‑1-, PDF/A‑2- und PDF/A‑3‑Konformität verboten. Der Wert **false** wird in diesem Fall automatisch verwendet.
## Siehe auch

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
