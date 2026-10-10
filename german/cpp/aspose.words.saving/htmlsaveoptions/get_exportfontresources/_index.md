---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportFontResources Methode"
linktitle: "get_ExportFontResources"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportFontResources Methode. Gibt an, ob Schriftressourcen nach HTML, MHTML oder EPUB exportiert werden sollen. Der Standardwert ist false in C++."
type: docs
weight: 16000
url: /de/cpp/aspose.words.saving/htmlsaveoptions/get_exportfontresources/
---
## HtmlSaveOptions::get_ExportFontResources method


Gibt an, ob Schriftartressourcen nach HTML, MHTML oder EPUB exportiert werden sollen. Standardwert ist **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportFontResources() const
```

## Hinweise


Das Exportieren von Schriftartenressourcen ermöglicht eine konsistente Dokumentdarstellung, unabhängig von den in der Umgebung eines bestimmten Benutzers verfügbaren Schriftarten.

Wenn [ExportFontResources](./) auf **true** gesetzt ist, verweist das Haupt‑HTML‑Dokument auf jede Schriftart über die CSS 3 **%@font-face** at‑rule und die Schriftarten werden als separate Dateien ausgegeben. Beim Exportieren in die Formate IDPF EPUB oder MHTML werden die Schriftarten zusammen mit anderen Neben‑Dateien in das entsprechende Paket eingebettet.

Wenn [ExportFontsAsBase64](../get_exportfontsasbase64/) auf **true** gesetzt ist, werden Schriftarten nicht in separate Dateien gespeichert. Stattdessen werden sie in **%@font-face**‑at‑rules im Base64‑Format eingebettet.

**Important!** When exporting font resources, font licensing issues should be considered. Authors who want to use specific fonts via a downloadable font mechanism must always carefully verify that their intended use is within the scope of the font license. Many commercial fonts presently do not allow web downloading of their fonts in any form. [License](../../../aspose.words/license/) agreements that cover some fonts specifically note that usage via **%@font-face** rules in CSS style sheets is not allowed. [Font](../../../aspose.words/font/) subsetting can also violate license terms.

## Siehe auch

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
