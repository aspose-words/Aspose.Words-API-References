---
title: DigitalSignatureCollection.GetEnumerator
linktitle: GetEnumerator
articleTitle: GetEnumerator
second_title: .NET için Aspose.Words
description: Tüm koleksiyon öğeleri arasında kullanışlı bir sözlük numaralandırıcısı ile kolayca yineleme yapmak için DigitalSignatureCollection GetEnumerator yöntemini keşfedin.
type: docs
weight: 50
url: /tr/net/aspose.words.digitalsignatures/digitalsignaturecollection/getenumerator/
---
## DigitalSignatureCollection.GetEnumerator method

Koleksiyondaki tüm öğeler üzerinde yineleme yapmak için kullanılabilen bir sözlük numaralandırıcı nesnesi döndürür.

```csharp
public IEnumerator<DigitalSignature> GetEnumerator()
```

## Örnekler

İmzalanmış bir belgenin tüm dijital imzalarının nasıl yazdırılacağını gösterir.

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

### Ayrıca bakınız

* class [DigitalSignature](../../digitalsignature/)
* class [DigitalSignatureCollection](../)
* ad alanı [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* toplantı [Aspose.Words](../../../)
