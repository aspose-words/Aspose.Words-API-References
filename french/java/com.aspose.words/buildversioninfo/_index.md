---
title: "BuildVersionInfo"
linktitle: "BuildVersionInfo"
second_title: "Aspose.Words pour Java"
description: "Fournit des informations sur le nom du produit actuel et sa version en Java."
type: docs
weight: 51
url: /fr/java/com.aspose.words/buildversioninfo/
---

**Inheritance:**
java.lang.Object
```
public class BuildVersionInfo
```

Fournit des informations sur le nom et la version du produit actuel.

Pour en savoir plus, consultez l'article de documentation [ Generator or Producer Name Included in Output Documents ][Generator or Producer Name Included in Output Documents].

 **Examples:** 

Montre comment afficher les informations sur la version installée d'Aspose.Words.

```

 System.out.println(MessageFormat.format("I am currently using {0}, version number {1}!", BuildVersionInfo.getProduct(), BuildVersionInfo.getVersion()));
 
```


[Generator or Producer Name Included in Output Documents]: https://docs.aspose.com/words/java/generator-or-producer-name-included-in-output-documents/
## Méthodes

| Méthode | Description |
| --- | --- |
| [getProduct()](#getProduct) | Obtient le nom complet du produit. |
| [getVersion()](#getVersion) | Obtient la version du produit. |
### getProduct() {#getProduct}
```
public static String getProduct()
```


Obtient le nom complet du produit.

 **Examples:** 

Montre comment afficher les informations sur la version installée d'Aspose.Words.

```

 System.out.println(MessageFormat.format("I am currently using {0}, version number {1}!", BuildVersionInfo.getProduct(), BuildVersionInfo.getVersion()));
 
```

**Returns:**
java.lang.String - Le nom complet du produit.
### getVersion() {#getVersion}
```
public static String getVersion()
```


Obtient la version du produit.

 **Remarks:** 

La version du produit est au format "Major.Minor.Hotfix.0".

 **Examples:** 

Montre comment afficher les informations sur la version installée d'Aspose.Words.

```

 System.out.println(MessageFormat.format("I am currently using {0}, version number {1}!", BuildVersionInfo.getProduct(), BuildVersionInfo.getVersion()));
 
```

**Returns:**
java.lang.String - La version du produit.
