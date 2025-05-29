---
title: FieldInfo.NewValue
linktitle: NewValue
articleTitle: NewValue
second_title: Aspose.Words para .NET
description: Descubra la propiedad NewValue de FieldInfo, administre fácilmente valores opcionales para mejorar sus actualizaciones de datos y agilizar su experiencia de codificación.
type: docs
weight: 30
url: /es/net/aspose.words.fields/fieldinfo/newvalue/
---
## FieldInfo.NewValue property

Obtiene o establece un valor opcional que actualiza la propiedad.

```csharp
public string NewValue { get; set; }
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
