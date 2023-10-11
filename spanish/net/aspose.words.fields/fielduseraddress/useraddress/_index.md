---
title: FieldUserAddress.UserAddress
second_title: Referencia de API de Aspose.Words para .NET
description: FieldUserAddress propiedad. Obtiene o establece la dirección postal del usuario actual.
type: docs
weight: 20
url: /es/net/aspose.words.fields/fielduseraddress/useraddress/
---
## FieldUserAddress.UserAddress property

Obtiene o establece la dirección postal del usuario actual.

```csharp
public string UserAddress { get; set; }
```

### Ejemplos

Muestra cómo utilizar el campo USERADDRESS.

```csharp
Document doc = new Document();

// Crea un objeto UserInformation y configúralo como fuente de información del usuario para cualquier campo que creemos.
UserInformation userInformation = new UserInformation();
userInformation.Address = "123 Main Street";
doc.FieldOptions.CurrentUser = userInformation;

// Crea un campo USERADDRESS para mostrar la dirección del usuario actual,
// tomado del objeto UserInformation que creamos anteriormente.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldUserAddress fieldUserAddress = (FieldUserAddress)builder.InsertField(FieldType.FieldUserAddress, true);
Assert.AreEqual(" USERADDRESS ", fieldUserAddress.GetFieldCode());
Assert.AreEqual("123 Main Street", fieldUserAddress.Result);

 // Podemos configurar esta propiedad para que nuestro campo anule el valor actualmente almacenado en el objeto UserInformation.
fieldUserAddress.UserAddress = "456 North Road";
fieldUserAddress.Update();

Assert.AreEqual(" USERADDRESS  \"456 North Road\"", fieldUserAddress.GetFieldCode());
Assert.AreEqual("456 North Road", fieldUserAddress.Result);

// Esto no afecta el valor en el objeto UserInformation.
Assert.AreEqual("123 Main Street", doc.FieldOptions.CurrentUser.Address);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.USERADDRESS.docx");
```

### Ver también

* class [FieldUserAddress](../)
* espacio de nombres [Aspose.Words.Fields](../../fielduseraddress/)
* asamblea [Aspose.Words](../../../)


