---
title: Bibliography.BibliographyStyle
linktitle: BibliographyStyle
articleTitle: BibliographyStyle
second_title: Aspose.Words para .NET
description: Descubra la propiedad BibliographyStyle: administre y personalice fácilmente el estilo activo de su bibliografía para una mejor organización y presentación.
type: docs
weight: 10
url: /es/net/aspose.words.bibliography/bibliography/bibliographystyle/
---
## Bibliography.BibliographyStyle property

Obtiene o establece una cadena que representa el nombre del estilo activo que se utilizará para una bibliografía.

```csharp
public string BibliographyStyle { get; set; }
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

* class [Bibliography](../)
* espacio de nombres [Aspose.Words.Bibliography](../../../aspose.words.bibliography/)
* asamblea [Aspose.Words](../../../)
