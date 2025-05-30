---
title: FontFamily Enum
linktitle: FontFamily
articleTitle: FontFamily
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.Fonts.FontFamily su clave para administrar diversas familias de fuentes sin esfuerzo para mejorar el estilo y el formato de los documentos.
type: docs
weight: 3340
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
| Auto | `0` | Especifica un nombre de familia genérico. Este nombre se utiliza cuando la información sobre una fuente no existe o no es relevante. Se utiliza la fuente predeterminada. |
| Roman | `1` | Especifica una fuente proporcional con serifas. Un ejemplo es Times New Roman. |
| Swiss | `2` | Especifica una fuente proporcional sin serifas. Un ejemplo es Arial. |
| Modern | `3` | Especifica una fuente monoespaciada con o sin serifas. Las fuentes monoespaciadas suelen ser modernas; por ejemplo, Pica, Elite y Courier New. |
| Script | `4` | Especifica una fuente diseñada para parecerse a una escritura a mano; algunos ejemplos incluyen Script y Cursive. |
| Decorative | `5` | Especifica una fuente novedosa. Un ejemplo es inglés antiguo. |

## Observaciones

Una familia de fuentes es un conjunto de fuentes que tienen un ancho de trazo y características serif comunes.

## Ejemplos

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

        // Los nombres Alt normalmente están en blanco.
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
