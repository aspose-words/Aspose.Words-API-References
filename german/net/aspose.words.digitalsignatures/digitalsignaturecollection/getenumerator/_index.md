---
title: DigitalSignatureCollection.GetEnumerator
linktitle: GetEnumerator
articleTitle: GetEnumerator
second_title: Aspose.Words für .NET
description: Erkunden Sie die GetEnumerator-Methode von DigitalSignatureCollection, um mit einem praktischen Wörterbuch-Enumerator einfach durch alle Sammlungselemente zu iterieren.
type: docs
weight: 50
url: /de/net/aspose.words.digitalsignatures/digitalsignaturecollection/getenumerator/
---
## DigitalSignatureCollection.GetEnumerator method

Gibt ein Wörterbuch-Enumeratorobjekt zurück, mit dem alle Elemente in der Sammlung durchlaufen werden können.

```csharp
public IEnumerator<DigitalSignature> GetEnumerator()
```

## Beispiele

Zeigt, wie alle digitalen Signaturen eines signierten Dokuments gedruckt werden.

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

### Siehe auch

* class [DigitalSignature](../../digitalsignature/)
* class [DigitalSignatureCollection](../)
* namensraum [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* Montage [Aspose.Words](../../../)
