---
title: Document.ExtractPages
second_title: Aspose.Words für .NET-API-Referenz
description: Document methode. Gibt die zurückDocument Objekt das den angegebenen Seitenbereich darstellt.
type: docs
weight: 620
url: /de/net/aspose.words/document/extractpages/
---
## Document.ExtractPages method

Gibt die zurück[`Document`](../) Objekt, das den angegebenen Seitenbereich darstellt.

```csharp
public Document ExtractPages(int index, int count)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| index | Int32 | Der nullbasierte Index der ersten zu extrahierenden Seite. |
| count | Int32 | Anzahl der zu extrahierenden Seiten. |

### Bemerkungen

Das resultierende Dokument sollte wie das in MS Word aussehen, als ob wir „Bestimmte Seiten drucken“ ausgeführt hätten – die Nummerierung, Kopf-/Fußzeilen und das Layout der Kreuztabellen bleiben erhalten. Aber aufgrund einer großen Anzahl von Nuancen, die angezeigt werden Während die Anzahl der Seiten reduziert wird, ist die vollständige Anpassung des Layouts eine ziemlich komplizierte Aufgabe, die viel Aufwand erfordert. Abhängig von der Komplexität des Dokuments kann es zu geringfügigen Unterschieden im resultierenden Layout des Dokumentinhalts im Vergleich zum Quelldokument kommen. Wir würden uns über Feedback freuen Ich bin sehr dankbar.

### Beispiele

Zeigt, wie ein bestimmter Seitenbereich aus dem Dokument abgerufen wird.

```csharp
Document doc = new Document(MyDir + "Layout entities.docx");

doc = doc.ExtractPages(0, 2);

doc.Save(ArtifactsDir + "Document.ExtractPages.docx");
```

### Siehe auch

* class [Document](../)
* namensraum [Aspose.Words](../../document/)
* Montage [Aspose.Words](../../../)


