---
title: "ContentDisposition"
linktitle: "ContentDisposition"
second_title: "Aspose.Words pour Java"
description: "Énumère les différentes manières de présenter le document dans le navigateur client en Java."
type: docs
weight: 126
url: /fr/java/com.aspose.words/contentdisposition/
---

**Inheritance:**
java.lang.Object
```
public class ContentDisposition
```

Énumère les différentes manières de présenter le document dans le navigateur client.

 **Remarks:** 

Notez que le comportement réel dans le navigateur client peut être affecté par la configuration de sécurité du navigateur.

 **Examples:** 

Montre comment effectuer une fusion de courrier, puis enregistrer le document dans le navigateur client.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.insertField(" MERGEFIELD FullName ");
 builder.insertParagraph();
 builder.insertField(" MERGEFIELD Company ");
 builder.insertParagraph();
 builder.insertField(" MERGEFIELD Address ");
 builder.insertParagraph();
 builder.insertField(" MERGEFIELD City ");

 doc.getMailMerge().execute(new String[]{"FullName", "Company", "Address", "City"},
         new Object[]{"James Bond", "MI5 Headquarters", "Milbank", "London"});
 
```
## Champs

| Champ | Description |
| --- | --- |
| [ATTACHMENT](#ATTACHMENT) | Envoyez le document au navigateur et proposez une option pour enregistrer le document sur le disque ou l'ouvrir dans l'application associée à l'extension du document. |
| [INLINE](#INLINE) | Envoyez le document au navigateur et proposez une option pour enregistrer le document sur le disque ou l'ouvrir dans le navigateur. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String contentDispositionName)](#fromName-java.lang.String) |  |
| [getName(int contentDisposition)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int contentDisposition)](#toString-int) |  |
### ATTACHMENT {#ATTACHMENT}
```
public static int ATTACHMENT
```


Envoyez le document au navigateur et proposez une option pour enregistrer le document sur le disque ou l'ouvrir dans l'application associée à l'extension du document.

### INLINE {#INLINE}
```
public static int INLINE
```


Envoyez le document au navigateur et proposez une option pour enregistrer le document sur le disque ou l'ouvrir dans le navigateur.

### length {#length}
```
public static int length
```


### fromName(String contentDispositionName) {#fromName-java.lang.String}
```
public static int fromName(String contentDispositionName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| contentDispositionName | java.lang.String |  |

**Returns:**
int
### getName(int contentDisposition) {#getName-int}
```
public static String getName(int contentDisposition)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| contentDisposition | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int contentDisposition) {#toString-int}
```
public static String toString(int contentDisposition)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| contentDisposition | int |  |

**Returns:**
java.lang.String
