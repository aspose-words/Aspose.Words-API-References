---
title: FieldComments.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words para .NET
description: Administre sus comentarios sin esfuerzo con la propiedad Texto FieldComments obtenga o configure fácilmente el texto del comentario para mejorar la interacción del usuario.
type: docs
weight: 20
url: /es/net/aspose.words.fields/fieldcomments/text/
---
## FieldComments.Text property

Obtiene o establece el texto de los comentarios.

```csharp
public string Text { get; set; }
```

## Ejemplos

Muestra cómo utilizar el campo COMENTARIOS.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Establezca un valor para la propiedad incorporada "Comentarios" del documento.
doc.BuiltInDocumentProperties.Comments = "My comment.";

// Cree un campo COMENTARIOS para mostrar el valor de esa propiedad incorporada.
FieldComments field = (FieldComments)builder.InsertField(FieldType.FieldComments, true);
field.Update();

Assert.AreEqual(" COMMENTS ", field.GetFieldCode());
Assert.AreEqual("My comment.", field.Result);

// Si le damos el valor de la propiedad Texto al campo COMENTARIOS y lo actualizamos, el campo
// sobrescribe el valor actual de la propiedad incorporada "Comentarios" con el valor de su propiedad Texto,
// y luego mostrar el nuevo valor.
field.Text = "My overriding comment.";
field.Update();

Assert.AreEqual(" COMMENTS  \"My overriding comment.\"", field.GetFieldCode());
Assert.AreEqual("My overriding comment.", field.Result);

doc.Save(ArtifactsDir + "Field.COMMENTS.docx");
```

### Ver también

* class [FieldComments](../)
* espacio de nombres [Aspose.Words.Fields](../../../aspose.words.fields/)
* asamblea [Aspose.Words](../../../)
