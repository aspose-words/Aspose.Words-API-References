---
title: DigitalSignatureCollection.GetEnumerator
linktitle: GetEnumerator
articleTitle: GetEnumerator
second_title: Aspose.Words för .NET
description: DigitalSignatureCollection GetEnumerator metod. Returnerar ett ordboksuppräkningsobjekt som kan användas för att iterera över alla objekt i samlingen i C#.
type: docs
weight: 50
url: /sv/net/aspose.words.digitalsignatures/digitalsignaturecollection/getenumerator/
---
## DigitalSignatureCollection.GetEnumerator method

Returnerar ett ordboksuppräkningsobjekt som kan användas för att iterera över alla objekt i samlingen.

```csharp
public IEnumerator<DigitalSignature> GetEnumerator()
```

## Exempel

Visar hur man skriver ut alla digitala signaturer för ett signerat dokument.

```csharp
DigitalSignatureCollection digitalSignatures =
    DigitalSignatureUtil.LoadSignatures(MyDir + "Digitally signed.docx");

using (IEnumerator<DigitalSignature> enumerator = digitalSignatures.GetEnumerator())
{
    while (enumerator.MoveNext())
    {
        DigitalSignature ds = enumerator.Current;

        if (ds != null)
            Console.WriteLine(ds.ToString());
    }
}
```

### Se även

* class [DigitalSignature](../../digitalsignature/)
* class [DigitalSignatureCollection](../)
* namnutrymme [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* hopsättning [Aspose.Words](../../../)
