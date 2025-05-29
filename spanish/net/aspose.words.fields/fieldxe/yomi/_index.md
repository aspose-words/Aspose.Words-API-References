---
title: FieldXE.Yomi
linktitle: Yomi
articleTitle: Yomi
second_title: Aspose.Words para .NET
description: Optimice sus entradas de índice con la propiedad FieldXE Yomi, que permite una clasificación eficiente utilizando el primer carácter fonético para una mejor organización de los datos.
type: docs
weight: 80
url: /es/net/aspose.words.fields/fieldxe/yomi/
---
## FieldXE.Yomi property

Obtiene o establece el yomi (primer carácter fonético para ordenar índices) para la entrada de índice

```csharp
public string Yomi { get; set; }
```

## Ejemplos

Muestra cómo ordenar las entradas del campo ÍNDICE fonéticamente.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Cree un campo INDEX que mostrará una entrada para cada campo XE encontrado en el documento.
// Cada entrada mostrará el valor de la propiedad de Texto del campo XE en el lado izquierdo,
// y el número de la página que contiene el campo XE a la derecha.
// La entrada INDEX recopilará todos los campos XE con valores coincidentes en la propiedad "Texto"
// en una sola entrada en lugar de hacer una entrada para cada campo XE.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

//La tabla INDEX ordena automáticamente sus entradas por los valores de sus propiedades de Texto en orden alfabético.
// Configure la tabla INDEX para ordenar las entradas fonéticamente usando Hiragana en su lugar.
index.UseYomi = sortEntriesUsingYomi;

if (sortEntriesUsingYomi)
    Assert.AreEqual(" INDEX  \\y", index.GetFieldCode());
else
    Assert.AreEqual(" INDEX ", index.GetFieldCode());

// Inserte 4 campos XE, que se mostrarán como entradas en la tabla de contenido del campo ÍNDICE.
// La propiedad "Texto" puede contener la ortografía de una palabra en kanji, cuya pronunciación puede ser ambigua,
// mientras que la versión "Yomi" de la palabra se escribirá exactamente como se pronuncia usando Hiragana.
// Si configuramos nuestro campo ÍNDICE para usar Yomi, ordenará estas entradas
// por el valor de sus propiedades Yomi, en lugar de sus valores de texto.
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
* espacio de nombres [Aspose.Words.Fields](../../../aspose.words.fields/)
* asamblea [Aspose.Words](../../../)
