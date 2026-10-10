---
title: "Aspose::Words::Saving::CssSavingArgs::get_CssStream Methode"
linktitle: "get_CssStream"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::CssSavingArgs::get_CssStream Methode. Ermöglicht die Angabe des Streams, in dem die CSS‑Informationen in C++ gespeichert werden."
type: docs
weight: 2000
url: /de/cpp/aspose.words.saving/csssavingargs/get_cssstream/
---
## CssSavingArgs::get_CssStream method


Ermöglicht das Angeben des Streams, in dem die CSS-Informationen gespeichert werden.

```cpp
System::SharedPtr<System::IO::Stream> Aspose::Words::Saving::CssSavingArgs::get_CssStream() const
```

## Hinweise


Diese Eigenschaft ermöglicht es Ihnen, CSS‑Informationen in einen Stream zu speichern.

Der Standardwert ist **null**. Diese Eigenschaft verhindert nicht das Speichern von CSS‑Informationen in einer Datei oder das Einbetten in ein HTML‑Dokument. Um den CSS‑Export zu unterdrücken, verwenden Sie die [IsExportNeeded](../get_isexportneeded/)‑Eigenschaft.

Mit [ICssSavingCallback](../../icsssavingcallback/) können Sie CSS nicht durch ein anderes ersetzen. Es ist ausschließlich zum Speichern von CSS in einen Stream gedacht.

## Siehe auch

* Class [CssSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
