---
title: PageSetup.Bidi
second_title: Referencia de API de Aspose.Words para .NET
description: PageSetup propiedad. Especifica que esta sección contiene texto bidireccional scripts complejos.
type: docs
weight: 10
url: /es/net/aspose.words/pagesetup/bidi/
---
## PageSetup.Bidi property

Especifica que esta sección contiene texto bidireccional (scripts complejos).

```csharp
public bool Bidi { get; set; }
```

### Observaciones

Cuando`verdadero`las columnas de esta sección están dispuestas de derecha a izquierda.

### Ejemplos

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

// Establece la propiedad "Bidi" en "verdadero" para organizar las columnas comenzando desde el lado derecho de la página.
// El orden de las columnas coincidirá con la dirección del texto de derecha a izquierda.
// Establece la propiedad "Bidi" en "falso" para organizar las columnas comenzando desde el lado izquierdo de la página.
// El orden de las columnas coincidirá con la dirección del texto de izquierda a derecha.
pageSetup.Bidi = reverseColumns;

doc.Save(ArtifactsDir + "PageSetup.Bidi.docx");
```

### Ver también

* class [PageSetup](../)
* espacio de nombres [Aspose.Words](../../pagesetup/)
* asamblea [Aspose.Words](../../../)


