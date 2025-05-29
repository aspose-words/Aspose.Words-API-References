---
title: FieldIndex.RunSubentriesOnSameLine
linktitle: RunSubentriesOnSameLine
articleTitle: RunSubentriesOnSameLine
second_title: Aspose.Words para .NET
description: Descubra la propiedad FieldIndex RunSubentriesOnSameLine para administrar fácilmente subentradas en línea con las entradas principales para una organización optimizada de los datos.
type: docs
weight: 140
url: /es/net/aspose.words.fields/fieldindex/runsubentriesonsameline/
---
## FieldIndex.RunSubentriesOnSameLine property

Obtiene o establece si se ejecutan subentradas en la misma línea que la entrada principal.

```csharp
public bool RunSubentriesOnSameLine { get; set; }
```

## Ejemplos

Muestra cómo trabajar con subentradas en un campo ÍNDICE.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Cree un campo INDEX que mostrará una entrada para cada campo XE encontrado en el documento.
// Cada entrada mostrará el valor de la propiedad de Texto del campo XE en el lado izquierdo,
// y el número de la página que contiene el campo XE a la derecha.
// La entrada INDEX recopilará todos los campos XE con valores coincidentes en la propiedad "Texto"
// en una sola entrada en lugar de hacer una entrada para cada campo XE.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);
index.PageNumberSeparator = ", see page ";
index.Heading = "A";

// Campos XE que tienen una propiedad Texto cuyo valor se convierte en el encabezado de la entrada INDEX.
// Si este valor contiene dos segmentos de cadena divididos por dos puntos (la entrada INDEX tratará el delimitador :),
// el primer segmento es el encabezado y el segundo segmento se convertirá en el subencabezado.
// El campo ÍNDICE primero agrupa las entradas alfabéticamente, luego, si hay varios campos XE con el mismo
// encabezados, el campo ÍNDICE los subagrupará aún más según los valores de estos encabezados.
// Puede haber múltiples capas de subagrupación, dependiendo de cuántas veces
//Las propiedades de texto de los campos XE se segmentan de esta manera.
// De forma predeterminada, un grupo de entrada de campo ÍNDICE creará una nueva línea para cada subtítulo dentro de este grupo.
// Podemos establecer el indicador RunSubentriesOnSameLine en verdadero para mantener el encabezado,
// y cada subtítulo del grupo en una sola línea, lo que hará que el campo ÍNDICE sea más compacto.
index.RunSubentriesOnSameLine = runSubentriesOnTheSameLine;

if (runSubentriesOnTheSameLine)
    Assert.AreEqual(" INDEX  \\e \", see page \" \\h A \\r", index.GetFieldCode());
else
    Assert.AreEqual(" INDEX  \\e \", see page \" \\h A", index.GetFieldCode());

// Insertar dos campos XE, cada uno en una página nueva, y con el mismo encabezado llamado "Encabezado 1",
// que utilizará el campo INDEX para agruparlos.
// Si RunSubentriesOnSameLine es falso, entonces la tabla INDEX creará tres líneas:
// una línea para el encabezado de agrupación "Encabezado 1", y una línea más para cada subencabezado.
// Si RunSubentriesOnSameLine es verdadero, entonces la tabla INDEX creará una línea única
// entrada que abarca el encabezado y cada subencabezado.
builder.InsertBreak(BreakType.PageBreak);
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Heading 1:Subheading 1";

Assert.AreEqual(" XE  \"Heading 1:Subheading 1\"", indexEntry.GetFieldCode());

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Heading 1:Subheading 2";

doc.UpdatePageLayout();
doc.UpdateFields();
doc.Save(ArtifactsDir + $"Field.INDEX.XE.Subheading.docx");
```

### Ver también

* class [FieldIndex](../)
* espacio de nombres [Aspose.Words.Fields](../../../aspose.words.fields/)
* asamblea [Aspose.Words](../../../)
