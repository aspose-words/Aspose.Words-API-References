---
title: IBibliographyStylesProvider Interface
linktitle: IBibliographyStylesProvider
articleTitle: IBibliographyStylesProvider
second_title: Aspose.Words para .NET
description: Mejore el formato de sus documentos con la interfaz Aspose.Words.IBibliographyStylesProvider, perfecta para personalizar los estilos de bibliografía en las citas.
type: docs
weight: 3080
url: /es/net/aspose.words.fields/ibibliographystylesprovider/
---
## IBibliographyStylesProvider interface

Implemente esta interfaz para proporcionar un estilo de bibliografía para la[`FieldBibliography`](../fieldbibliography/) y[`FieldCitation`](../fieldcitation/) campos cuando se actualizan.

```csharp
public interface IBibliographyStylesProvider
```

## Métodos

| Nombre | Descripción |
| --- | --- |
| [GetStyle](../../aspose.words.fields/ibibliographystylesprovider/getstyle/)(*string*) | Devuelve el estilo de la bibliografía. |

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

* espacio de nombres [Aspose.Words.Fields](../../aspose.words.fields/)
* asamblea [Aspose.Words](../../)
