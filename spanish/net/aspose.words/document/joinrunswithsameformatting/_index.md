---
title: Document.JoinRunsWithSameFormatting
linktitle: JoinRunsWithSameFormatting
articleTitle: JoinRunsWithSameFormatting
second_title: Aspose.Words para .NET
description: Document JoinRunsWithSameFormatting método. Las uniones se ejecutan con el mismo formato en todos los párrafos del documento en C#.
type: docs
weight: 620
url: /es/net/aspose.words/document/joinrunswithsameformatting/
---
## Document.JoinRunsWithSameFormatting method

Las uniones se ejecutan con el mismo formato en todos los párrafos del documento.

```csharp
public int JoinRunsWithSameFormatting()
```

### Valor_devuelto

Número de uniones realizadas. Cuando**norte** se unen tramos adyacentes, cuentan como**norte-1** Uniones.

## Observaciones

Este es un método de optimización. Algunos documentos contienen ejecuciones adyacentes con el mismo formato. Generalmente esto ocurre si un documento se editó manualmente de manera intensiva. Puede reducir el tamaño del documento y acelerar el procesamiento posterior uniendo estas ejecuciones.

La operación comprueba cada[`Paragraph`](../../paragraph/) nodo en el documento para adyacente[`Run`](../../run/) nodos que tienen propiedades idénticas. Ignora los identificadores únicos utilizados para rastrear las sesiones de edición de creación y modificación de run . La primera ejecución de cada secuencia de unión acumula todo el texto. Las ejecuciones restantes se eliminan del documento.

## Ejemplos

Muestra cómo unir ejecuciones en un documento para reducir ejecuciones innecesarias.

```csharp
// Abrir un documento que contiene tiradas de texto adyacentes con formato idéntico,
// lo cual ocurre comúnmente si editamos el mismo párrafo varias veces en Microsoft Word.
Document doc = new Document(MyDir + "Rendering.docx");

// Si cualquier número de estas ejecuciones son adyacentes con formato idéntico,
// entonces el documento puede simplificarse.
Assert.AreEqual(317, doc.GetChildNodes(NodeType.Run, true).Count);

// Combine dichas ejecuciones con este método y verifique la cantidad de uniones de ejecución que se llevarán a cabo.
Assert.AreEqual(121, doc.JoinRunsWithSameFormatting());

// El número de uniones y el número de ejecuciones que tenemos después de la unión
// debería sumar el número de ejecuciones que teníamos inicialmente.
Assert.AreEqual(196, doc.GetChildNodes(NodeType.Run, true).Count);
```

### Ver también

* class [Document](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
