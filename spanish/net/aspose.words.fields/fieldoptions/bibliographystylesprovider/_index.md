---
title: FieldOptions.BibliographyStylesProvider
linktitle: BibliographyStylesProvider
articleTitle: BibliographyStylesProvider
second_title: Aspose.Words para .NET
description: Descubra la propiedad FieldOptions BibliographyStylesProvider para estilos de bibliografía personalizables y mejorar sus campos FieldBibliography y FieldCitation.
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

Muestra cómo anular estilos incorporados o proporcionar uno personalizado.

```csharp
public void ChangeBibliographyStyles()
{
    Document doc = new Document(MyDir + "Bibliography.docx");

    // Si el documento ya tiene un estilo puedes cambiarlo con el siguiente código:
    // doc.Bibliography.BibliographyStyle = "Estilo personalizado de bibliografía.xsl";

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
