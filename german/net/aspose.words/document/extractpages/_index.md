---
title: Document.ExtractPages
linktitle: ExtractPages
articleTitle: ExtractPages
second_title: Aspose.Words für .NET
description: Entdecken Sie die Methode „Document ExtractPages“, um mühelos bestimmte Seitenbereiche abzurufen und so Ihre Dokumentenverwaltung und Effizienz zu verbessern.
type: docs
weight: 640
url: /de/net/aspose.words/document/extractpages/
---
## Document.ExtractPages method

Gibt die[`Document`](../) Objekt, das den angegebenen Seitenbereich darstellt.

```csharp
public Document ExtractPages(int index, int count)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| index | Int32 | Der nullbasierte Index der ersten zu extrahierenden Seite. |
| count | Int32 | Anzahl der zu extrahierenden Seiten. |

## Bemerkungen

Das resultierende Dokument sollte wie das in MS Word aussehen, als hätten wir „Bestimmte Seiten drucken“ ausgeführt – die Nummerierung, Kopf-/Fußzeilen und das Layout der Kreuztabellen bleiben erhalten. Aufgrund der Vielzahl von Nuancen, die bei der Reduzierung der Seitenzahl auftreten, ist die vollständige Anpassung des Layouts jedoch eine ziemlich komplizierte Aufgabe, die viel Aufwand erfordert. Je nach Komplexität des Dokuments kann es leichte Unterschiede im Layout des resultierenden Dokumentinhalts im Vergleich zum Quelldokument geben. Für jedes Feedback sind wir sehr dankbar.

## Beispiele

Zeigt, wie ein bestimmter Seitenbereich aus dem Dokument abgerufen wird.

```csharp
Document doc = new Document(MyDir + "Layout entities.docx");

doc = doc.ExtractPages(0, 2);

doc.Save(ArtifactsDir + "Document.ExtractPages.docx");
```

### Siehe auch

* class [Document](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
