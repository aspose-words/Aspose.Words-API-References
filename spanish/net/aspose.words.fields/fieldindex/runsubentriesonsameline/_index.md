---
title: FieldIndex.RunSubentriesOnSameLine
second_title: Referencia de API de Aspose.Words para .NET
description: FieldIndex propiedad. Obtiene o establece si se ejecutan subentradas en la misma línea que la entrada principal.
type: docs
weight: 140
url: /es/net/aspose.words.fields/fieldindex/runsubentriesonsameline/
---
## FieldIndex.RunSubentriesOnSameLine property

Obtiene o establece si se ejecutan subentradas en la misma línea que la entrada principal.

```csharp
public bool RunSubentriesOnSameLine { get; set; }
```

### Ejemplos

Muestra cómo trabajar con subentradas en un campo ÍNDICE.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Cree un campo ÍNDICE que mostrará una entrada para cada campo XE encontrado en el documento.
// Cada entrada mostrará el valor de la propiedad Texto del campo XE en el lado izquierdo,
// y el número de la página que contiene el campo XE a la derecha.
// La entrada ÍNDICE recopilará todos los campos XE con valores coincidentes en la propiedad "Texto"
// en una entrada en lugar de hacer una entrada para cada campo XE.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);
index.PageNumberSeparator = ", see page ";
index.Heading = "A";

// Campos XE que tienen una propiedad Texto cuyo valor se convierte en el encabezado de la entrada ÍNDICE.
// Si este valor contiene dos segmentos de cadena divididos por dos puntos (la entrada ÍNDICE tratará :) delimitador,
// el primer segmento es el encabezado y el segundo segmento se convertirá en el subencabezado.
// El campo ÍNDICE primero agrupa las entradas en orden alfabético, luego, si hay varios campos XE con el mismo
// encabezados, el campo ÍNDICE los subagrupará aún más por los valores de estos encabezados.
// Puede haber múltiples capas de subgrupos, dependiendo de cuántas veces
// las propiedades de texto de los campos XE se segmentan así.
  // De forma predeterminada, un grupo de entrada de campo ÍNDICE creará una nueva línea para cada subtítulo dentro de este grupo.
// Podemos establecer el indicador RunSubentriesOnSameLine en verdadero para mantener el encabezado,
// y cada subtítulo del grupo en una sola línea, lo que hará que el campo ÍNDICE sea más compacto.
index.RunSubentriesOnSameLine = runSubentriesOnTheSameLine;

if (runSubentriesOnTheSameLine)
    Assert.AreEqual(" INDEX  \\e \", see page \" \\h A \\r", index.GetFieldCode());
else
    Assert.AreEqual(" INDEX  \\e \", see page \" \\h A", index.GetFieldCode());

// Insertar dos campos XE, cada uno en una nueva página, y con el mismo encabezado llamado "Título 1",
// que usará el campo ÍNDICE para agruparlos.
// Si RunSubentriesOnSameLine es falso, la tabla INDEX creará tres líneas:
// una línea para el encabezado de agrupación "Título 1", y una línea más para cada subtítulo.
// Si RunSubentriesOnSameLine es verdadero, entonces la tabla ÍNDICE creará una línea
// entrada que engloba el título y todos los subtítulos.
builder.InsertBreak(BreakType.PageBreak);
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Heading 1:Subheading 1";

Assert.AreEqual(" XE  \"Heading 1:Subheading 1\"", indexEntry.GetFieldCode());

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Heading 1:Subheading 2";

doc.UpdateFields();
doc.Save(ArtifactsDir + $"Field.INDEX.XE.Subheading.docx");
```

### Ver también

* class [FieldIndex](../)
* espacio de nombres [Aspose.Words.Fields](../../fieldindex/)
* asamblea [Aspose.Words](../../../)


