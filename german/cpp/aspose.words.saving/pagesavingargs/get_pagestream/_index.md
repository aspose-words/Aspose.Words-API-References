---
title: "Aspose::Words::Saving::PageSavingArgs::get_PageStream Methode"
linktitle: "get_PageStream"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::PageSavingArgs::get_PageStream-Methode. Ermöglicht das Angeben des Streams, in dem die Dokumentenseite in C++ gespeichert wird."
type: docs
weight: 6000
url: /de/cpp/aspose.words.saving/pagesavingargs/get_pagestream/
---
## PageSavingArgs::get_PageStream method


Ermöglicht die Angabe des Streams, in dem die Dokumentenseite gespeichert wird.

```cpp
System::SharedPtr<System::IO::Stream> Aspose::Words::Saving::PageSavingArgs::get_PageStream() const
```

## Hinweise


Diese Eigenschaft ermöglicht es Ihnen, Dokumentenseiten in Streams statt in Dateien zu speichern.

Der Standardwert ist **null**. Wenn diese Eigenschaft **null** ist, wird die Dokumentenseite in einer Datei gespeichert, die in der [PageFileName](../get_pagefilename/)-Eigenschaft angegeben ist.

Wenn sowohl [PageStream](./) als auch [PageFileName](../get_pagefilename/) festgelegt sind, wird PageStream verwendet.

## Siehe auch

* Class [PageSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
