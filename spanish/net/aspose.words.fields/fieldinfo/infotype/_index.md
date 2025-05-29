---
title: FieldInfo.InfoType
linktitle: InfoType
articleTitle: InfoType
second_title: Aspose.Words para .NET
description: Descubra cómo gestionar fácilmente las propiedades de InfoType de FieldInfo. Configure o recupere fácilmente tipos de documentos para una integración perfecta en sus proyectos.
type: docs
weight: 20
url: /es/net/aspose.words.fields/fieldinfo/infotype/
---
## FieldInfo.InfoType property

Obtiene o establece el tipo de propiedad del documento que se va a insertar.

```csharp
public string InfoType { get; set; }
```

## Ejemplos

Muestra cómo trabajar con campos INFO.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Establezca un valor para la propiedad incorporada "Comentarios" y luego inserte un campo INFO para mostrar el valor de esa propiedad.
doc.BuiltInDocumentProperties.Comments = "My comment";
FieldInfo field = (FieldInfo)builder.InsertField(FieldType.FieldInfo, true);
field.InfoType = "Comments";
field.Update();

Assert.AreEqual(" INFO  Comments", field.GetFieldCode());
Assert.AreEqual("My comment", field.Result);

builder.Writeln();

// Establecer un valor para la propiedad NewValue del campo y actualizar
// el campo también sobrescribirá la propiedad incorporada correspondiente con el nuevo valor.
field = (FieldInfo)builder.InsertField(FieldType.FieldInfo, true);
field.InfoType = "Comments";
field.NewValue = "New comment";
field.Update();

Assert.AreEqual(" INFO  Comments \"New comment\"", field.GetFieldCode());
Assert.AreEqual("New comment", field.Result);
Assert.AreEqual("New comment", doc.BuiltInDocumentProperties.Comments);

doc.Save(ArtifactsDir + "Field.INFO.docx");
```

### Ver también

* class [FieldInfo](../)
* espacio de nombres [Aspose.Words.Fields](../../../aspose.words.fields/)
* asamblea [Aspose.Words](../../../)
