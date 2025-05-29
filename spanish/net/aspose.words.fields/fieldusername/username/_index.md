---
title: FieldUserName.UserName
linktitle: UserName
articleTitle: UserName
second_title: Aspose.Words para .NET
description: Administre fácilmente el nombre del usuario actual con la propiedad FieldUserName. Mejore la experiencia del usuario y personalice las interacciones sin problemas.
type: docs
weight: 20
url: /es/net/aspose.words.fields/fieldusername/username/
---
## FieldUserName.UserName property

Gest o establece el nombre del usuario actual.

```csharp
public string UserName { get; set; }
```

## Ejemplos

Muestra cómo utilizar el campo NOMBRE DE USUARIO.

```csharp
Document doc = new Document();

// Cree un objeto UserInformation y configúrelo como la fuente de información del usuario para cualquier campo que creemos.
UserInformation userInformation = new UserInformation();
userInformation.Name = "John Doe";
doc.FieldOptions.CurrentUser = userInformation;

DocumentBuilder builder = new DocumentBuilder(doc);

// Crea un campo NOMBRE DE USUARIO para mostrar el nombre del usuario actual,
// tomado del objeto UserInformation que creamos anteriormente.
FieldUserName fieldUserName = (FieldUserName)builder.InsertField(FieldType.FieldUserName, true);
Assert.AreEqual(userInformation.Name, fieldUserName.Result);

Assert.AreEqual(" USERNAME ", fieldUserName.GetFieldCode());
Assert.AreEqual("John Doe", fieldUserName.Result);

 //Podemos configurar esta propiedad para que nuestro campo anule el valor actualmente almacenado en el objeto UserInformation.
fieldUserName.UserName = "Jane Doe";
fieldUserName.Update();

Assert.AreEqual(" USERNAME  \"Jane Doe\"", fieldUserName.GetFieldCode());
Assert.AreEqual("Jane Doe", fieldUserName.Result);

// Esto no afecta el valor en el objeto UserInformation.
Assert.AreEqual("John Doe", doc.FieldOptions.CurrentUser.Name);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.USERNAME.docx");
```

### Ver también

* class [FieldUserName](../)
* espacio de nombres [Aspose.Words.Fields](../../../aspose.words.fields/)
* asamblea [Aspose.Words](../../../)
