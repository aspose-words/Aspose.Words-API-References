---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_CssStyleSheetFileName Methode"
linktitle: "get_CssStyleSheetFileName"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_CssStyleSheetFileName Methode. Gibt den Pfad und den Namen der Cascading Style Sheet (CSS)‑Datei an, die beim Export eines Dokuments nach HTML geschrieben wird. Der Standardwert ist eine leere Zeichenkette in C++."
type: docs
weight: 6000
url: /de/cpp/aspose.words.saving/htmlsaveoptions/get_cssstylesheetfilename/
---
## HtmlSaveOptions::get_CssStyleSheetFileName method


Gibt den Pfad und den Namen des Cascading‑[Style](../../../aspose.words/style/)‑Sheets (CSS) an, das beim Export eines Dokuments nach HTML geschrieben wird. Der Standardwert ist eine leere Zeichenkette.

```cpp
System::String Aspose::Words::Saving::HtmlSaveOptions::get_CssStyleSheetFileName() const
```

## Hinweise


Diese Eigenschaft hat nur Wirkung, wenn ein Dokument im HTML‑Format gespeichert wird und ein externes CSS‑Stylesheet über [CssStyleSheetType](../get_cssstylesheettype/) angefordert wird.

Ist diese Eigenschaft leer, wird die CSS‑Datei im selben Ordner und mit demselben Namen wie das HTML‑Dokument, jedoch mit der Erweiterung ".css" gespeichert.

Wenn nur ein Pfad, aber kein Dateiname in dieser Eigenschaft angegeben ist, wird die CSS‑Datei im angegebenen Ordner gespeichert und trägt denselben Namen wie das HTML‑Dokument, jedoch mit der Erweiterung ".css".

Falls der durch diese Eigenschaft angegebene Ordner nicht existiert, wird er automatisch erstellt, bevor die CSS‑Datei gespeichert wird.

Eine weitere Möglichkeit, einen Ordner anzugeben, in dem die externe CSS‑Datei gespeichert wird, besteht darin, [ResourceFolder](../get_resourcefolder/) zu verwenden.

## Siehe auch

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
