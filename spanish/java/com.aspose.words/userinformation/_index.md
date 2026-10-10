---
title: "UserInformation"
linktitle: "UserInformation"
second_title: "Aspose.Words para Java"
description: "Especifica información sobre el usuario en Java."
type: docs
weight: 702
url: /es/java/com.aspose.words/userinformation/
---

**Inheritance:**
java.lang.Object
```
public class UserInformation
```

Especifica información sobre el usuario.

Para obtener más información, visite el artículo de documentación [ Working with Fields ][Working with Fields].

 **Examples:** 

Muestra cómo establecer los detalles del usuario y mostrarlos usando campos.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create a UserInformation object and set it as the data source for fields that display user information.
 UserInformation userInformation = new UserInformation();
 userInformation.setName("John Doe");
 userInformation.setInitials("J. D.");
 userInformation.setAddress("123 Main Street");
 doc.getFieldOptions().setCurrentUser(userInformation);

 // Insert USERNAME, USERINITIALS, and USERADDRESS fields, which display values of
 // the respective properties of the UserInformation object that we have created above.
 Assert.assertEquals(userInformation.getName(), builder.insertField(" USERNAME ").getResult());
 Assert.assertEquals(userInformation.getInitials(), builder.insertField(" USERINITIALS ").getResult());
 Assert.assertEquals(userInformation.getAddress(), builder.insertField(" USERADDRESS ").getResult());

 // The field options object also has a static default user that fields from all documents can refer to.
 UserInformation.getDefaultUser().setName("Default User");
 UserInformation.getDefaultUser().setInitials("D. U.");
 UserInformation.getDefaultUser().setAddress("One Microsoft Way");
 doc.getFieldOptions().setCurrentUser(UserInformation.getDefaultUser());

 Assert.assertEquals("Default User", builder.insertField(" USERNAME ").getResult());
 Assert.assertEquals("D. U.", builder.insertField(" USERINITIALS ").getResult());
 Assert.assertEquals("One Microsoft Way", builder.insertField(" USERADDRESS ").getResult());

 doc.updateFields();
 doc.save(getArtifactsDir() + "FieldOptions.CurrentUser.docx");
 
```


[Working with Fields]: https://docs.aspose.com/words/java/working-with-fields/
## Métodos

| Método | Descripción |
| --- | --- |
| [getAddress()](#getAddress) | Obtiene la dirección postal del usuario. |
| [getDefaultUser()](#getDefaultUser) | Información predeterminada del usuario. |
| [getInitials()](#getInitials) | Obtiene las iniciales del usuario. |
| [getName()](#getName) | Obtiene el nombre del usuario. |
| [setAddress(String value)](#setAddress-java.lang.String) | Establece la dirección postal del usuario. |
| [setInitials(String value)](#setInitials-java.lang.String) | Establece las iniciales del usuario. |
| [setName(String value)](#setName-java.lang.String) | Establece el nombre del usuario. |
### getAddress() {#getAddress}
```
public String getAddress()
```


Obtiene la dirección postal del usuario.

 **Examples:** 

Muestra cómo establecer los detalles del usuario y mostrarlos usando campos.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create a UserInformation object and set it as the data source for fields that display user information.
 UserInformation userInformation = new UserInformation();
 userInformation.setName("John Doe");
 userInformation.setInitials("J. D.");
 userInformation.setAddress("123 Main Street");
 doc.getFieldOptions().setCurrentUser(userInformation);

 // Insert USERNAME, USERINITIALS, and USERADDRESS fields, which display values of
 // the respective properties of the UserInformation object that we have created above.
 Assert.assertEquals(userInformation.getName(), builder.insertField(" USERNAME ").getResult());
 Assert.assertEquals(userInformation.getInitials(), builder.insertField(" USERINITIALS ").getResult());
 Assert.assertEquals(userInformation.getAddress(), builder.insertField(" USERADDRESS ").getResult());

 // The field options object also has a static default user that fields from all documents can refer to.
 UserInformation.getDefaultUser().setName("Default User");
 UserInformation.getDefaultUser().setInitials("D. U.");
 UserInformation.getDefaultUser().setAddress("One Microsoft Way");
 doc.getFieldOptions().setCurrentUser(UserInformation.getDefaultUser());

 Assert.assertEquals("Default User", builder.insertField(" USERNAME ").getResult());
 Assert.assertEquals("D. U.", builder.insertField(" USERINITIALS ").getResult());
 Assert.assertEquals("One Microsoft Way", builder.insertField(" USERADDRESS ").getResult());

 doc.updateFields();
 doc.save(getArtifactsDir() + "FieldOptions.CurrentUser.docx");
 
```

