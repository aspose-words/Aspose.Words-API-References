---
title: "Aspose::Words::Saving::DocumentPartSavingArgs::get_DocumentPartStream Methode"
linktitle: "get_DocumentPartStream"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::DocumentPartSavingArgs::get_DocumentPartStream Methode. Ermöglicht die Angabe des Streams, in dem der Dokumentteil in C++ gespeichert wird."
type: docs
weight: 4000
url: /de/cpp/aspose.words.saving/documentpartsavingargs/get_documentpartstream/
---
## DocumentPartSavingArgs::get_DocumentPartStream method


Ermöglicht die Angabe des Streams, in dem der Dokumentteil gespeichert wird.

```cpp
System::SharedPtr<System::IO::Stream> Aspose::Words::Saving::DocumentPartSavingArgs::get_DocumentPartStream() const
```

## Hinweise


Diese Eigenschaft ermöglicht es Ihnen, Dokumentteile während des HTML-Exports in Streams anstatt in Dateien zu speichern.

Der Standardwert ist **null**. Wenn diese Eigenschaft **null** ist, wird der Dokumentteil in einer Datei gespeichert, die in der [DocumentPartFileName](../get_documentpartfilename/) Eigenschaft angegeben ist.

Wenn das Speichern in einen Stream im HTML-Format durch [Save()](../) oder [Save()](../) angefordert wird und der erste Dokumentteil gespeichert werden soll, schlägt Aspose.Words hier den vom Aufrufer zunächst übergebenen Hauptausgabestream vor.

Beim Speichern im EPUB-Format, das ein containerbasiertes Format auf HTML-Basis ist, kann [DocumentPartStream](./) nicht angegeben werden, weil alle Unterteile in ein einziges Ausgabepaket gekapselt werden.

## Siehe auch

* Class [DocumentPartSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
