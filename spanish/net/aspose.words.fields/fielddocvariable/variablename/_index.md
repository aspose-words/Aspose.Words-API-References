---
title: FieldDocVariable.VariableName
linktitle: VariableName
articleTitle: VariableName
second_title: Aspose.Words para .NET
description: Descubra la propiedad FieldDocVariableVariableName para gestionar fácilmente las variables de documentos. ¡Simplifique la recuperación y mejore la gestión de sus documentos hoy mismo!
type: docs
weight: 20
url: /es/net/aspose.words.fields/fielddocvariable/variablename/
---
## FieldDocVariable.VariableName property

Obtiene o establece el nombre de la variable del documento a recuperar.

```csharp
public string VariableName { get; set; }
```

## Ejemplos

Muestra cómo utilizar los campos DOCPROPERTY para mostrar propiedades y variables del documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// A continuación se muestran dos formas de utilizar los campos DOCPROPERTY.
// 1 - Mostrar una propiedad incorporada:
// Establezca un valor personalizado para la propiedad incorporada "Categoría", luego inserte un campo DOCPROPERTY que la haga referencia.
doc.BuiltInDocumentProperties.Category = "My category";

FieldDocProperty fieldDocProperty = (FieldDocProperty)builder.InsertField(" DOCPROPERTY Category ");
fieldDocProperty.Update();

Assert.AreEqual(" DOCPROPERTY Category ", fieldDocProperty.GetFieldCode());
Assert.AreEqual("My category", fieldDocProperty.Result);

builder.InsertParagraph();

// 2 - Mostrar una variable de documento personalizada:
// Defina una variable personalizada y luego haga referencia a esa variable con un campo DOCPROPERTY.
Assert.AreEqual(0, doc.Variables.Count);
doc.Variables.Add("My variable", "My variable's value");

FieldDocVariable fieldDocVariable = (FieldDocVariable)builder.InsertField(FieldType.FieldDocVariable, true);
fieldDocVariable.VariableName = "My Variable";
fieldDocVariable.Update();

Assert.AreEqual(" DOCVARIABLE  \"My Variable\"", fieldDocVariable.GetFieldCode());
Assert.AreEqual("My variable's value", fieldDocVariable.Result);

doc.Save(ArtifactsDir + "Field.DOCPROPERTY.DOCVARIABLE.docx");
```

### Ver también

* class [FieldDocVariable](../)
* espacio de nombres [Aspose.Words.Fields](../../../aspose.words.fields/)
* asamblea [Aspose.Words](../../../)
