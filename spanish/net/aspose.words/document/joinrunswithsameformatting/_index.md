---
title: Document.JoinRunsWithSameFormatting
linktitle: JoinRunsWithSameFormatting
articleTitle: JoinRunsWithSameFormatting
second_title: Aspose.Words para .NET
description: Descubra cómo el método JoinRunsWithSameFormatting fusiona sin problemas el texto formateado en los párrafos de su documento para lograr una apariencia pulida y profesional.
type: docs
weight: 660
url: /es/net/aspose.words/document/joinrunswithsameformatting/
---
## Document.JoinRunsWithSameFormatting method

Une ejecuciones con el mismo formato en todos los párrafos del documento.

```csharp
public int JoinRunsWithSameFormatting()
```

### Valor_devuelto

Número de uniones realizadas. Cuando**norte** Se unen carreras adyacentes y se cuentan como**N-1** se une.

## Observaciones

Este es un método de optimización. Algunos documentos contienen ejecuciones adyacentes con el mismo formato. Esto suele ocurrir si un documento se editó manualmente de forma intensiva. Puede reducir el tamaño del documento y acelerar el procesamiento posterior uniendo estas ejecuciones.

La operación verifica cada[`Paragraph`](../../paragraph/) nodo en el documento para adyacente[`Run`](../../run/)Nodos con propiedades idénticas. Se ignoran los identificadores únicos utilizados para registrar las sesiones de edición de creación y modificación de run . La primera ejecución de cada secuencia de unión acumula todo el texto. Las ejecuciones restantes se eliminan del documento.

## Ejemplos

Muestra cómo unir ejecuciones en un documento para reducir ejecuciones innecesarias.

```csharp
//Abre un documento que contiene líneas de texto adyacentes con formato idéntico,
// lo que ocurre comúnmente si editamos el mismo párrafo varias veces en Microsoft Word.
Document doc = new Document(MyDir + "Rendering.docx");

// Si alguna cantidad de estas ejecuciones son adyacentes con formato idéntico,
//Entonces el documento puede simplificarse.
Assert.AreEqual(317, doc.GetChildNodes(NodeType.Run, true).Count);

// Combine dichas ejecuciones con este método y verifique la cantidad de uniones de ejecuciones que se realizarán.
Assert.AreEqual(121, doc.JoinRunsWithSameFormatting());

// El número de uniones y el número de ejecuciones que tenemos después de la unión
//deberíamos sumar el número de carreras que teníamos inicialmente.
Assert.AreEqual(196, doc.GetChildNodes(NodeType.Run, true).Count);
```

### Ver también

* class [Document](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
