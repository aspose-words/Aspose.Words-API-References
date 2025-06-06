---
title: Table.DistanceBottom
linktitle: DistanceBottom
articleTitle: DistanceBottom
second_title: Aspose.Words para .NET
description: Ajuste la propiedad DistanciaBottom de la tabla para controlar el espaciado entre la parte inferior de la tabla y el texto circundante, mejorando el diseño y la legibilidad.
type: docs
weight: 120
url: /es/net/aspose.words.tables/table/distancebottom/
---
## Table.DistanceBottom property

Obtiene o establece la distancia entre la parte inferior de la tabla y el texto circundante, en puntos.

```csharp
public double DistanceBottom { get; set; }
```

## Ejemplos

Muestra cómo establecer la distancia entre los límites de la tabla y el texto.

```csharp
Document doc = new Document(MyDir + "Table wrapped by text.docx");

Table table = doc.FirstSection.Body.Tables[0];
Assert.AreEqual(25.9d, table.DistanceTop);
Assert.AreEqual(25.9d, table.DistanceBottom);
Assert.AreEqual(17.3d, table.DistanceLeft);
Assert.AreEqual(17.3d, table.DistanceRight);

// Establezca la distancia entre la tabla y el texto circundante.
table.DistanceLeft = 24;
table.DistanceRight = 24;
table.DistanceTop = 3;
table.DistanceBottom = 3;

doc.Save(ArtifactsDir + "Table.DistanceBetweenTableAndText.docx");
```

### Ver también

* class [Table](../)
* espacio de nombres [Aspose.Words.Tables](../../../aspose.words.tables/)
* asamblea [Aspose.Words](../../../)
