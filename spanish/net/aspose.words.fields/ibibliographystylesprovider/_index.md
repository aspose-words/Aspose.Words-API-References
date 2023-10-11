---
title: Interface IBibliographyStylesProvider
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Fields.IBibliographyStylesProvider interfaz. Implemente esta interfaz para proporcionar estilo de bibliografía para elFieldBibliography yFieldCitation campos cuando se actualizan.
type: docs
weight: 2670
url: /es/net/aspose.words.fields/ibibliographystylesprovider/
---
## IBibliographyStylesProvider interface

Implemente esta interfaz para proporcionar estilo de bibliografía para el[`FieldBibliography`](../fieldbibliography/) y[`FieldCitation`](../fieldcitation/) campos cuando se actualizan.

```csharp
public interface IBibliographyStylesProvider
```

## Métodos

| Nombre | Descripción |
| --- | --- |
| [GetStyle](../../aspose.words.fields/ibibliographystylesprovider/getstyle/)(string) | Devuelve el estilo de bibliografía. |

### Ejemplos

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

* espacio de nombres [Aspose.Words.Fields](../../aspose.words.fields/)
* asamblea [Aspose.Words](../../)


