---
title: FontInfo.IsTrueType
linktitle: IsTrueType
articleTitle: IsTrueType
second_title: Aspose.Words para .NET
description: FontInfo IsTrueType propiedad. Indica que esta fuente es una fuente TrueType u OpenType en lugar de una fuente rasterizada o vectorial. El valor predeterminado esverdadero  en C#.
type: docs
weight: 40
url: /es/net/aspose.words.fonts/fontinfo/istruetype/
---
## FontInfo.IsTrueType property

Indica que esta fuente es una fuente TrueType u OpenType en lugar de una fuente rasterizada o vectorial. El valor predeterminado es`verdadero` .

```csharp
public bool IsTrueType { get; set; }
```

## Ejemplos

Muestra cómo imprimir los detalles de las fuentes presentes en un documento.

```csharp
Document doc = new Document(MyDir + "Embedded font.docx");

FontInfoCollection allFonts = doc.FontInfos;
// Imprime todas las fuentes usadas y no utilizadas en el documento.
for (int i = 0; i < allFonts.Count; i++)
{
    Console.WriteLine($"Font index #{i}");
    Console.WriteLine($"\tName: {allFonts[i].Name}");
    Console.WriteLine($"\tIs {(allFonts[i].IsTrueType ? "" : "not ")}a trueType font");
}
```

### Ver también

* class [FontInfo](../)
* espacio de nombres [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* asamblea [Aspose.Words](../../../)
