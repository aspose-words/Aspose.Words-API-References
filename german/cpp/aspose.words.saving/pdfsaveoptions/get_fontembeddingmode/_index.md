---
title: "Aspose::Words::Saving::PdfSaveOptions::get_FontEmbeddingMode Methode"
linktitle: "get_FontEmbeddingMode"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::PdfSaveOptions::get_FontEmbeddingMode Methode. Gibt den Schriftart-Einbettungsmodus in C++ an."
type: docs
weight: 18000
url: /de/cpp/aspose.words.saving/pdfsaveoptions/get_fontembeddingmode/
---
## PdfSaveOptions::get_FontEmbeddingMode method


Gibt den Schriftart‑Einbettungsmodus an.

```cpp
Aspose::Words::Saving::PdfFontEmbeddingMode Aspose::Words::Saving::PdfSaveOptions::get_FontEmbeddingMode() const
```

## Hinweise


Der Standardwert ist [EmbedAll](../../pdffontembeddingmode/).

Diese Einstellung funktioniert nur für Text in ANSI (Windows‑1252)-Kodierung. Enthält das Dokument nicht‑ANSI‑Text, werden die entsprechenden Schriftarten unabhängig von dieser Einstellung eingebettet.

PDF/A- und PDF/UA-Konformität erfordert, dass alle Schriftarten eingebettet werden. Der Wert [EmbedAll](../../pdffontembeddingmode/) wird beim Speichern als PDF/A oder PDF/UA automatisch verwendet.
## Siehe auch

* Enum [PdfFontEmbeddingMode](../../pdffontembeddingmode/)
* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
