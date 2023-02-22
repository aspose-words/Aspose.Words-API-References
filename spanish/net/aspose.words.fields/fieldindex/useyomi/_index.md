---
title: FieldIndex.UseYomi
second_title: Referencia de API de Aspose.Words para .NET
description: FieldIndex propiedad. Obtiene o establece si habilitar el uso de yomi text para entradas de índice.
type: docs
weight: 170
url: /es/net/aspose.words.fields/fieldindex/useyomi/
---
## FieldIndex.UseYomi property

Obtiene o establece si habilitar el uso de yomi text para entradas de índice.

```csharp
public bool UseYomi { get; set; }
```

### Ejemplos

Muestra cómo ordenar fonéticamente las entradas del campo ÍNDICE.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Cree un campo ÍNDICE que mostrará una entrada para cada campo XE encontrado en el documento.
// Cada entrada mostrará el valor de la propiedad Texto del campo XE en el lado izquierdo,
// y el número de la página que contiene el campo XE a la derecha.
// La entrada ÍNDICE recopilará todos los campos XE con valores coincidentes en la propiedad "Texto"
// en una entrada en lugar de hacer una entrada para cada campo XE.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// La tabla ÍNDICE ordena automáticamente sus entradas por los valores de sus propiedades de Texto en orden alfabético.
// Configure la tabla ÍNDICE para ordenar las entradas fonéticamente usando Hiragana en su lugar.
index.UseYomi = sortEntriesUsingYomi;

if (sortEntriesUsingYomi)
    Assert.AreEqual(" INDEX  \\y", index.GetFieldCode());
else
    Assert.AreEqual(" INDEX ", index.GetFieldCode());

// Inserte 4 campos XE, que se mostrarían como entradas en la tabla de contenido del campo ÍNDICE.
// La propiedad "Texto" puede contener la ortografía de una palabra en Kanji, cuya pronunciación puede ser ambigua,
// mientras que la versión "Yomi" de la palabra se deletrea exactamente como se pronuncia usando Hiragana.
// Si configuramos nuestro campo ÍNDICE para usar Yomi, ordenará estas entradas
// por el valor de sus propiedades Yomi, en lugar de sus valores de Texto.
builder.InsertBreak(BreakType.PageBreak);
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "愛子";
indexEntry.Yomi = "あ";

Assert.AreEqual(" XE  愛子 \\y あ", indexEntry.GetFieldCode());

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "明美";
indexEntry.Yomi = "あ";

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "恵美";
indexEntry.Yomi = "え";

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "愛美";
indexEntry.Yomi = "え";

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.Yomi.docx");
```

### Ver también

* class [FieldIndex](../)
* espacio de nombres [Aspose.Words.Fields](../../fieldindex/)
* asamblea [Aspose.Words](../../../)


