---
title: TxtLeadingSpacesOptions Enum
linktitle: TxtLeadingSpacesOptions
articleTitle: TxtLeadingSpacesOptions
second_title: Aspose.Words para .NET
description: Descubra la enumeración TxtLeadingSpacesOptions de Aspose.Words para gestionar eficientemente los espacios iniciales al importar archivos de texto. ¡Optimice el procesamiento de sus documentos hoy mismo!
type: docs
weight: 4180
url: /es/net/aspose.words.loading/txtleadingspacesoptions/
---
## TxtLeadingSpacesOptions enumeration

Especifica las opciones disponibles para el manejo del espacio inicial durante la importación desdeText archivo.

```csharp
public enum TxtLeadingSpacesOptions
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| ConvertToIndent | `0` | Los espacios iniciales se eliminan y se convierten en sangría izquierda. |
| Trim | `1` | Los espacios iniciales se recortan |
| Preserve | `2` | Se conservan los espacios iniciales. |

## Ejemplos

Muestra cómo recortar espacios en blanco al cargar documentos de texto sin formato.

```csharp
string textDoc = "      Line 1 \n" +
                 "    Line 2   \n" +
                 " Line 3       ";

// Crea un objeto "TxtLoadOptions", que podemos pasar al constructor de un documento
// para modificar la forma en que cargamos un documento de texto plano.
TxtLoadOptions loadOptions = new TxtLoadOptions();

// Establezca la propiedad "LeadingSpacesOptions" en "TxtLeadingSpacesOptions.Preserve"
// para preservar todos los caracteres de espacio en blanco al comienzo de cada línea.
// Establezca la propiedad "LeadingSpacesOptions" en "TxtLeadingSpacesOptions.ConvertToIndent"
// para eliminar todos los espacios en blanco del comienzo de cada línea,
// y luego aplique una sangría en la primera línea izquierda del párrafo para simular el efecto de los espacios en blanco.
// Establezca la propiedad "LeadingSpacesOptions" en "TxtLeadingSpacesOptions.Trim"
// para eliminar todos los caracteres de espacio en blanco del inicio de cada línea.
loadOptions.LeadingSpacesOptions = txtLeadingSpacesOptions;

// Establezca la propiedad "TrailingSpacesOptions" en "TxtTrailingSpacesOptions.Preserve"
 // para preservar todos los caracteres de espacio en blanco al final de cada línea.
 // Establezca la propiedad "TrailingSpacesOptions" en "TxtTrailingSpacesOptions.Trim" para
// eliminar todos los espacios en blanco del final de cada línea.
loadOptions.TrailingSpacesOptions = txtTrailingSpacesOptions;

Document doc = new Document(new MemoryStream(Encoding.UTF8.GetBytes(textDoc)), loadOptions);
ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

switch (txtLeadingSpacesOptions)
{
    case TxtLeadingSpacesOptions.ConvertToIndent:
        Assert.AreEqual(37.8d, paragraphs[0].ParagraphFormat.FirstLineIndent);
        Assert.AreEqual(25.2d, paragraphs[1].ParagraphFormat.FirstLineIndent);
        Assert.AreEqual(6.3d, paragraphs[2].ParagraphFormat.FirstLineIndent);

        Assert.True(paragraphs[0].GetText().StartsWith("Line 1"));
        Assert.True(paragraphs[1].GetText().StartsWith("Line 2"));
        Assert.True(paragraphs[2].GetText().StartsWith("Line 3"));
        break;
    case TxtLeadingSpacesOptions.Preserve:
        Assert.True(paragraphs.All(p => ((Paragraph)p).ParagraphFormat.FirstLineIndent == 0.0d));

        Assert.True(paragraphs[0].GetText().StartsWith("      Line 1"));
        Assert.True(paragraphs[1].GetText().StartsWith("    Line 2"));
        Assert.True(paragraphs[2].GetText().StartsWith(" Line 3"));
        break;
    case TxtLeadingSpacesOptions.Trim:
        Assert.True(paragraphs.All(p => ((Paragraph)p).ParagraphFormat.FirstLineIndent == 0.0d));

        Assert.True(paragraphs[0].GetText().StartsWith("Line 1"));
        Assert.True(paragraphs[1].GetText().StartsWith("Line 2"));
        Assert.True(paragraphs[2].GetText().StartsWith("Line 3"));
        break;
}

switch (txtTrailingSpacesOptions)
{
    case TxtTrailingSpacesOptions.Preserve:
        Assert.True(paragraphs[0].GetText().EndsWith("Line 1 \r"));
        Assert.True(paragraphs[1].GetText().EndsWith("Line 2   \r"));
        Assert.True(paragraphs[2].GetText().EndsWith("Line 3       \f"));
        break;
    case TxtTrailingSpacesOptions.Trim:
        Assert.True(paragraphs[0].GetText().EndsWith("Line 1\r"));
        Assert.True(paragraphs[1].GetText().EndsWith("Line 2\r"));
        Assert.True(paragraphs[2].GetText().EndsWith("Line 3\f"));
        break;
}
```

### Ver también

* espacio de nombres [Aspose.Words.Loading](../../aspose.words.loading/)
* asamblea [Aspose.Words](../../)
