---
title: "Aspose::Words::Saving::ResourceSavingArgs::get_ResourceStream-Methode"
linktitle: "get_ResourceStream"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::ResourceSavingArgs::get_ResourceStream-Methode. Ermöglicht die Angabe des Streams, in dem die Ressource in C++ gespeichert wird."
type: docs
weight: 6000
url: /de/cpp/aspose.words.saving/resourcesavingargs/get_resourcestream/
---
## ResourceSavingArgs::get_ResourceStream method


Ermöglicht die Angabe des Streams, in dem die Ressource gespeichert wird.

```cpp
System::SharedPtr<System::IO::Stream> Aspose::Words::Saving::ResourceSavingArgs::get_ResourceStream() const
```

## Hinweise


Diese Eigenschaft ermöglicht es Ihnen, Ressourcen in Streams statt in Dateien zu speichern.

Der Standardwert ist **null**. Wenn diese Eigenschaft **null** ist, wird die Ressource in einer Datei gespeichert, die in der Eigenschaft [ResourceFileName](../get_resourcefilename/) angegeben ist.

Mit [IResourceSavingCallback](../../iresourcesavingcallback/) können Sie eine Ressource nicht durch eine andere ersetzen. Sie dient ausschließlich zur Steuerung des Speicherorts von Ressourcen.

## Siehe auch

* Class [ResourceSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
