---
title: Columns
second_title: Referencia de API de Aspose.Words para .NET
description: Especifica el número de columnas con las que se formatea el área de notas al pie.
type: docs
weight: 10
url: /es/net/aspose.words.notes/footnoteoptions/columns/
---
## FootnoteOptions.Columns property

Especifica el número de columnas con las que se formatea el área de notas al pie.

```csharp
public int Columns { get; set; }
```

### Observaciones

Si esta propiedad tiene el valor 0, el área de notas al pie se formatea con un número de columnas basado en el número de columnas en la página mostrada. El valor predeterminado es 0.

### Ejemplos

Muestra cómo dividir la sección de notas al pie en un número determinado de columnas.

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");
doc.FootnoteOptions.Columns = 2;
doc.Save(ArtifactsDir + "Document.FootnoteColumns.docx");
```

### Ver también

* class [FootnoteOptions](../../footnoteoptions)
* espacio de nombres [Aspose.Words.Notes](../../footnoteoptions)
* asamblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
