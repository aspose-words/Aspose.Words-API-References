---
title: FieldEQ.AsOfficeMath
linktitle: AsOfficeMath
articleTitle: AsOfficeMath
second_title: Aspose.Words per .NET
description: Trasforma i campi EQ con il metodo AsOfficeMath di FieldEQ, convertendoli senza sforzo in oggetti Office Math per un'integrazione ottimale dei documenti.
type: docs
weight: 20
url: /it/net/aspose.words.fields/fieldeq/asofficemath/
---
## FieldEQ.AsOfficeMath method

Restituisce l'oggetto Office Math corrispondente al campo EQ.

```csharp
public OfficeMath AsOfficeMath()
```

### Valore di ritorno

Restituisce`null` se il codice campo è vuoto o non valido, altrimenti un[`OfficeMath`](../../../aspose.words.math/officemath/) istanza.

## Esempi

Mostra come sostituire il campo EQ con Office Math.

```csharp
Document doc = new Document(MyDir + "Field sample - EQ.docx");
FieldEQ fieldEQ = doc.Range.Fields.OfType<FieldEQ>().First();

OfficeMath officeMath = fieldEQ.AsOfficeMath();

fieldEQ.Start.ParentNode.InsertBefore(officeMath, fieldEQ.Start);
fieldEQ.Remove();

doc.Save(ArtifactsDir + "Field.EQAsOfficeMath.docx");
```

### Guarda anche

* class [OfficeMath](../../../aspose.words.math/officemath/)
* class [FieldEQ](../)
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
