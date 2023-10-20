---
title: FieldOptions.BibliographyStylesProvider
linktitle: BibliographyStylesProvider
articleTitle: BibliographyStylesProvider
second_title: Aspose.Words para .NET
description: FieldOptions BibliographyStylesProvider propiedad. Obtiene o establece un proveedor que devuelve un estilo de bibliografía para elFieldBibliography yFieldCitation campos en C#.
type: docs
weight: 20
url: /es/net/aspose.words.fields/fieldoptions/bibliographystylesprovider/
---
## FieldOptions.BibliographyStylesProvider property

Obtiene o establece un proveedor que devuelve un estilo de bibliografía para el[`FieldBibliography`](../../fieldbibliography/) y[`FieldCitation`](../../fieldcitation/) campos.

```csharp
public IBibliographyStylesProvider BibliographyStylesProvider { get; set; }
```

## Ejemplos

Muestra cómo anular los estilos integrados o proporcionar uno personalizado.

```csharp
public void ChangeBibliographyStyles()
{            
    Document doc = new Document(MyDir + "Bibliography.docx");

    doc.FieldOptions.BibliographyStylesProvider = new BibliographyStylesProvider();
    doc.UpdateFields();

    doc.Save(ArtifactsDir + "Field.ChangeBibliographyStyles.docx");
}

public class BibliographyStylesProvider : IBibliographyStylesProvider
{
    Stream IBibliographyStylesProvider.GetStyle(string styleFileName)
    {
        return File.OpenRead(MyDir + "Bibliography custom style.xsl");
    }
}
```

### Ver también

* interface [IBibliographyStylesProvider](../../ibibliographystylesprovider/)
* class [FieldOptions](../)
* espacio de nombres [Aspose.Words.Fields](../../../aspose.words.fields/)
* asamblea [Aspose.Words](../../../)
