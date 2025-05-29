---
title: DigitalSignatureCollection.GetEnumerator
linktitle: GetEnumerator
articleTitle: GetEnumerator
second_title: Aspose.Words para .NET
description: Explore el método GetEnumerator de DigitalSignatureCollection para iterar fácilmente a través de todos los elementos de la colección con un enumerador de diccionario conveniente.
type: docs
weight: 50
url: /es/net/aspose.words.digitalsignatures/digitalsignaturecollection/getenumerator/
---
## DigitalSignatureCollection.GetEnumerator method

Devuelve un objeto enumerador de diccionario que se puede utilizar para iterar sobre todos los elementos de la colección.

```csharp
public IEnumerator<DigitalSignature> GetEnumerator()
```

## Ejemplos

Muestra cómo imprimir todas las firmas digitales de un documento firmado.

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

### Ver también

* class [DigitalSignature](../../digitalsignature/)
* class [DigitalSignatureCollection](../)
* espacio de nombres [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* asamblea [Aspose.Words](../../../)
