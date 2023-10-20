---
title: FieldSubject.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words para .NET
description: FieldSubject Text propiedad. Obtiene o establece el texto del asunto en C#.
type: docs
weight: 20
url: /es/net/aspose.words.fields/fieldsubject/text/
---
## FieldSubject.Text property

Obtiene o establece el texto del asunto.

```csharp
public string Text { get; set; }
```

## Ejemplos

Muestra cómo utilizar el campo ASUNTO.

```csharp
Document doc = new Document();

// Establece un valor para la propiedad incorporada "Asunto" del documento.
doc.BuiltInDocumentProperties.Subject = "My subject";

// Crea un campo ASUNTO para mostrar el valor de esa propiedad incorporada.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldSubject field = (FieldSubject)builder.InsertField(FieldType.FieldSubject, true);
field.Update();

Assert.AreEqual(" SUBJECT ", field.GetFieldCode());
Assert.AreEqual("My subject", field.Result);

// Si le damos el valor de la propiedad Texto del campo ASUNTO y lo actualizamos, el campo
// sobrescribe el valor actual de la propiedad incorporada "Asunto" con el valor de su propiedad Texto,
// y luego mostrar el nuevo valor.
field.Text = "My new subject";
field.Update();

Assert.AreEqual(" SUBJECT  \"My new subject\"", field.GetFieldCode());
Assert.AreEqual("My new subject", field.Result);

Assert.AreEqual("My new subject", doc.BuiltInDocumentProperties.Subject);

doc.Save(ArtifactsDir + "Field.SUBJECT.docx");
```

### Ver también

* class [FieldSubject](../)
* espacio de nombres [Aspose.Words.Fields](../../../aspose.words.fields/)
* asamblea [Aspose.Words](../../../)
