---
title: FieldXE.Yomi
second_title: Referencia de API de Aspose.Words para .NET
description: FieldXE propiedad. Obtiene o establece el yomi primer carácter fonético para ordenar índices para la entrada del índice
type: docs
weight: 80
url: /es/net/aspose.words.fields/fieldxe/yomi/
---
## FieldXE.Yomi property

Obtiene o establece el yomi (primer carácter fonético para ordenar índices) para la entrada del índice

```csharp
public string Yomi { get; set; }
```

### Ejemplos

Muestra cómo ordenar fonéticamente las entradas del campo ÍNDICE.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Cree un campo ÍNDICE que mostrará una entrada para cada campo XE que se encuentra en el documento.
// Cada entrada mostrará el valor de la propiedad Texto del campo XE en el lado izquierdo,
// y el número de la página que contiene el campo XE a la derecha.
// La entrada ÍNDICE recopilará todos los campos XE con valores coincidentes en la propiedad "Texto"
// en una entrada en lugar de hacer una entrada para cada campo XE.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// La tabla INDEX ordena automáticamente sus entradas por los valores de sus propiedades de Texto en orden alfabético.
// Configura la tabla INDEX para ordenar las entradas fonéticamente usando Hiragana.
index.UseYomi = sortEntriesUsingYomi;

if (sortEntriesUsingYomi)
    Assert.AreEqual(" INDEX  \\y", index.GetFieldCode());
else
    Assert.AreEqual(" INDEX ", index.GetFieldCode());

// Inserte 4 campos XE, que aparecerán como entradas en la tabla de contenido del campo ÍNDICE.
// La propiedad "Texto" puede contener la ortografía de una palabra en kanji, cuya pronunciación puede ser ambigua,
// mientras que la versión "Yomi" de la palabra se escribirá exactamente como se pronuncia usando Hiragana.
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

doc.UpdatePageLayout();
doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.Yomi.docx");
```

### Ver también

* class [FieldXE](../)
* espacio de nombres [Aspose.Words.Fields](../../fieldxe/)
* asamblea [Aspose.Words](../../../)


