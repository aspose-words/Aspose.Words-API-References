---
title: Style.Styles
second_title: Referencia de API de Aspose.Words para .NET
description: Style propiedad. Obtiene la colección de estilos a la que pertenece este estilo.
type: docs
weight: 170
url: /es/net/aspose.words/style/styles/
---
## Style.Styles property

Obtiene la colección de estilos a la que pertenece este estilo.

```csharp
public StyleCollection Styles { get; }
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

* class [StyleCollection](../../stylecollection/)
* class [Style](../)
* espacio de nombres [Aspose.Words](../../style/)
* asamblea [Aspose.Words](../../../)


