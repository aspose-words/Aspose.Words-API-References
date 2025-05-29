---
title: TxtLoadOptions
linktitle: TxtLoadOptions
articleTitle: TxtLoadOptions
second_title: Aspose.Words para .NET
description: ¡Descubre el constructor TxtLoadOptions! Inicialízalo fácilmente con valores predeterminados y optimiza tu proceso de carga de datos para un rendimiento mejorado.
type: docs
weight: 10
url: /es/net/aspose.words.loading/txtloadoptions/txtloadoptions/
---
## TxtLoadOptions constructor

Inicializa una nueva instancia de esta clase con valores predeterminados.

```csharp
public TxtLoadOptions()
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