**Returns:**
java.lang.String - La dirección postal del usuario.
### getDefaultUser() {#getDefaultUser}
```
public static UserInformation getDefaultUser()
```


Información predeterminada del usuario.

 **Remarks:** 

Utiliza la propiedad [FieldOptions.getCurrentUser()](../../com.aspose.words/fieldoptions/\#getCurrentUser) / [FieldOptions.setCurrentUser(com.aspose.words.UserInformation)](../../com.aspose.words/fieldoptions/\#setCurrentUser-com.aspose.words.UserInformation) para especificar la información del usuario para un documento único.

 **Examples:** 

Muestra cómo establecer los detalles del usuario y mostrarlos usando campos.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create a UserInformation object and set it as the data source for fields that display user information.
 UserInformation userInformation = new UserInformation();
 userInformation.setName("John Doe");
 userInformation.setInitials("J. D.");
 userInformation.setAddress("123 Main Street");
 doc.getFieldOptions().setCurrentUser(userInformation);

 // Insert USERNAME, USERINITIALS, and USERADDRESS fields, which display values of
 // the respective properties of the UserInformation object that we have created above.
 Assert.assertEquals(userInformation.getName(), builder.insertField(" USERNAME ").getResult());
 Assert.assertEquals(userInformation.getInitials(), builder.insertField(" USERINITIALS ").getResult());
 Assert.assertEquals(userInformation.getAddress(), builder.insertField(" USERADDRESS ").getResult());

 // The field options object also has a static default user that fields from all documents can refer to.
 UserInformation.getDefaultUser().setName("Default User");
 UserInformation.getDefaultUser().setInitials("D. U.");
 UserInformation.getDefaultUser().setAddress("One Microsoft Way");
 doc.getFieldOptions().setCurrentUser(UserInformation.getDefaultUser());

 Assert.assertEquals("Default User", builder.insertField(" USERNAME ").getResult());
 Assert.assertEquals("D. U.", builder.insertField(" USERINITIALS ").getResult());
 Assert.assertEquals("One Microsoft Way", builder.insertField(" USERADDRESS ").getResult());

 doc.updateFields();
 doc.save(getArtifactsDir() + "FieldOptions.CurrentUser.docx");
 
```

**Returns:**
[UserInformation](../../com.aspose.words/userinformation/) - The corresponding [UserInformation](../../com.aspose.words/userinformation/) value.
### getInitials() {#getInitials}
```
public String getInitials()
```


Obtiene las iniciales del usuario.

 **Examples:** 

Muestra cómo establecer los detalles del usuario y mostrarlos usando campos.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create a UserInformation object and set it as the data source for fields that display user information.
 UserInformation userInformation = new UserInformation();
 userInformation.setName("John Doe");
 userInformation.setInitials("J. D.");
 userInformation.setAddress("123 Main Street");
 doc.getFieldOptions().setCurrentUser(userInformation);

 // Insert USERNAME, USERINITIALS, and USERADDRESS fields, which display values of
 // the respective properties of the UserInformation object that we have created above.
 Assert.assertEquals(userInformation.getName(), builder.insertField(" USERNAME ").getResult());
 Assert.assertEquals(userInformation.getInitials(), builder.insertField(" USERINITIALS ").getResult());
 Assert.assertEquals(userInformation.getAddress(), builder.insertField(" USERADDRESS ").getResult());

 // The field options object also has a static default user that fields from all documents can refer to.
 UserInformation.getDefaultUser().setName("Default User");
 UserInformation.getDefaultUser().setInitials("D. U.");
 UserInformation.getDefaultUser().setAddress("One Microsoft Way");
 doc.getFieldOptions().setCurrentUser(UserInformation.getDefaultUser());

 Assert.assertEquals("Default User", builder.insertField(" USERNAME ").getResult());
 Assert.assertEquals("D. U.", builder.insertField(" USERINITIALS ").getResult());
 Assert.assertEquals("One Microsoft Way", builder.insertField(" USERADDRESS ").getResult());

 doc.updateFields();
 doc.save(getArtifactsDir() + "FieldOptions.CurrentUser.docx");
 
```

**Returns:**
java.lang.String - Las iniciales del usuario.
### getName() {#getName}
```
public String getName()
```


Obtiene el nombre del usuario.

 **Examples:** 

Muestra cómo establecer los detalles del usuario y mostrarlos usando campos.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create a UserInformation object and set it as the data source for fields that display user information.
 UserInformation userInformation = new UserInformation();
 userInformation.setName("John Doe");
 userInformation.setInitials("J. D.");
 userInformation.setAddress("123 Main Street");
 doc.getFieldOptions().setCurrentUser(userInformation);

 // Insert USERNAME, USERINITIALS, and USERADDRESS fields, which display values of
 // the respective properties of the UserInformation object that we have created above.
 Assert.assertEquals(userInformation.getName(), builder.insertField(" USERNAME ").getResult());
 Assert.assertEquals(userInformation.getInitials(), builder.insertField(" USERINITIALS ").getResult());
 Assert.assertEquals(userInformation.getAddress(), builder.insertField(" USERADDRESS ").getResult());

 // The field options object also has a static default user that fields from all documents can refer to.
 UserInformation.getDefaultUser().setName("Default User");
 UserInformation.getDefaultUser().setInitials("D. U.");
 UserInformation.getDefaultUser().setAddress("One Microsoft Way");
 doc.getFieldOptions().setCurrentUser(UserInformation.getDefaultUser());

 Assert.assertEquals("Default User", builder.insertField(" USERNAME ").getResult());
 Assert.assertEquals("D. U.", builder.insertField(" USERINITIALS ").getResult());
 Assert.assertEquals("One Microsoft Way", builder.insertField(" USERADDRESS ").getResult());

 doc.updateFields();
 doc.save(getArtifactsDir() + "FieldOptions.CurrentUser.docx");
 
```

**Returns:**
java.lang.String - El nombre del usuario.
### setAddress(String value) {#setAddress-java.lang.String}
```
public void setAddress(String value)
```


Establece la dirección postal del usuario.

 **Examples:** 

Muestra cómo establecer los detalles del usuario y mostrarlos usando campos.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create a UserInformation object and set it as the data source for fields that display user information.
 UserInformation userInformation = new UserInformation();
 userInformation.setName("John Doe");
 userInformation.setInitials("J. D.");
 userInformation.setAddress("123 Main Street");
 doc.getFieldOptions().setCurrentUser(userInformation);

 // Insert USERNAME, USERINITIALS, and USERADDRESS fields, which display values of
 // the respective properties of the UserInformation object that we have created above.
 Assert.assertEquals(userInformation.getName(), builder.insertField(" USERNAME ").getResult());
 Assert.assertEquals(userInformation.getInitials(), builder.insertField(" USERINITIALS ").getResult());
 Assert.assertEquals(userInformation.getAddress(), builder.insertField(" USERADDRESS ").getResult());

 // The field options object also has a static default user that fields from all documents can refer to.
 UserInformation.getDefaultUser().setName("Default User");
 UserInformation.getDefaultUser().setInitials("D. U.");
 UserInformation.getDefaultUser().setAddress("One Microsoft Way");
 doc.getFieldOptions().setCurrentUser(UserInformation.getDefaultUser());

 Assert.assertEquals("Default User", builder.insertField(" USERNAME ").getResult());
 Assert.assertEquals("D. U.", builder.insertField(" USERINITIALS ").getResult());
 Assert.assertEquals("One Microsoft Way", builder.insertField(" USERADDRESS ").getResult());

 doc.updateFields();
 doc.save(getArtifactsDir() + "FieldOptions.CurrentUser.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.lang.String | La dirección postal del usuario. |

### setInitials(String value) {#setInitials-java.lang.String}
```
public void setInitials(String value)
```


Establece las iniciales del usuario.

 **Examples:** 

Muestra cómo establecer los detalles del usuario y mostrarlos usando campos.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create a UserInformation object and set it as the data source for fields that display user information.
 UserInformation userInformation = new UserInformation();
 userInformation.setName("John Doe");
 userInformation.setInitials("J. D.");
 userInformation.setAddress("123 Main Street");
 doc.getFieldOptions().setCurrentUser(userInformation);

 // Insert USERNAME, USERINITIALS, and USERADDRESS fields, which display values of
 // the respective properties of the UserInformation object that we have created above.
 Assert.assertEquals(userInformation.getName(), builder.insertField(" USERNAME ").getResult());
 Assert.assertEquals(userInformation.getInitials(), builder.insertField(" USERINITIALS ").getResult());
 Assert.assertEquals(userInformation.getAddress(), builder.insertField(" USERADDRESS ").getResult());

 // The field options object also has a static default user that fields from all documents can refer to.
 UserInformation.getDefaultUser().setName("Default User");
 UserInformation.getDefaultUser().setInitials("D. U.");
 UserInformation.getDefaultUser().setAddress("One Microsoft Way");
 doc.getFieldOptions().setCurrentUser(UserInformation.getDefaultUser());

 Assert.assertEquals("Default User", builder.insertField(" USERNAME ").getResult());
 Assert.assertEquals("D. U.", builder.insertField(" USERINITIALS ").getResult());
 Assert.assertEquals("One Microsoft Way", builder.insertField(" USERADDRESS ").getResult());

 doc.updateFields();
 doc.save(getArtifactsDir() + "FieldOptions.CurrentUser.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.lang.String | Las iniciales del usuario. |

### setName(String value) {#setName-java.lang.String}
```
public void setName(String value)
```


Establece el nombre del usuario.

 **Examples:** 

Muestra cómo establecer los detalles del usuario y mostrarlos usando campos.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create a UserInformation object and set it as the data source for fields that display user information.
 UserInformation userInformation = new UserInformation();
 userInformation.setName("John Doe");
 userInformation.setInitials("J. D.");
 userInformation.setAddress("123 Main Street");
 doc.getFieldOptions().setCurrentUser(userInformation);

 // Insert USERNAME, USERINITIALS, and USERADDRESS fields, which display values of
 // the respective properties of the UserInformation object that we have created above.
 Assert.assertEquals(userInformation.getName(), builder.insertField(" USERNAME ").getResult());
 Assert.assertEquals(userInformation.getInitials(), builder.insertField(" USERINITIALS ").getResult());
 Assert.assertEquals(userInformation.getAddress(), builder.insertField(" USERADDRESS ").getResult());

 // The field options object also has a static default user that fields from all documents can refer to.
 UserInformation.getDefaultUser().setName("Default User");
 UserInformation.getDefaultUser().setInitials("D. U.");
 UserInformation.getDefaultUser().setAddress("One Microsoft Way");
 doc.getFieldOptions().setCurrentUser(UserInformation.getDefaultUser());

 Assert.assertEquals("Default User", builder.insertField(" USERNAME ").getResult());
 Assert.assertEquals("D. U.", builder.insertField(" USERINITIALS ").getResult());
 Assert.assertEquals("One Microsoft Way", builder.insertField(" USERADDRESS ").getResult());

 doc.updateFields();
 doc.save(getArtifactsDir() + "FieldOptions.CurrentUser.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.lang.String | El nombre del usuario. |

