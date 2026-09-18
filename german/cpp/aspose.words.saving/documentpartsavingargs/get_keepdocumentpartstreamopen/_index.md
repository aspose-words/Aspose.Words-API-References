---
title: "Aspose::Words::Saving::DocumentPartSavingArgs::get_KeepDocumentPartStreamOpen Methode"
linktitle: "get_KeepDocumentPartStreamOpen"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::DocumentPartSavingArgs::get_KeepDocumentPartStreamOpen Methode. Gibt an, ob Aspose.Words den Stream offen halten oder nach dem Speichern eines Dokumentparts in C++ schließen soll."
type: docs
weight: 5000
url: /de/cpp/aspose.words.saving/documentpartsavingargs/get_keepdocumentpartstreamopen/
---
## DocumentPartSavingArgs::get_KeepDocumentPartStreamOpen method


Gibt an, ob Aspose.Words den Stream nach dem Speichern eines Dokumentteils offen halten oder schließen soll.

```cpp
bool Aspose::Words::Saving::DocumentPartSavingArgs::get_KeepDocumentPartStreamOpen() const
```

## Hinweise


Standard ist **false** und Aspose.Words schließt den Stream, den Sie in der Eigenschaft [DocumentPartStream](../get_documentpartstream/) angegeben haben, nachdem ein Dokumentteil darin geschrieben wurde. Geben Sie **true** an, um den Stream offen zu halten. Bitte beachten Sie, dass der Hauptausgabestream, der beim Aufruf von [Save()](../) oder [Save()](../) bereitgestellt wird, niemals von Aspose.Words geschlossen wird, selbst wenn [KeepDocumentPartStreamOpen](./) auf **false** gesetzt ist.

## Siehe auch

* Class [DocumentPartSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
