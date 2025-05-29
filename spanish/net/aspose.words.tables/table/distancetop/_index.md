---
title: Table.DistanceTop
linktitle: DistanceTop
articleTitle: DistanceTop
second_title: Aspose.Words para .NET
description: Ajuste fácilmente la distancia entre la superficie de su mesa y el texto circundante. ¡Mejore su diseño para una apariencia impecable y profesional con DistanceTop!
type: docs
weight: 150
url: /es/net/aspose.words.tables/table/distancetop/
---
## Table.DistanceTop property

Obtiene o establece la distancia entre la parte superior de la mesa y el texto circundante, en puntos.

```csharp
public double DistanceTop { get; set; }
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
