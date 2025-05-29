---
title: IBibliographyStylesProvider.GetStyle
linktitle: GetStyle
articleTitle: GetStyle
second_title: Aspose.Words para .NET
description: Descubra el método GetStyle de IBibliographyStylesProvider para recuperar y personalizar sin esfuerzo sus estilos de bibliografía para mejorar la escritura académica.
type: docs
weight: 10
url: /es/net/aspose.words.fields/ibibliographystylesprovider/getstyle/
---
## IBibliographyStylesProvider.GetStyle method

Devuelve el estilo de la bibliografía.

```csharp
public Stream GetStyle(string styleFileName)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| styleFileName | String | El nombre del archivo de estilo de bibliografía. |

### Valor_devuelto

ElStream con estilo de bibliografía y hoja de estilos XSLT.

## Observaciones

La implementación debería retornar`nulo` para indicar que se debe utilizar la versión de MS Word del estilo especificado.

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

* interface [IBibliographyStylesProvider](../)
* espacio de nombres [Aspose.Words.Fields](../../../aspose.words.fields/)
* asamblea [Aspose.Words](../../../)
