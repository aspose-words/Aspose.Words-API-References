---
title: Style.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words para .NET
description: Style Type propiedad. Obtiene el tipo de estilo párrafo o carácter en C#.
type: docs
weight: 170
url: /es/net/aspose.words/style/type/
---
## Style.Type property

Obtiene el tipo de estilo (párrafo o carácter).

```csharp
public StyleType Type { get; }
```

## Ejemplos

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

* enum [StyleType](../../styletype/)
* class [Style](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
