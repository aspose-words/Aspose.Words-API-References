---
title: Field.Unlink
linktitle: Unlink
articleTitle: Unlink
second_title: Aspose.Words für .NET
description: Entdecken Sie die Methode „Feldverknüpfung aufheben“, um mühelos die Verknüpfung von Feldern aufzuheben, Ihr Datenmanagement zu verbessern und Ihren Arbeitsablauf für optimale Ergebnisse zu optimieren.
type: docs
weight: 130
url: /de/net/aspose.words.fields/field/unlink/
---
## Field.Unlink method

Führt die Feldverknüpfung aus.

```csharp
public bool Unlink()
```

### Rückgabewert

`WAHR` wenn die Verknüpfung des Feldes aufgehoben wurde, andernfalls`FALSCH` .

## Bemerkungen

Ersetzt das Feld durch das aktuellste Ergebnis.

Die Verknüpfung mancher Felder, wie etwa XE-Felder (Indexeintrag) und SEQ-Felder (Sequenz), kann nicht aufgehoben werden.

## Beispiele

Zeigt, wie die Verknüpfung eines Felds aufgehoben wird.

```csharp
Document doc = new Document(MyDir + "Linked fields.docx");
doc.Range.Fields[1].Unlink();
```

### Siehe auch

* class [Field](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
