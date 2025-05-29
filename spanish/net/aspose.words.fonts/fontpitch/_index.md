---
title: FontPitch Enum
linktitle: FontPitch
articleTitle: FontPitch
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.Fonts.FontPitch, una poderosa herramienta para administrar estilos de fuente y mejorar el formato de documentos en sus aplicaciones.
type: docs
weight: 3390
url: /es/net/aspose.words.fonts/fontpitch/
---
## FontPitch enumeration

Representa el paso de fuente.

```csharp
public enum FontPitch
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Default | `0` | Especifica que no hay información disponible sobre el paso de una fuente. |
| Fixed | `1` | Especifica que se trata de una fuente de ancho fijo. |
| Variable | `2` | Especifica que se trata de una fuente de ancho proporcional. |

## Observaciones

El paso indica si la fuente tiene un paso fijo, está espaciada proporcionalmente o se basa en una configuración predeterminada.

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
