---
title: Style.IsHeading
second_title: Referencia de API de Aspose.Words para .NET
description: Style propiedad. Verdadero cuando el estilo es uno de los estilos de título integrados.
type: docs
weight: 70
url: /es/net/aspose.words/style/isheading/
---
## Style.IsHeading property

Verdadero cuando el estilo es uno de los estilos de título integrados.

```csharp
public bool IsHeading { get; }
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

* class [Style](../)
* espacio de nombres [Aspose.Words](../../style/)
* asamblea [Aspose.Words](../../../)


