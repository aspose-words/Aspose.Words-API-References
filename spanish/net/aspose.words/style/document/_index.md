---
title: Style.Document
linktitle: Document
articleTitle: Document
second_title: Aspose.Words para .NET
description: Descubra la propiedad Documento de estilo para acceder y administrar fácilmente su documento de propietario para una mejor organización y eficiencia.
type: docs
weight: 50
url: /es/net/aspose.words/style/document/
---
## Style.Document property

Obtiene el documento del propietario.

```csharp
public DocumentBase Document { get; }
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

* class [DocumentBase](../../documentbase/)
* class [Style](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
