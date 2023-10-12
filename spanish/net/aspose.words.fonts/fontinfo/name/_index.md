---
title: FontInfo.Name
second_title: Referencia de API de Aspose.Words para .NET
description: FontInfo propiedad. Obtiene el nombre de la fuente.
type: docs
weight: 50
url: /es/net/aspose.words.fonts/fontinfo/name/
---
## FontInfo.Name property

Obtiene el nombre de la fuente.

```csharp
public string Name { get; }
```

### Observaciones

No puede ser`nulo`. Puede ser una cadena vacía.

### Ejemplos

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
* espacio de nombres [Aspose.Words.Fonts](../../fontinfo/)
* asamblea [Aspose.Words](../../../)


