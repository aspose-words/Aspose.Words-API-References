---
title: DigitalSignatureCollection.GetEnumerator
linktitle: GetEnumerator
articleTitle: GetEnumerator
second_title: Aspose.Words per .NET
description: DigitalSignatureCollection GetEnumerator metodo. Restituisce un oggetto enumeratore dizionario che può essere utilizzato per scorrere tutti gli elementi della raccolta in C#.
type: docs
weight: 50
url: /it/net/aspose.words.digitalsignatures/digitalsignaturecollection/getenumerator/
---
## DigitalSignatureCollection.GetEnumerator method

Restituisce un oggetto enumeratore dizionario che può essere utilizzato per scorrere tutti gli elementi della raccolta.

```csharp
public IEnumerator<DigitalSignature> GetEnumerator()
```

## Esempi

Mostra come stampare tutte le firme digitali di un documento firmato.

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

### Guarda anche

* class [DigitalSignature](../../digitalsignature/)
* class [DigitalSignatureCollection](../)
* spazio dei nomi [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* assemblea [Aspose.Words](../../../)
