---
title: FieldTitle.Text
second_title: Referencia de API de Aspose.Words para .NET
description: FieldTitle propiedad. Obtiene o establece el texto del título.
type: docs
weight: 20
url: /es/net/aspose.words.fields/fieldtitle/text/
---
## FieldTitle.Text property

Obtiene o establece el texto del título.

```csharp
public string Text { get; set; }
```

### Ejemplos

Muestra cómo utilizar el campo TÍTULO.

```csharp
Document doc = new Document();

 // Establece un valor para la propiedad del documento incorporada "Título".
doc.BuiltInDocumentProperties.Title = "My Title";

// Podemos usar el campo TÍTULO para mostrar el valor de esta propiedad en el documento.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldTitle field = (FieldTitle)builder.InsertField(FieldType.FieldTitle, false);
field.Update();

Assert.AreEqual(" TITLE ", field.GetFieldCode());
Assert.AreEqual("My Title", field.Result);

// Estableciendo un valor para la propiedad Texto del campo,
// y luego actualizar el campo también sobrescribirá la propiedad incorporada correspondiente con el nuevo valor.
builder.Writeln();
field = (FieldTitle)builder.InsertField(FieldType.FieldTitle, false);
field.Text = "My New Title";
field.Update();

Assert.AreEqual(" TITLE  \"My New Title\"", field.GetFieldCode());
Assert.AreEqual("My New Title", field.Result);
Assert.AreEqual("My New Title", doc.BuiltInDocumentProperties.Title);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.TITLE.docx");
```

### Ver también

* class [FieldTitle](../)
* espacio de nombres [Aspose.Words.Fields](../../fieldtitle/)
* asamblea [Aspose.Words](../../../)


