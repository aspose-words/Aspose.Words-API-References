---
title: Enum FontFamily
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Fonts.FontFamily enumeración. Representa la familia de fuentes.
type: docs
weight: 2910
url: /es/net/aspose.words.fonts/fontfamily/
---
## FontFamily enumeration

Representa la familia de fuentes.

```csharp
public enum FontFamily
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Auto | `0` | Especifica un apellido genérico. Este nombre se utiliza cuando la información sobre una fuente no existe o no importa. Se utiliza la fuente predeterminada. |
| Roman | `1` | Especifica una fuente proporcional con serifas. Un ejemplo es Times New Roman. |
| Swiss | `2` | Especifica una fuente proporcional sin serifas. Un ejemplo es Arial. |
| Modern | `3` | Especifica una fuente monoespaciada con o sin serifas. Las fuentes monoespaciadas suelen ser modernas; los ejemplos incluyen Pica, Elite y Courier New. |
| Script | `4` | Especifica una fuente diseñada para parecerse a escritura a mano; los ejemplos incluyen escritura y cursiva. |
| Decorative | `5` | Especifica una fuente novedosa. Un ejemplo es el inglés antiguo. |

### Observaciones

Una familia de fuentes es un conjunto de fuentes que tienen características serif y ancho de trazo comunes.

### Ejemplos

Muestra cómo acceder e imprimir detalles de cada fuente en un documento.

```csharp
Document doc = new Document(MyDir + "Document.docx");

IEnumerator<FontInfo> fontCollectionEnumerator = doc.FontInfos.GetEnumerator();
while (fontCollectionEnumerator.MoveNext())
{
    FontInfo fontInfo = fontCollectionEnumerator.Current;
    if (fontInfo != null)
    {
        Console.WriteLine("Font name: " + fontInfo.Name);

        // Los nombres alternativos suelen estar en blanco.
        Console.WriteLine("Alt name: " + fontInfo.AltName);
        Console.WriteLine("\t- Family: " + fontInfo.Family);
        Console.WriteLine("\t- " + (fontInfo.IsTrueType ? "Is TrueType" : "Is not TrueType"));
        Console.WriteLine("\t- Pitch: " + fontInfo.Pitch);
        Console.WriteLine("\t- Charset: " + fontInfo.Charset);
        Console.WriteLine("\t- Panose:");
        Console.WriteLine("\t\tFamily Kind: " + fontInfo.Panose[0]);
        Console.WriteLine("\t\tSerif Style: " + fontInfo.Panose[1]);
        Console.WriteLine("\t\tWeight: " + fontInfo.Panose[2]);
        Console.WriteLine("\t\tProportion: " + fontInfo.Panose[3]);
        Console.WriteLine("\t\tContrast: " + fontInfo.Panose[4]);
        Console.WriteLine("\t\tStroke Variation: " + fontInfo.Panose[5]);
        Console.WriteLine("\t\tArm Style: " + fontInfo.Panose[6]);
        Console.WriteLine("\t\tLetterform: " + fontInfo.Panose[7]);
        Console.WriteLine("\t\tMidline: " + fontInfo.Panose[8]);
        Console.WriteLine("\t\tX-Height: " + fontInfo.Panose[9]);
    }
}
```

### Ver también

* espacio de nombres [Aspose.Words.Fonts](../../aspose.words.fonts/)
* asamblea [Aspose.Words](../../)


