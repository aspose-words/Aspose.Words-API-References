---
title: FieldInclude.SourceFullName
linktitle: SourceFullName
articleTitle: SourceFullName
second_title: Aspose.Words para .NET
description: Descubra cómo usar la propiedad FieldInclude SourceFullName para gestionar eficientemente la ubicación de los documentos. ¡Mejore su flujo de trabajo hoy mismo!
type: docs
weight: 40
url: /es/net/aspose.words.fields/fieldinclude/sourcefullname/
---
## FieldInclude.SourceFullName property

Obtiene o establece la ubicación del documento.

```csharp
public string SourceFullName { get; set; }
```

## Ejemplos

Muestra cómo crear un campo INCLUDE y configurar sus propiedades.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

//Podemos utilizar un campo INCLUDE para importar una parte de otro documento en el sistema de archivos local.
//El marcador del otro documento al que hacemos referencia con este campo contiene esta parte importada.
FieldInclude field = (FieldInclude)builder.InsertField(FieldType.FieldInclude, true);
field.SourceFullName = MyDir + "Bookmarks.docx";
field.BookmarkName = "MyBookmark1";
field.LockFields = false;
field.TextConverter = "Microsoft Word";

Assert.True(Regex.Match(field.GetFieldCode(), " INCLUDE .* MyBookmark1 \\\\c \"Microsoft Word\"").Success);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INCLUDE.docx");
```

### Ver también

* class [FieldInclude](../)
* espacio de nombres [Aspose.Words.Fields](../../../aspose.words.fields/)
* asamblea [Aspose.Words](../../../)
