---
title: "Aspose::Words::Saving::DocumentPartSavingArgs::get_DocumentPartFileName Methode"
linktitle: "get_DocumentPartFileName"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::DocumentPartSavingArgs::get_DocumentPartFileName Methode. Gibt den Dateinamen (ohne Pfad) zurück oder legt ihn fest, unter dem der Dokumentteil in C++ gespeichert wird."
type: docs
weight: 3000
url: /de/cpp/aspose.words.saving/documentpartsavingargs/get_documentpartfilename/
---
## DocumentPartSavingArgs::get_DocumentPartFileName method


Liest oder setzt den Dateinamen (ohne Pfad), in dem der Dokumentteil gespeichert wird.

```cpp
System::String Aspose::Words::Saving::DocumentPartSavingArgs::get_DocumentPartFileName() const
```

## Hinweise


Diese Eigenschaft ermöglicht es Ihnen, die Art und Weise neu zu definieren, wie die Dateinamen von Dokumentteilen beim Export nach HTML oder EPUB erzeugt werden.

Wenn der Rückruf aufgerufen wird, enthält diese Eigenschaft den von Aspose.Words erzeugten Dateinamen. Sie können den Wert dieser Eigenschaft ändern, um den Dokumentteil in einer anderen Datei zu speichern. Beachten Sie, dass der Dateiname für jeden Teil eindeutig sein muss.

[DocumentPartFileName](./) must contain only the file name without the path. Aspose.Words determines the path for saving using the document file name. If output document file name was not specified, for instance when saving to a stream, this file name is used only for referencing document parts. The same is true when saving to EPUB format.

## Siehe auch

* Class [DocumentPartSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
