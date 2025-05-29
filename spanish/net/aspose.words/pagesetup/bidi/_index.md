---
title: PageSetup.Bidi
linktitle: Bidi
articleTitle: Bidi
second_title: Aspose.Words para .NET
description: Descubra la propiedad PageSetup Bidi para un formato de texto bidireccional perfecto. Mejore sus documentos con compatibilidad con scripts complejos para una mejor legibilidad.
type: docs
weight: 10
url: /es/net/aspose.words/pagesetup/bidi/
---
## PageSetup.Bidi property

Especifica que esta sección contiene texto bidireccional (scripts complejos).

```csharp
public bool Bidi { get; set; }
```

## Observaciones

Cuando`verdadero`Las columnas de esta sección están dispuestas de derecha a izquierda.

## Ejemplos

Muestra cómo establecer el orden de las columnas de texto en una sección.

```csharp
Document doc = new Document();

PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.TextColumns.SetCount(3);

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Column 1.");
builder.InsertBreak(BreakType.ColumnBreak);
builder.Write("Column 2.");
builder.InsertBreak(BreakType.ColumnBreak);
builder.Write("Column 3.");

// Establezca la propiedad "Bidi" en "verdadero" para organizar las columnas comenzando desde el lado derecho de la página.
//El orden de las columnas coincidirá con la dirección del texto de derecha a izquierda.
// Establezca la propiedad "Bidi" en "falso" para organizar las columnas comenzando desde el lado izquierdo de la página.
//El orden de las columnas coincidirá con la dirección del texto de izquierda a derecha.
pageSetup.Bidi = reverseColumns;

doc.Save(ArtifactsDir + "PageSetup.Bidi.docx");
```

### Ver también

* class [PageSetup](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
