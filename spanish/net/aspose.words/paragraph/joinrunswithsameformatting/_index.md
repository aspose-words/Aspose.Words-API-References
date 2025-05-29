---
title: Paragraph.JoinRunsWithSameFormatting
linktitle: JoinRunsWithSameFormatting
articleTitle: JoinRunsWithSameFormatting
second_title: Aspose.Words para .NET
description: Une fácilmente secuencias con un formato uniforme en tus párrafos con el método JoinRunsWithSameFormatting. ¡Mejora el estilo de tu documento hoy mismo!
type: docs
weight: 300
url: /es/net/aspose.words/paragraph/joinrunswithsameformatting/
---
## Paragraph.JoinRunsWithSameFormatting method

Une líneas con el mismo formato en el párrafo.

```csharp
public int JoinRunsWithSameFormatting()
```

### Valor_devuelto

Número de uniones realizadas. Cuando**norte** Se unen carreras adyacentes y se cuentan como**N-1** se une.

## Ejemplos

Muestra cómo simplificar párrafos fusionando líneas superfluas.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserta cuatro líneas de texto en el párrafo.
builder.Write("Run 1. ");
builder.Write("Run 2. ");
builder.Write("Run 3. ");
builder.Write("Run 4. ");

// Si abrimos este documento en Microsoft Word, el párrafo se verá como un cuerpo de texto sin fisuras.
// Sin embargo, constará de cuatro secciones separadas con el mismo formato. Párrafos fragmentados como este
// Puede ocurrir cuando editamos manualmente partes de un párrafo muchas veces en Microsoft Word.
Paragraph para = builder.CurrentParagraph;

Assert.AreEqual(4, para.Runs.Count);

// Cambia el estilo de la última ejecución para diferenciarla de las tres primeras.
para.Runs[3].Font.StyleIdentifier = StyleIdentifier.Emphasis;

// Podemos ejecutar el método "JoinRunsWithSameFormatting" para optimizar el contenido del documento
// fusionando ejecuciones similares en una sola, reduciendo su recuento general.
// Este método también devuelve el número de ejecuciones que este método fusionó.
// Estas dos fusiones se produjeron para combinar las ejecuciones n.° 1, n.° 2 y n.° 3.
// mientras que dejamos fuera la ejecución n.° 4 porque tiene un estilo incompatible.
Assert.AreEqual(2, para.JoinRunsWithSameFormatting());

// El número de carreras restantes será igual al recuento original
// menos el número de fusiones de ejecuciones que realizó el método "JoinRunsWithSameFormatting".
Assert.AreEqual(2, para.Runs.Count);
Assert.AreEqual("Run 1. Run 2. Run 3. ", para.Runs[0].Text);
Assert.AreEqual("Run 4. ", para.Runs[1].Text);
```

### Ver también

* class [Paragraph](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
