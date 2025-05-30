---
title: FieldInclude.TextConverter
linktitle: TextConverter
articleTitle: TextConverter
second_title: Aspose.Words para .NET
description: Descubra la propiedad FieldInclude TextConverter administre fácilmente las conversiones de formatos de archivo con nombres de convertidores de texto personalizables para mejorar la eficiencia del flujo de trabajo.
type: docs
weight: 50
url: /es/net/aspose.words.fields/fieldinclude/textconverter/
---
## FieldInclude.TextConverter property

Obtiene o establece el nombre del convertidor de texto para el formato del archivo incluido.

```csharp
public string TextConverter { get; set; }
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
