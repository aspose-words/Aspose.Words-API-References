---
title: StyleCollection.GetEnumerator
second_title: Referencia de API de Aspose.Words para .NET
description: StyleCollection método. Obtiene un objeto enumerador que enumerará los estilos en el orden alfabético de sus nombres.
type: docs
weight: 90
url: /es/net/aspose.words/stylecollection/getenumerator/
---
## StyleCollection.GetEnumerator method

Obtiene un objeto enumerador que enumerará los estilos en el orden alfabético de sus nombres.

```csharp
public IEnumerator<Style> GetEnumerator()
```

### Ejemplos

Muestra cómo acceder a la colección de estilos de un documento.

```csharp
Document doc = new Document();

Assert.AreEqual(4, doc.Styles.Count);

// Enumerar y enumerar todos los estilos que contiene de forma predeterminada un documento creado con Aspose.Words.
using (IEnumerator<Style> stylesEnum = doc.Styles.GetEnumerator())
{
    while (stylesEnum.MoveNext())
    {
        Style curStyle = stylesEnum.Current;
        Console.WriteLine($"Style name:\t\"{curStyle.Name}\", of type \"{curStyle.Type}\"");
        Console.WriteLine($"\tSubsequent style:\t{curStyle.NextParagraphStyleName}");
        Console.WriteLine($"\tIs heading:\t\t\t{curStyle.IsHeading}");
        Console.WriteLine($"\tIs QuickStyle:\t\t{curStyle.IsQuickStyle}");

        Assert.AreEqual(doc, curStyle.Document);
    }
}
```

### Ver también

* class [Style](../../style/)
* class [StyleCollection](../)
* espacio de nombres [Aspose.Words](../../stylecollection/)
* asamblea [Aspose.Words](../../../)


