---
title: StyleCollection.GetEnumerator
linktitle: GetEnumerator
articleTitle: GetEnumerator
second_title: Aspose.Words para .NET
description: Descubre el método GetEnumerator de StyleCollection para listar estilos alfabéticamente por nombre sin esfuerzo. ¡Mejora tu eficiencia de codificación hoy mismo!
type: docs
weight: 90
url: /es/net/aspose.words/stylecollection/getenumerator/
---
## StyleCollection.GetEnumerator method

Obtiene un objeto enumerador que enumerará los estilos en el orden alfabético de sus nombres.

```csharp
public IEnumerator<Style> GetEnumerator()
```

## Ejemplos

Muestra cómo acceder a la colección de estilos de un documento.

```csharp
Document doc = new Document();

Assert.AreEqual(4, doc.Styles.Count);

// Enumerar y listar todos los estilos que un documento creado con Aspose.Words contiene de forma predeterminada.
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
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
