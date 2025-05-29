---
title: FootnoteOptions.Columns
linktitle: Columns
articleTitle: Columns
second_title: Aspose.Words para .NET
description: Descubra la propiedad Columnas FootnoteOptions para formatear fácilmente sus notas al pie con diseños de columnas personalizables para una mejor legibilidad y presentación.
type: docs
weight: 10
url: /es/net/aspose.words.notes/footnoteoptions/columns/
---
## FootnoteOptions.Columns property

Especifica el número de columnas con las que se formatea el área de notas al pie.

```csharp
public int Columns { get; set; }
```

## Observaciones

Si esta propiedad tiene el valor 0, el área de notas al pie se formatea con un número de columnas basado en el número de columnas de la página mostrada. El valor predeterminado es 0.

## Ejemplos

Muestra cómo dividir la sección de notas al pie en un número determinado de columnas.

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");
doc.FootnoteOptions.Columns = 2;
doc.Save(ArtifactsDir + "Document.FootnoteColumns.docx");
```

### Ver también

* class [FootnoteOptions](../)
* espacio de nombres [Aspose.Words.Notes](../../../aspose.words.notes/)
* asamblea [Aspose.Words](../../../)
