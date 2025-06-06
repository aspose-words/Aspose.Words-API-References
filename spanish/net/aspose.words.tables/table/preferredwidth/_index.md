---
title: Table.PreferredWidth
linktitle: PreferredWidth
articleTitle: PreferredWidth
second_title: Aspose.Words para .NET
description: Descubra cómo utilizar la propiedad Table PreferredWidth para configurar y optimizar fácilmente el diseño de su tabla para mejorar el diseño y la experiencia del usuario.
type: docs
weight: 220
url: /es/net/aspose.words.tables/table/preferredwidth/
---
## Table.PreferredWidth property

Obtiene o establece el ancho preferido de la tabla.

```csharp
public PreferredWidth PreferredWidth { get; set; }
```

## Observaciones

El valor predeterminado es[`Auto`](../../preferredwidth/auto/).

## Ejemplos

Muestra cómo configurar una tabla para que se ajuste automáticamente al 50% del ancho de la página.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Cell #1");
builder.InsertCell();
builder.Write("Cell #2");
builder.InsertCell();
builder.Write("Cell #3");

table.PreferredWidth = PreferredWidth.FromPercent(50);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertTableWithPreferredWidth.docx");
```

### Ver también

* class [PreferredWidth](../../preferredwidth/)
* class [Table](../)
* espacio de nombres [Aspose.Words.Tables](../../../aspose.words.tables/)
* asamblea [Aspose.Words](../../../)
