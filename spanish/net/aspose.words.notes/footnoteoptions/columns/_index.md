---
title: FootnoteOptions.Columns
linktitle: Columns
articleTitle: Columns
second_title: Aspose.Words para .NET
description: FootnoteOptions Columns propiedad. Especifica el número de columnas con las que se formatea el área de notas al pie en C#.
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

Si esta propiedad tiene el valor de 0, el área de notas al pie tiene formato con una cantidad de columnas basadas en la cantidad de columnas en la página mostrada. El valor predeterminado es 0.

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
