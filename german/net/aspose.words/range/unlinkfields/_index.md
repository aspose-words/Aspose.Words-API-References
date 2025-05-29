---
title: Range.UnlinkFields
linktitle: UnlinkFields
articleTitle: UnlinkFields
second_title: Aspose.Words für .NET
description: Entdecken Sie die Methode „Range UnlinkFields“, um mühelos die Verknüpfung von Feldern in Ihrem Dokumentbereich aufzuheben und so Ihren Arbeitsablauf und Ihr Dokumentenmanagement zu verbessern.
type: docs
weight: 120
url: /de/net/aspose.words/range/unlinkfields/
---
## Range.UnlinkFields method

Hebt die Verknüpfung der Felder in diesem Bereich auf.

```csharp
public void UnlinkFields()
```

## Bemerkungen

Ersetzt alle Felder in diesem Bereich durch ihre aktuellsten Ergebnisse.

Um die Verknüpfung von Feldern im gesamten Dokument aufzuheben, verwenden Sie`UnlinkFields`.

## Beispiele

Zeigt, wie die Verknüpfung aller Felder in einem Bereich aufgehoben wird.

```csharp
Document doc = new Document(MyDir + "Linked fields.docx");

Section newSection = (Section)doc.Sections[0].Clone(true);
doc.Sections.Add(newSection);

doc.Sections[1].Range.UnlinkFields();
```

### Siehe auch

* class [Range](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
