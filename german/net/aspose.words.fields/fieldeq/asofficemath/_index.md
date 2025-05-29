---
title: FieldEQ.AsOfficeMath
linktitle: AsOfficeMath
articleTitle: AsOfficeMath
second_title: Aspose.Words für .NET
description: Transformieren Sie EQ-Felder mit der AsOfficeMath-Methode von FieldEQ und konvertieren Sie sie mühelos in Office Math-Objekte für eine nahtlose Dokumentintegration.
type: docs
weight: 20
url: /de/net/aspose.words.fields/fieldeq/asofficemath/
---
## FieldEQ.AsOfficeMath method

Das Office Math-Objekt von Returns entsprach dem EQ-Feld.

```csharp
public OfficeMath AsOfficeMath()
```

### Rückgabewert

Rückgaben`null` wenn Feldcode leer oder ungültig ist, andernfalls ein[`OfficeMath`](../../../aspose.words.math/officemath/) Instanz.

## Beispiele

Zeigt, wie das EQ-Feld durch Office Math ersetzt wird.

```csharp
Document doc = new Document(MyDir + "Field sample - EQ.docx");
FieldEQ fieldEQ = doc.Range.Fields.OfType<FieldEQ>().First();

OfficeMath officeMath = fieldEQ.AsOfficeMath();

fieldEQ.Start.ParentNode.InsertBefore(officeMath, fieldEQ.Start);
fieldEQ.Remove();

doc.Save(ArtifactsDir + "Field.EQAsOfficeMath.docx");
```

### Siehe auch

* class [OfficeMath](../../../aspose.words.math/officemath/)
* class [FieldEQ](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
