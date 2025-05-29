---
title: FieldInclude.LockFields
linktitle: LockFields
articleTitle: LockFields
second_title: Aspose.Words para .NET
description: Gestione fácilmente las actualizaciones de documentos con la propiedad FieldInclude LockFields. Controle la edición de campos y mejore la integridad de los documentos fácilmente.
type: docs
weight: 30
url: /es/net/aspose.words.fields/fieldinclude/lockfields/
---
## FieldInclude.LockFields property

Obtiene o establece si se debe evitar que se actualicen los campos del documento incluido.

```csharp
public bool LockFields { get; set; }
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
