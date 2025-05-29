---
title: TxtLoadOptions.DetectHyperlinks
linktitle: DetectHyperlinks
articleTitle: DetectHyperlinks
second_title: Aspose.Words para .NET
description: Descubra cómo la propiedad DetectHyperlinks de TxtLoadOptions optimiza el procesamiento de texto al detectar hipervínculos, lo que mejora la precisión de los datos. El valor predeterminado es falso.
type: docs
weight: 30
url: /es/net/aspose.words.loading/txtloadoptions/detecthyperlinks/
---
## TxtLoadOptions.DetectHyperlinks property

Especifica si se deben detectar hipervínculos en el texto. El valor predeterminado es`FALSO` .

```csharp
public bool DetectHyperlinks { get; set; }
```

## Ejemplos

Muestra cómo leer y mostrar hipervínculos.

```csharp
const string inputText = "Some links in TXT:\n" +
        "https://www.aspose.com/\n" +
        "https://docs.aspose.com/words/net/\n";

using (Stream stream = new MemoryStream())
{
    byte[] buf = Encoding.ASCII.GetBytes(inputText);
    stream.Write(buf, 0, buf.Length);

    //Cargar documento con hipervínculos.
    Document doc = new Document(stream, new TxtLoadOptions() { DetectHyperlinks = true });

    // Imprimir el texto de los hipervínculos.
    foreach (Field field in doc.Range.Fields)
        Console.WriteLine(field.Result);

    Assert.AreEqual(doc.Range.Fields[0].Result.Trim(), "https://www.aspose.com/");
    Assert.AreEqual(doc.Range.Fields[1].Result.Trim(), "https://docs.aspose.com/words/net/");
}
```

### Ver también

* class [TxtLoadOptions](../)
* espacio de nombres [Aspose.Words.Loading](../../../aspose.words.loading/)
* asamblea [Aspose.Words](../../../)
