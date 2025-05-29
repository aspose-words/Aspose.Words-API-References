---
title: FieldQuote.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words para .NET
description: Propiedad de texto de FieldQuote. Recupere o configure texto fácilmente para una mejor gestión de datos. ¡Optimice su flujo de trabajo con esta potente función!
type: docs
weight: 20
url: /es/net/aspose.words.fields/fieldquote/text/
---
## FieldQuote.Text property

Obtiene o establece el texto a recuperar.

```csharp
public string Text { get; set; }
```

## Ejemplos

Muestra cómo utilizar el campo QUOTE.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserte un campo QUOTE, que mostrará el valor de su propiedad Texto.
FieldQuote field = (FieldQuote)builder.InsertField(FieldType.FieldQuote, true);
field.Text = "\"Quoted text\"";

Assert.AreEqual(" QUOTE  \"\\\"Quoted text\\\"\"", field.GetFieldCode());

// Inserta un campo QUOTE y anida un campo DATE dentro de él.
// Los campos FECHA actualizan su valor a la fecha actual cada vez que abrimos el documento usando Microsoft Word.
// Anidar el campo FECHA dentro del campo COTIZACIÓN de esta manera congelará su valor
// a la fecha en que creamos el documento.
builder.Write("\nDocument creation date: ");
field = (FieldQuote)builder.InsertField(FieldType.FieldQuote, true);
builder.MoveTo(field.Separator);
builder.InsertField(FieldType.FieldDate, true);

Assert.AreEqual(" QUOTE \u0013 DATE \u0014" + DateTime.Now.Date.ToShortDateString() + "\u0015", field.GetFieldCode());

//Actualice todos los campos para mostrar sus resultados correctos.
doc.UpdateFields();

Assert.AreEqual("\"Quoted text\"", doc.Range.Fields[0].Result);

doc.Save(ArtifactsDir + "Field.QUOTE.docx");
```

### Ver también

* class [FieldQuote](../)
* espacio de nombres [Aspose.Words.Fields](../../../aspose.words.fields/)
* asamblea [Aspose.Words](../../../)
