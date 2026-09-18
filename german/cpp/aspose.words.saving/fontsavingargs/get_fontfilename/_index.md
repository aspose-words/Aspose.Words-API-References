---
title: "Aspose::Words::Saving::FontSavingArgs::get_FontFileName Methode"
linktitle: "get_FontFileName"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::FontSavingArgs::get_FontFileName Methode. Ruft den Datenamen (ohne Pfad) ab oder legt ihn fest, unter dem die Schriftart in C++ gespeichert wird."
type: docs
weight: 5000
url: /de/cpp/aspose.words.saving/fontsavingargs/get_fontfilename/
---
## FontSavingArgs::get_FontFileName method


Liest oder setzt den Dateinamen (ohne Pfad), in dem die Schriftart gespeichert wird.

```cpp
System::String Aspose::Words::Saving::FontSavingArgs::get_FontFileName() const
```

## Hinweise


Diese Eigenschaft ermöglicht es Ihnen, die Art und Weise, wie Schriftdateinamen beim Export nach HTML generiert werden, neu zu definieren.

Wenn das Ereignis ausgelöst wird, enthält diese Eigenschaft den von Aspose.Words generierten Datenamen. Sie können den Wert dieser Eigenschaft ändern, um die Schriftart in einer anderen Datei zu speichern. Beachten Sie, dass Datenamen eindeutig sein müssen.

Aspose.Words erzeugt beim Export in das HTML-Format automatisch einen eindeutigen Datenamen für jede eingebettete Schriftart. Wie der Schriftdateiname generiert wird, hängt davon ab, ob Sie das Dokument in einer Datei oder in einem Stream speichern.

Beim Speichern eines Dokuments in einer Datei sieht der generierte Schriftdateiname wie *%<document base file name>.<original file name><optional suffix>.<extension>* aus.

Beim Speichern eines Dokuments in einem Stream sieht der generierte Schriftdateiname wie *Aspose.Words.<document guid>.<original file name><optional suffix>.<extension>* aus.

[FontFileName](./) must contain only the file name without the path. Aspose.Words determines the path for saving using the document file name, the [FontsFolder](../../htmlsaveoptions/get_fontsfolder/) and [FontsFolderAlias](../../htmlsaveoptions/get_fontsfolderalias/) properties.

## Siehe auch

* Class [FontSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
