---
title: "UserInformation"
linktitle: "UserInformation"
second_title: "Aspose.Words pour Java"
description: "Spécifie les informations sur l'utilisateur en Java."
type: docs
weight: 702
url: /fr/java/com.aspose.words/userinformation/
---

**Inheritance:**
java.lang.Object
```
public class UserInformation
```

Spécifie les informations sur l'utilisateur.

Pour en savoir plus, consultez l'article de documentation [ Working with Fields ][Working with Fields].

 **Examples:** 

Montre comment définir les détails de l'utilisateur et les afficher à l'aide de champs.

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
## Méthodes

| Méthode | Description |
| --- | --- |
| [getAddress()](#getAddress) | Obtient l'adresse postale de l'utilisateur. |
| [getDefaultUser()](#getDefaultUser) | Informations utilisateur par défaut. |
| [getInitials()](#getInitials) | Obtient les initiales de l'utilisateur. |
| [getName()](#getName) | Obtient le nom de l'utilisateur. |
| [setAddress(String value)](#setAddress-java.lang.String) | Définit l'adresse postale de l'utilisateur. |
| [setInitials(String value)](#setInitials-java.lang.String) | Définit les initiales de l'utilisateur. |
| [setName(String value)](#setName-java.lang.String) | Définit le nom de l'utilisateur. |
### getAddress() {#getAddress}
```
public String getAddress()
```


Obtient l'adresse postale de l'utilisateur.

 **Examples:** 

Montre comment définir les détails de l'utilisateur et les afficher à l'aide de champs.

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
java.lang.String - L'adresse postale de l'utilisateur.
### getDefaultUser() {#getDefaultUser}
```
public static UserInformation getDefaultUser()
```


Informations utilisateur par défaut.

 **Remarks:** 

Utilisez la propriété [FieldOptions.getCurrentUser()](../../com.aspose.words/fieldoptions/\#getCurrentUser) / [FieldOptions.setCurrentUser(com.aspose.words.UserInformation)](../../com.aspose.words/fieldoptions/\#setCurrentUser-com.aspose.words.UserInformation) pour spécifier les informations de l'utilisateur pour un seul document.

 **Examples:** 

Montre comment définir les détails de l'utilisateur et les afficher à l'aide de champs.

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


Obtient les initiales de l'utilisateur.

 **Examples:** 

Montre comment définir les détails de l'utilisateur et les afficher à l'aide de champs.

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
java.lang.String - Les initiales de l'utilisateur.
### getName() {#getName}
```
public String getName()
```


Obtient le nom de l'utilisateur.

 **Examples:** 

Montre comment définir les détails de l'utilisateur et les afficher à l'aide de champs.

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
java.lang.String - Le nom de l'utilisateur.
### setAddress(String value) {#setAddress-java.lang.String}
```
public void setAddress(String value)
```


Définit l'adresse postale de l'utilisateur.

 **Examples:** 

Montre comment définir les détails de l'utilisateur et les afficher à l'aide de champs.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | java.lang.String | L'adresse postale de l'utilisateur. |

### setInitials(String value) {#setInitials-java.lang.String}
```
public void setInitials(String value)
```


Définit les initiales de l'utilisateur.

 **Examples:** 

Montre comment définir les détails de l'utilisateur et les afficher à l'aide de champs.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | java.lang.String | Les initiales de l'utilisateur. |

### setName(String value) {#setName-java.lang.String}
```
public void setName(String value)
```


Définit le nom de l'utilisateur.

 **Examples:** 

Montre comment définir les détails de l'utilisateur et les afficher à l'aide de champs.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | java.lang.String | Le nom de l'utilisateur. |

