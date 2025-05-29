---
title: DigitalSignatureCollection.GetEnumerator
linktitle: GetEnumerator
articleTitle: GetEnumerator
second_title: Aspose.Words pour .NET
description: Explorez la méthode GetEnumerator de DigitalSignatureCollection pour parcourir facilement tous les éléments de la collection avec un énumérateur de dictionnaire pratique.
type: docs
weight: 50
url: /fr/net/aspose.words.digitalsignatures/digitalsignaturecollection/getenumerator/
---
## DigitalSignatureCollection.GetEnumerator method

Renvoie un objet énumérateur de dictionnaire qui peut être utilisé pour parcourir tous les éléments de la collection.

```csharp
public IEnumerator<DigitalSignature> GetEnumerator()
```

## Exemples

Montre comment imprimer toutes les signatures numériques d'un document signé.

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

### Voir également

* class [DigitalSignature](../../digitalsignature/)
* class [DigitalSignatureCollection](../)
* espace de noms [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* Assemblée [Aspose.Words](../../../)
