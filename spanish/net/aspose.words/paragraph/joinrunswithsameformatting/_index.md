---
title: Paragraph.JoinRunsWithSameFormatting
second_title: Referencia de API de Aspose.Words para .NET
description: Paragraph método. Une ejecuciones con el mismo formato en el párrafo.
type: docs
weight: 300
url: /es/net/aspose.words/paragraph/joinrunswithsameformatting/
---
## Paragraph.JoinRunsWithSameFormatting method

Une ejecuciones con el mismo formato en el párrafo.

```csharp
public int JoinRunsWithSameFormatting()
```

### Valor_devuelto

Número de uniones realizadas. Cuando **norte** se unen tramos adyacentes, cuentan como **norte-1** Uniones.

### Ejemplos

Muestra cómo simplificar párrafos fusionando ejecuciones superfluas.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserta cuatro corridas de texto en el párrafo.
builder.Write("Run 1. ");
builder.Write("Run 2. ");
builder.Write("Run 3. ");
builder.Write("Run 4. ");

// Si abrimos este documento en Microsoft Word, el párrafo se verá como un cuerpo de texto sin interrupciones.
// Sin embargo, constará de cuatro ejecuciones separadas con el mismo formato. Párrafos fragmentados como este
// puede ocurrir cuando editamos manualmente partes de un párrafo muchas veces en Microsoft Word.
Paragraph para = builder.CurrentParagraph;

Assert.AreEqual(4, para.Runs.Count);

// Cambia el estilo de la última ejecución para diferenciarla de las tres primeras.
para.Runs[3].Font.StyleIdentifier = StyleIdentifier.Emphasis;

// Podemos ejecutar el método "JoinRunsWithSameFormatting" para optimizar el contenido del documento
// fusionando ejecuciones similares en una, reduciendo su recuento general.
// Este método también devuelve el número de ejecuciones que este método fusionó.
// Estas dos fusiones ocurrieron para combinar las Ejecuciones #1, #2 y #3,
// y omite la ejecución n.° 4 porque tiene un estilo incompatible.
Assert.AreEqual(2, para.JoinRunsWithSameFormatting());

// El número de ejecuciones restantes será igual al recuento original
// menos el número de fusiones de ejecución que realizó el método "JoinRunsWithSameFormatting".
Assert.AreEqual(2, para.Runs.Count);
Assert.AreEqual("Run 1. Run 2. Run 3. ", para.Runs[0].Text);
Assert.AreEqual("Run 4. ", para.Runs[1].Text);
```

### Ver también

* class [Paragraph](../)
* espacio de nombres [Aspose.Words](../../paragraph/)
* asamblea [Aspose.Words](../../../)


