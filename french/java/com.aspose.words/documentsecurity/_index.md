---
title: "DocumentSecurity"
linktitle: "DocumentSecurity"
second_title: "Aspose.Words pour Java"
description: "Utilisé comme valeur pour la propriété BuiltInDocumentProperties.getSecurity / BuiltInDocumentProperties.setSecurityint en Java."
type: docs
weight: 173
url: /fr/java/com.aspose.words/documentsecurity/
---

**Inheritance:**
java.lang.Object
```
public class DocumentSecurity
```

Utilisé comme valeur pour la propriété [BuiltInDocumentProperties.getSecurity()](../../com.aspose.words/builtindocumentproperties/\\#getSecurity) / [BuiltInDocumentProperties.setSecurity(int)](../../com.aspose.words/builtindocumentproperties/\\#setSecurity-int). Spécifie le niveau de sécurité d'un document sous forme de valeur numérique.

 **Examples:** 

Montre comment utiliser les propriétés du document pour afficher le niveau de sécurité d'un document.

```

 Document doc = new Document();

 Assert.assertEquals(DocumentSecurity.NONE, doc.getBuiltInDocumentProperties().getSecurity());

 // If we configure a document to be read-only, it will display this status using the "Security" built-in property.
 doc.getWriteProtection().setReadOnlyRecommended(true);
 doc.save(getArtifactsDir() + "DocumentProperties.Security.ReadOnlyRecommended.docx");

 Assert.assertEquals(DocumentSecurity.READ_ONLY_RECOMMENDED,
         new Document(getArtifactsDir() + "DocumentProperties.Security.ReadOnlyRecommended.docx").getBuiltInDocumentProperties().getSecurity());

 // Write-protect a document, and then verify its security level.
 doc = new Document();

 Assert.assertFalse(doc.getWriteProtection().isWriteProtected());

 doc.getWriteProtection().setPassword("MyPassword");

 Assert.assertTrue(doc.getWriteProtection().validatePassword("MyPassword"));
 Assert.assertTrue(doc.getWriteProtection().isWriteProtected());

 doc.save(getArtifactsDir() + "DocumentProperties.Security.ReadOnlyEnforced.docx");

 Assert.assertEquals(DocumentSecurity.READ_ONLY_ENFORCED,
         new Document(getArtifactsDir() + "DocumentProperties.Security.ReadOnlyEnforced.docx").getBuiltInDocumentProperties().getSecurity());

 // "Security" is a descriptive property. We can edit its value manually.
 doc = new Document();

 doc.protect(ProtectionType.ALLOW_ONLY_COMMENTS, "MyPassword");
 doc.getBuiltInDocumentProperties().setSecurity(DocumentSecurity.READ_ONLY_EXCEPT_ANNOTATIONS);
 doc.save(getArtifactsDir() + "DocumentProperties.Security.ReadOnlyExceptAnnotations.docx");

 Assert.assertEquals(DocumentSecurity.READ_ONLY_EXCEPT_ANNOTATIONS,
         new Document(getArtifactsDir() + "DocumentProperties.Security.ReadOnlyExceptAnnotations.docx").getBuiltInDocumentProperties().getSecurity());
 
```
## Champs

| Champ | Description |
| --- | --- |
| [NONE](#NONE) | Aucun état de sécurité n'est spécifié par la propriété. |
| [PASSWORD_PROTECTED](#PASSWORD-PROTECTED) | Le document est protégé par mot de passe. |
| [READ_ONLY_ENFORCED](#READ-ONLY-ENFORCED) | Le document doit toujours être ouvert en lecture seule. |
| [READ_ONLY_EXCEPT_ANNOTATIONS](#READ-ONLY-EXCEPT-ANNOTATIONS) | Le document doit toujours être ouvert en lecture seule, sauf pour les annotations. |
| [READ_ONLY_RECOMMENDED](#READ-ONLY-RECOMMENDED) | Le document doit être ouvert en lecture seule si possible, mais le paramètre peut être remplacé. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String documentSecurityName)](#fromName-java.lang.String) |  |
| [fromNames(Set documentSecurityNames)](#fromNames-java.util.Set) |  |
| [getName(int documentSecurity)](#getName-int) |  |
| [getNames(int documentSecurity)](#getNames-int) |  |
| [getValues()](#getValues) |  |
| [toString(int documentSecurity)](#toString-int) |  |
| [toStringSet(int attr)](#toStringSet-int) |  |
### NONE {#NONE}
```
public static int NONE
```


Aucun état de sécurité n'est spécifié par la propriété.

### PASSWORD_PROTECTED {#PASSWORD-PROTECTED}
```
public static int PASSWORD_PROTECTED
```


Le document est protégé par mot de passe. (Remarque : cela n'a jamais été observé dans un document jusqu'à présent).

### READ_ONLY_ENFORCED {#READ-ONLY-ENFORCED}
```
public static int READ_ONLY_ENFORCED
```


Le document doit toujours être ouvert en lecture seule.

### READ_ONLY_EXCEPT_ANNOTATIONS {#READ-ONLY-EXCEPT-ANNOTATIONS}
```
public static int READ_ONLY_EXCEPT_ANNOTATIONS
```


Le document doit toujours être ouvert en lecture seule, sauf pour les annotations.

### READ_ONLY_RECOMMENDED {#READ-ONLY-RECOMMENDED}
```
public static int READ_ONLY_RECOMMENDED
```


Le document doit être ouvert en lecture seule si possible, mais le paramètre peut être remplacé.

### length {#length}
```
public static int length
```


### fromName(String documentSecurityName) {#fromName-java.lang.String}
```
public static int fromName(String documentSecurityName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| documentSecurityName | java.lang.String |  |

**Returns:**
int
### fromNames(Set documentSecurityNames) {#fromNames-java.util.Set}
```
public static int fromNames(Set documentSecurityNames)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| documentSecurityNames | java.util.Set |  |

**Returns:**
int
### getName(int documentSecurity) {#getName-int}
```
public static String getName(int documentSecurity)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| documentSecurity | int |  |

**Returns:**
java.lang.String
### getNames(int documentSecurity) {#getNames-int}
```
public static Set getNames(int documentSecurity)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| documentSecurity | int |  |

**Returns:**
java.util.Set
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int documentSecurity) {#toString-int}
```
public static String toString(int documentSecurity)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| documentSecurity | int |  |

**Returns:**
java.lang.String
### toStringSet(int attr) {#toStringSet-int}
```
public static String toStringSet(int attr)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| attr | int |  |

**Returns:**
java.lang.String
