---
title: FontInfo.Name
linktitle: Name
articleTitle: Name
second_title: Aspose.Words para .NET
description: Descubra la propiedad Nombre FontInfo para acceder y utilizar fácilmente los nombres de fuentes para mejorar la tipografía en sus proyectos.
type: docs
weight: 60
url: /es/net/aspose.words.fonts/fontinfo/name/
---
## FontInfo.Name property

Obtiene el nombre de la fuente.

```csharp
public string Name { get; }
```

## Observaciones

No puede ser`nulo`. Puede ser una cadena vacía.

## Ejemplos

Muestra cómo imprimir los detalles de las fuentes presentes en un documento.

```csharp
Document doc = new Document(MyDir + "Embedded font.docx");

FontInfoCollection allFonts = doc.FontInfos;
// Imprime todas las fuentes utilizadas y no utilizadas en el documento.
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
