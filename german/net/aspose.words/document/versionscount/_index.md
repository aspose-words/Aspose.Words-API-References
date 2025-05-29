---
title: Document.VersionsCount
linktitle: VersionsCount
articleTitle: VersionsCount
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „Document VersionsCount“, um die Anzahl der gespeicherten Dokumentversionen in Ihren DOC-Dateien einfach zu verfolgen und so die Verwaltung und Organisation zu verbessern.
type: docs
weight: 480
url: /de/net/aspose.words/document/versionscount/
---
## Document.VersionsCount property

Ruft die Anzahl der Dokumentversionen ab, die im DOC-Dokument gespeichert wurden.

```csharp
public int VersionsCount { get; }
```

## Bemerkungen

Der Zugriff auf Versionen in Microsoft Word erfolgt über das Menü „Datei“ &gt; „Versionen“. Microsoft Word unterstützt -Versionen nur für DOC-Dateien.

Mit dieser Eigenschaft lässt sich feststellen, ob in diesem Dokument Dokumentversionen gespeichert waren, bevor es in Aspose.Words geöffnet wurde. Aspose.Words bietet keine weitere Unterstützung für Dokumentversionen. Wenn Sie dieses Dokument mit Aspose.Words speichern, wird das Dokument ohne Versionen gespeichert.

## Beispiele

Zeigt, wie Sie mit der Versionszählfunktion älterer Microsoft Word-Dokumente arbeiten.

```csharp
Document doc = new Document(MyDir + "Versions.doc");

// Wir können diese Eigenschaft eines Dokuments lesen, aber beim Speichern nicht beibehalten.
Assert.AreEqual(4, doc.VersionsCount);

doc.Save(ArtifactsDir + "Document.VersionsCount.doc");
doc = new Document(ArtifactsDir + "Document.VersionsCount.doc");

Assert.AreEqual(0, doc.VersionsCount);
```

### Siehe auch

* class [Document](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
