---
title: Field.Unlink
linktitle: Unlink
articleTitle: Unlink
second_title: Aspose.Words för .NET
description: Field Unlink metod. Utför fältavlänkningen i C#.
type: docs
weight: 130
url: /sv/net/aspose.words.fields/field/unlink/
---
## Field.Unlink method

Utför fältavlänkningen.

```csharp
public bool Unlink()
```

### Returvärde

`Sann` om fältet har tagits bort, annars`falsk` .

## Anmärkningar

Ersätter fältet med det senaste resultatet.

Vissa fält, som XE-fält (Indexinmatning) och SEQ-fält (sekvens), kan inte kopplas bort.

## Exempel

Visar hur man tar bort länken till ett fält.

```csharp
Document doc = new Document(MyDir + "Linked fields.docx");
doc.Range.Fields[1].Unlink();
```

### Se även

* class [Field](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
