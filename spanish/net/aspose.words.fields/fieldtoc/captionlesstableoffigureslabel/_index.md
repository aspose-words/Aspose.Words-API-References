---
title: FieldToc.CaptionlessTableOfFiguresLabel
linktitle: CaptionlessTableOfFiguresLabel
articleTitle: CaptionlessTableOfFiguresLabel
second_title: Aspose.Words para .NET
description: Descubra la propiedad FieldToc CaptionlessTableOfFiguresLabel para personalizar su tabla de figuras. ¡Administre fácilmente identificadores de secuencia sin subtítulos!
type: docs
weight: 30
url: /es/net/aspose.words.fields/fieldtoc/captionlesstableoffigureslabel/
---
## FieldToc.CaptionlessTableOfFiguresLabel property

Obtiene o establece el nombre del identificador de secuencia utilizado al crear una tabla de figuras que no incluye la etiqueta y el número del título.

```csharp
public string CaptionlessTableOfFiguresLabel { get; set; }
```

## Ejemplos

Muestra cómo establecer el nombre del identificador de secuencia.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);
fieldToc.CaptionlessTableOfFiguresLabel = "Test";

Assert.AreEqual(" TOC  \\a Test", fieldToc.GetFieldCode());
```

### Ver también

* class [FieldToc](../)
* espacio de nombres [Aspose.Words.Fields](../../../aspose.words.fields/)
* asamblea [Aspose.Words](../../../)
