---
title: FieldUserInitials.UserInitials
linktitle: UserInitials
articleTitle: UserInitials
second_title: Aspose.Words para .NET
description: FieldUserInitials UserInitials propiedad. Obtiene o establece las iniciales del usuario actual en C#.
type: docs
weight: 20
url: /es/net/aspose.words.fields/fielduserinitials/userinitials/
---
## FieldUserInitials.UserInitials property

Obtiene o establece las iniciales del usuario actual.

```csharp
public string UserInitials { get; set; }
```

## Ejemplos

Muestra cómo utilizar el campo USERINITIIALS.

```csharp
Document doc = new Document();

// Crea un objeto UserInformation y configúralo como fuente de información del usuario para cualquier campo que creemos.
UserInformation userInformation = new UserInformation();
userInformation.Initials = "J. D.";
doc.FieldOptions.CurrentUser = userInformation;

// Crea un campo USERINITIALES para mostrar las iniciales del usuario actual,
// tomado del objeto UserInformation que creamos anteriormente.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldUserInitials fieldUserInitials = (FieldUserInitials)builder.InsertField(FieldType.FieldUserInitials, true);
Assert.AreEqual(userInformation.Initials, fieldUserInitials.Result);

Assert.AreEqual(" USERINITIALS ", fieldUserInitials.GetFieldCode());
Assert.AreEqual("J. D.", fieldUserInitials.Result);

 // Podemos configurar esta propiedad para que nuestro campo anule el valor actualmente almacenado en el objeto UserInformation.
fieldUserInitials.UserInitials = "J. C.";
fieldUserInitials.Update();

Assert.AreEqual(" USERINITIALS  \"J. C.\"", fieldUserInitials.GetFieldCode());
Assert.AreEqual("J. C.", fieldUserInitials.Result);

// Esto no afecta el valor en el objeto UserInformation.
Assert.AreEqual("J. D.", doc.FieldOptions.CurrentUser.Initials);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.USERINITIALS.docx");
```

### Ver también

* class [FieldUserInitials](../)
* espacio de nombres [Aspose.Words.Fields](../../../aspose.words.fields/)
* asamblea [Aspose.Words](../../../)
