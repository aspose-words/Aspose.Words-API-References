---
title: "Aspose::Words::Document::get_VersionsCount-Methode"
linktitle: "get_VersionsCount"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Document::get_VersionsCount-Methode. Gibt die Anzahl der Dokumentversionen zurück, die im DOC-Dokument in C++ gespeichert wurden."
type: docs
weight: 57000
url: /de/cpp/aspose.words/document/get_versionscount/
---
## Document::get_VersionsCount method


Liest die Anzahl der Dokumentversionen, die im DOC‑Dokument gespeichert wurden.

```cpp
int32_t Aspose::Words::Document::get_VersionsCount()
```

## Hinweise


Versionen in Microsoft Word werden über das Menü Datei/Versionen aufgerufen. Microsoft Word unterstützt Versionen nur für DOC-Dateien.

Diese Eigenschaft ermöglicht zu erkennen, ob Dokumentversionen in diesem Dokument gespeichert waren, bevor es in Aspose.Words geöffnet wurde. Aspose.Words bietet keine weitere Unterstützung für Dokumentversionen. Wenn Sie dieses Dokument mit Aspose.Words speichern, wird es ohne Versionen gespeichert.

## Beispiele



Zeigt, wie man mit der Versionszählfunktion älterer Microsoft Word-Dokumente arbeitet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Versions.doc");

// Wir können diese Eigenschaft eines Dokuments lesen, aber sie beim Speichern nicht erhalten.
ASSERT_EQ(4, doc->get_VersionsCount());

doc->Save(get_ArtifactsDir() + u"Document.VersionsCount.doc");
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Document.VersionsCount.doc");

ASSERT_EQ(0, doc->get_VersionsCount());
```

## Siehe auch

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
