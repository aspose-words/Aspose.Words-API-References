---
title: Class UserInformation
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Fields.UserInformation clase. Especifica información sobre el usuario.
type: docs
weight: 2790
url: /es/net/aspose.words.fields/userinformation/
---
## UserInformation class

Especifica información sobre el usuario.

Para obtener más información, visite el[Trabajar con campos](https://docs.aspose.com/words/net/working-with-fields/) artículo de documentación.

```csharp
public class UserInformation
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [UserInformation](userinformation/)() | Constructor predeterminado |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| static [DefaultUser](../../aspose.words.fields/userinformation/defaultuser/) { get; } | Información de usuario predeterminada. |
| [Address](../../aspose.words.fields/userinformation/address/) { get; set; } | Obtiene o establece la dirección postal del usuario. |
| [Initials](../../aspose.words.fields/userinformation/initials/) { get; set; } | Obtiene o establece las iniciales del usuario. |
| [Name](../../aspose.words.fields/userinformation/name/) { get; set; } | Obtiene o establece el nombre del usuario. |

### Ejemplos

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

// Inserte los campos NOMBRE DE USUARIO, INICIALES DE USUARIO y DIRECCIÓN DE USUARIO, que muestran valores de
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

* espacio de nombres [Aspose.Words.Fields](../../aspose.words.fields/)
* asamblea [Aspose.Words](../../)


