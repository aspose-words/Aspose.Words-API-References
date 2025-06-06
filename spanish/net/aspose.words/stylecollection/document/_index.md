---
title: StyleCollection.Document
linktitle: Document
articleTitle: Document
second_title: Aspose.Words para .NET
description: Accede fácilmente al documento del propietario con StyleCollection. ¡Descubre una gestión documental fluida y optimiza tu flujo de trabajo hoy mismo!
type: docs
weight: 40
url: /es/net/aspose.words/stylecollection/document/
---
## StyleCollection.Document property

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
* class [StyleCollection](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
