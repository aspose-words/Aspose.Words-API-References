---
title: "UserInformation"
linktitle: "UserInformation"
second_title: "Aspose.Words Java için"
description: "Java'da kullanıcı hakkında bilgi belirtir."
type: docs
weight: 702
url: /tr/java/com.aspose.words/userinformation/
---

**Inheritance:**
java.lang.Object
```
public class UserInformation
```

Kullanıcı hakkında bilgi belirtir.

Daha fazla bilgi için, [ Working with Fields ][Working with Fields] dokümantasyon makalesini ziyaret edin.

 **Examples:** 

Kullanıcı detaylarını nasıl ayarlayacağınızı ve alanlar aracılığıyla nasıl görüntüleneceğini gösterir.

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
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [getAddress()](#getAddress) | Kullanıcının posta adresini alır. |
| [getDefaultUser()](#getDefaultUser) | Varsayılan kullanıcı bilgileri. |
| [getInitials()](#getInitials) | Kullanıcının baş harflerini alır. |
| [getName()](#getName) | Kullanıcının adını alır. |
| [setAddress(String value)](#setAddress-java.lang.String) | Kullanıcının posta adresini ayarlar. |
| [setInitials(String value)](#setInitials-java.lang.String) | Kullanıcının baş harflerini ayarlar. |
| [setName(String value)](#setName-java.lang.String) | Kullanıcının adını ayarlar. |
### getAddress() {#getAddress}
```
public String getAddress()
```


Kullanıcının posta adresini alır.

 **Examples:** 

Kullanıcı detaylarını nasıl ayarlayacağınızı ve alanlar aracılığıyla nasıl görüntüleneceğini gösterir.

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
java.lang.String - Kullanıcının posta adresi.
### getDefaultUser() {#getDefaultUser}
```
public static UserInformation getDefaultUser()
```


Varsayılan kullanıcı bilgileri.

 **Remarks:** 

Tek bir belge için kullanıcı bilgilerini belirtmek üzere [FieldOptions.getCurrentUser()](../../com.aspose.words/fieldoptions/\#getCurrentUser) / [FieldOptions.setCurrentUser(com.aspose.words.UserInformation)](../../com.aspose.words/fieldoptions/\#setCurrentUser-com.aspose.words.UserInformation) özelliğini kullanın.

 **Examples:** 

Kullanıcı detaylarını nasıl ayarlayacağınızı ve alanlar aracılığıyla nasıl görüntüleneceğini gösterir.

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


Kullanıcının baş harflerini alır.

 **Examples:** 

Kullanıcı detaylarını nasıl ayarlayacağınızı ve alanlar aracılığıyla nasıl görüntüleneceğini gösterir.

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
java.lang.String - Kullanıcının baş harfleri.
### getName() {#getName}
```
public String getName()
```


Kullanıcının adını alır.

 **Examples:** 

Kullanıcı detaylarını nasıl ayarlayacağınızı ve alanlar aracılığıyla nasıl görüntüleneceğini gösterir.

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
java.lang.String - Kullanıcının adı.
### setAddress(String value) {#setAddress-java.lang.String}
```
public void setAddress(String value)
```


Kullanıcının posta adresini ayarlar.

 **Examples:** 

Kullanıcı detaylarını nasıl ayarlayacağınızı ve alanlar aracılığıyla nasıl görüntüleneceğini gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | Kullanıcının posta adresi. |

### setInitials(String value) {#setInitials-java.lang.String}
```
public void setInitials(String value)
```


Kullanıcının baş harflerini ayarlar.

 **Examples:** 

Kullanıcı detaylarını nasıl ayarlayacağınızı ve alanlar aracılığıyla nasıl görüntüleneceğini gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | Kullanıcının baş harfleri. |

### setName(String value) {#setName-java.lang.String}
```
public void setName(String value)
```


Kullanıcının adını ayarlar.

 **Examples:** 

Kullanıcı detaylarını nasıl ayarlayacağınızı ve alanlar aracılığıyla nasıl görüntüleneceğini gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | Kullanıcının adı. |

