---
title: Field.Unlink
linktitle: Unlink
articleTitle: Unlink
second_title: Aspose.Words för .NET
description: Upptäck metoden Field Unlink för att enkelt koppla bort fält, förbättra din datahantering och effektivisera ditt arbetsflöde för optimala resultat.
type: docs
weight: 130
url: /sv/net/aspose.words.fields/field/unlink/
---
## Field.Unlink method

Utför fältavkopplingen.

```csharp
public bool Unlink()
```

### Returvärde

`sann` om fältet har kopplats bort, annars`falsk` .

## Anmärkningar

Ersätter fältet med dess senaste resultat.

Vissa fält, till exempel XE-fält (indexpost) och SEQ-fält (sekvens), kan inte avlänkas.

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
