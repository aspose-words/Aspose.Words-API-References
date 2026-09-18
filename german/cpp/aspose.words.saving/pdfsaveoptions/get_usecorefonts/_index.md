---
title: "Aspose::Words::Saving::PdfSaveOptions::get_UseCoreFonts Methode"
linktitle: "get_UseCoreFonts"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::PdfSaveOptions::get_UseCoreFonts Methode. Ruft einen Wert ab oder legt ihn fest, der bestimmt, ob TrueType‑Schriften Arial, Times New Roman, Courier New und Symbol durch Kern‑PDF‑Type‑1‑Schriften ersetzt werden sollen, in C++."
type: docs
weight: 32000
url: /de/cpp/aspose.words.saving/pdfsaveoptions/get_usecorefonts/
---
## PdfSaveOptions::get_UseCoreFonts method


Liest oder legt einen Wert fest, der bestimmt, ob TrueType-Schriften Arial, Times New Roman, Courier New und Symbol durch Kern-PDF-Type‑1-Schriften ersetzt werden sollen oder nicht.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_UseCoreFonts() const
```

## Hinweise


Der Standardwert ist **false**. Wenn dieser Wert auf **true** gesetzt wird, werden die Schriften Arial, Times New Roman, Courier New und Symbol im PDF‑Dokument durch die entsprechenden Kern‑Type‑1‑Schriften ersetzt.

Kern‑PDF‑Schriften oder deren Schriftmetriken und geeignete Ersatzschriften müssen in jeder PDF‑Betrachter‑Anwendung verfügbar sein.

Diese Einstellung funktioniert nur für Text in ANSI‑Kodierung (Windows‑1252). Nicht‑ANSI‑Text wird unabhängig von dieser Einstellung mit eingebetteter TrueType‑Schrift geschrieben.

PDF/A- und PDF/UA-Konformität erfordert, dass alle Schriftarten eingebettet werden. Der **false**‑Wert wird beim Speichern in PDF/A und PDF/UA automatisch verwendet.

Core-Schriftarten werden beim Speichern im PDF‑2.0‑Format nicht unterstützt. Der **false**‑Wert wird beim Speichern in PDF 2.0 automatisch verwendet.

Diese Option hat eine höhere Priorität als die [FontEmbeddingMode](../get_fontembeddingmode/)-Option.
## Siehe auch

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
