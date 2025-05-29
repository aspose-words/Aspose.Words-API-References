---
title: FieldEQ.AsOfficeMath
linktitle: AsOfficeMath
articleTitle: AsOfficeMath
second_title: Aspose.Words för .NET
description: Transformera EQ-fält med FieldEQs AsOfficeMath-metod och konvertera dem enkelt till Office Math-objekt för sömlös dokumentintegration.
type: docs
weight: 20
url: /sv/net/aspose.words.fields/fieldeq/asofficemath/
---
## FieldEQ.AsOfficeMath method

Returnerar Office Math-objektet som motsvarade EQ-fältet.

```csharp
public OfficeMath AsOfficeMath()
```

### Returvärde

Returer`null` om fältkoden är tom eller ogiltig, annars en[`OfficeMath`](../../../aspose.words.math/officemath/) instans.

## Exempel

Visar hur man ersätter EQ-fältet med Office Math.

```csharp
Document doc = new Document(MyDir + "Field sample - EQ.docx");
FieldEQ fieldEQ = doc.Range.Fields.OfType<FieldEQ>().First();

OfficeMath officeMath = fieldEQ.AsOfficeMath();

fieldEQ.Start.ParentNode.InsertBefore(officeMath, fieldEQ.Start);
fieldEQ.Remove();

doc.Save(ArtifactsDir + "Field.EQAsOfficeMath.docx");
```

### Se även

* class [OfficeMath](../../../aspose.words.math/officemath/)
* class [FieldEQ](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
