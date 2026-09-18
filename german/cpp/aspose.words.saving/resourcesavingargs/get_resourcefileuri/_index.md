---
title: "Aspose::Words::Saving::ResourceSavingArgs::get_ResourceFileUri method"
linktitle: "get_ResourceFileUri"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::ResourceSavingArgs::get_ResourceFileUri-Methode. Gibt die Uniform Resource Identifier (URI) zurück oder legt sie fest, die verwendet wird, um die Ressourcendatei aus dem Dokument in C++ zu referenzieren."
type: docs
weight: 5000
url: /de/cpp/aspose.words.saving/resourcesavingargs/get_resourcefileuri/
---
## ResourceSavingArgs::get_ResourceFileUri method


Liest oder setzt den Uniform Resource Identifier (URI), der verwendet wird, um die Ressourcendatei aus dem Dokument zu referenzieren.

```cpp
System::String Aspose::Words::Saving::ResourceSavingArgs::get_ResourceFileUri() const
```

## Hinweise


Diese Eigenschaft ermöglicht es Ihnen, URIs von Ressourcendateien zu ändern, die in feste Seiten‑HTML, SVG‑ oder Markdown‑Dokumente exportiert werden.

Aspose.Words erzeugt beim Export in das feste Seiten‑HTML, SVG‑ oder Markdown‑Format automatisch einen URI für jede Ressourcendatei. Die erzeugten URIs verweisen auf die von Aspose.Words gespeicherten Ressourcendateien. Die URIs können jedoch falsch sein, wenn die Ressourcendateien an einen anderen Ort verschoben werden oder in Streams gespeichert werden. Diese Eigenschaft ermöglicht es, die URIs in diesen Fällen zu korrigieren.

Wenn das Ereignis ausgelöst wird, enthält diese Eigenschaft den von Aspose.Words erzeugten URI. Sie können den Wert dieser Eigenschaft ändern, um einen benutzerdefinierten URI für die Ressourcendatei bereitzustellen.
## Siehe auch

* Class [ResourceSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
