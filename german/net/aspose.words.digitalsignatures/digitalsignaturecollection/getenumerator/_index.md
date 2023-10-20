---
title: DigitalSignatureCollection.GetEnumerator
linktitle: GetEnumerator
articleTitle: GetEnumerator
second_title: Aspose.Words für .NET
description: DigitalSignatureCollection GetEnumerator methode. Gibt ein WörterbuchEnumeratorobjekt zurück das zum Durchlaufen aller Elemente in der Sammlung verwendet werden kann in C#.
type: docs
weight: 50
url: /de/net/aspose.words.digitalsignatures/digitalsignaturecollection/getenumerator/
---
## DigitalSignatureCollection.GetEnumerator method

Gibt ein Wörterbuch-Enumeratorobjekt zurück, das zum Durchlaufen aller Elemente in der Sammlung verwendet werden kann.

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
