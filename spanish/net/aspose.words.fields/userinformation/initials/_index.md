---
title: UserInformation.Initials
linktitle: Initials
articleTitle: Initials
second_title: Aspose.Words para .NET
description: Descubra cómo utilizar la propiedad Iniciales de UserInformation para administrar y personalizar fácilmente las iniciales del usuario para una mejor personalización y experiencia del usuario.
type: docs
weight: 40
url: /es/net/aspose.words.fields/userinformation/initials/
---
## UserInformation.Initials property

Obtiene o establece las iniciales del usuario.

```csharp
public string Initials { get; set; }
```

## Ejemplos

Muestra cómo configurar los detalles del usuario y mostrarlos mediante campos.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Cree un objeto UserInformation y configúrelo como fuente de datos para los campos que muestran información del usuario.
UserInformation userInformation = new UserInformation
{
    Name = "John Doe",
    Initials = "J. D.",
    Address = "123 Main Street"
};
doc.FieldOptions.CurrentUser = userInformation;

// Inserte los campos NOMBRE DE USUARIO, INICIALES DEL USUARIO y DIRECCIÓN DEL USUARIO, que muestran los valores de
 // las propiedades respectivas del objeto UserInformation que hemos creado anteriormente.
Assert.AreEqual(userInformation.Name, builder.InsertField(" USERNAME ").Result);
Assert.AreEqual(userInformation.Initials, builder.InsertField(" USERINITIALS ").Result);
Assert.AreEqual(userInformation.Address, builder.InsertField(" USERADDRESS ").Result);

// El objeto de opciones de campo también tiene un usuario predeterminado estático al que pueden hacer referencia los campos de todos los documentos.
UserInformation.DefaultUser.Name = "Default User";
UserInformation.DefaultUser.Initials = "D. U.";
UserInformation.DefaultUser.Address = "One Microsoft Way";
doc.FieldOptions.CurrentUser = UserInformation.DefaultUser;

Assert.AreEqual("Default User", builder.InsertField(" USERNAME ").Result);
Assert.AreEqual("D. U.", builder.InsertField(" USERINITIALS ").Result);
Assert.AreEqual("One Microsoft Way", builder.InsertField(" USERADDRESS ").Result);

doc.UpdateFields();
doc.Save(ArtifactsDir + "FieldOptions.CurrentUser.docx");
```

### Ver también

* class [UserInformation](../)
* espacio de nombres [Aspose.Words.Fields](../../../aspose.words.fields/)
* asamblea [Aspose.Words](../../../)
