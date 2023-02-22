---
title: FieldQuote.Text
second_title: Referencia de API de Aspose.Words para .NET
description: FieldQuote propiedad. Obtiene o establece el texto a recuperar.
type: docs
weight: 20
url: /es/net/aspose.words.fields/fieldquote/text/
---
## FieldQuote.Text property

Obtiene o establece el texto a recuperar.

```csharp
public string Text { get; set; }
```

### Ejemplos

Muestra para usar el campo COTIZACIÓN.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserte un campo COTIZACIÓN, que mostrará el valor de su propiedad Texto.
FieldQuote field = (FieldQuote)builder.InsertField(FieldType.FieldQuote, true);
field.Text = "\"Quoted text\"";

Assert.AreEqual(" QUOTE  \"\\\"Quoted text\\\"\"", field.GetFieldCode());

// Inserta un campo de COTIZACIÓN y anida un campo de FECHA dentro de él.
// Los campos FECHA actualizan su valor a la fecha actual cada vez que abrimos el documento usando Microsoft Word.
// Anidar el campo FECHA dentro del campo COTIZACIÓN de esta manera congelará su valor
// hasta la fecha en que creamos el documento.
builder.Write("\nDocument creation date: ");
field = (FieldQuote)builder.InsertField(FieldType.FieldQuote, true);
builder.MoveTo(field.Separator);
builder.InsertField(FieldType.FieldDate, true);

Assert.AreEqual(" QUOTE \u0013 DATE \u0014" + DateTime.Now.Date.ToShortDateString() + "\u0015", field.GetFieldCode());

// Actualice todos los campos para mostrar sus resultados correctos.
doc.UpdateFields();

Assert.AreEqual("\"Quoted text\"", doc.Range.Fields[0].Result);

doc.Save(ArtifactsDir + "Field.QUOTE.docx");
```

### Ver también

* class [FieldQuote](../)
* espacio de nombres [Aspose.Words.Fields](../../fieldquote/)
* asamblea [Aspose.Words](../../../)


