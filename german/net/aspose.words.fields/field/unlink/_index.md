---
title: Field.Unlink
second_title: Aspose.Words für .NET-API-Referenz
description: Field methode. Führt das Feld unlink aus.
type: docs
weight: 130
url: /de/net/aspose.words.fields/field/unlink/
---
## Field.Unlink method

Führt das Feld unlink aus.

```csharp
public bool Unlink()
```

### Rückgabewert

`WAHR` wenn die Verknüpfung des Feldes aufgehoben wurde, andernfalls`FALSCH` .

### Bemerkungen

Ersetzt das Feld durch das aktuellste Ergebnis.

Die Verknüpfung einiger Felder, wie etwa XE-Felder (Indexeintrag) und SEQ-Felder (Sequenz), kann nicht aufgehoben werden.

### Beispiele

Zeigt, wie die Verknüpfung eines Felds aufgehoben wird.

```csharp
Document doc = new Document(MyDir + "Linked fields.docx");
doc.Range.Fields[1].Unlink();
```

### Siehe auch

* class [Field](../)
* namensraum [Aspose.Words.Fields](../../field/)
* Montage [Aspose.Words](../../../)


