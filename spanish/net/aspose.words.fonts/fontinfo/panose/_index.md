---
title: FontInfo.Panose
linktitle: Panose
articleTitle: Panose
second_title: Aspose.Words para .NET
description: Descubra la propiedad FontInfo PANOSE, obtenga o configure fácilmente el número de clasificación tipográfica para una mejor gestión de fuentes y precisión de diseño.
type: docs
weight: 70
url: /es/net/aspose.words.fonts/fontinfo/panose/
---
## FontInfo.Panose property

Obtiene o establece el número de clasificación de tipografía PANOSE.

```csharp
public byte[] Panose { get; set; }
```

## Observaciones

PANOSE es una descripción compacta de 10 bytes de las características visuales esenciales de una fuente, como el contraste, el grosor y el estilo serif. Los dígitos representan el tipo de familia, el estilo serif, el grosor, la proporción, el contraste, la variación del trazo, el estilo del brazo, la forma de la letra, la línea media y la altura de la X.

Puede ser`nulo`.

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

* class [FontInfo](../)
* espacio de nombres [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* asamblea [Aspose.Words](../../../)
