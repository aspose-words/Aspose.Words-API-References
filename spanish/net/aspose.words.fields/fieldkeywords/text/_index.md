---
title: FieldKeywords.Text
second_title: Referencia de API de Aspose.Words para .NET
description: FieldKeywords propiedad. Obtiene o establece el texto de las palabras clave.
type: docs
weight: 20
url: /es/net/aspose.words.fields/fieldkeywords/text/
---
## FieldKeywords.Text property

Obtiene o establece el texto de las palabras clave.

```csharp
public string Text { get; set; }
```

### Ejemplos

Muestra para insertar un campo PALABRAS CLAVE.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Agregue algunas palabras clave, también denominadas "etiquetas" en el Explorador de archivos.
doc.BuiltInDocumentProperties.Keywords = "Keyword1, Keyword2";

// El campo PALABRAS CLAVE muestra el valor de esta propiedad.
FieldKeywords field = (FieldKeywords)builder.InsertField(FieldType.FieldKeyword, true);
field.Update();

Assert.AreEqual(" KEYWORDS ", field.GetFieldCode());
Assert.AreEqual("Keyword1, Keyword2", field.Result);

// Estableciendo un valor para la propiedad Texto del campo,
// y luego actualizar el campo también sobrescribirá la propiedad incorporada correspondiente con el nuevo valor.
field.Text = "OverridingKeyword";
field.Update();

Assert.AreEqual(" KEYWORDS  OverridingKeyword", field.GetFieldCode());
Assert.AreEqual("OverridingKeyword", field.Result);
Assert.AreEqual("OverridingKeyword", doc.BuiltInDocumentProperties.Keywords);

doc.Save(ArtifactsDir + "Field.KEYWORDS.docx");
```

### Ver también

* class [FieldKeywords](../)
* espacio de nombres [Aspose.Words.Fields](../../fieldkeywords/)
* asamblea [Aspose.Words](../../../)


