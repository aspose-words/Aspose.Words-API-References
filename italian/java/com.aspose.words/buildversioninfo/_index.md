---
title: "BuildVersionInfo"
linktitle: "BuildVersionInfo"
second_title: "Aspose.Words per Java"
description: "Fornisce informazioni sul nome e sulla versione corrente del prodotto in Java."
type: docs
weight: 51
url: /it/java/com.aspose.words/buildversioninfo/
---

**Inheritance:**
java.lang.Object
```
public class BuildVersionInfo
```

Fornisce informazioni sul nome e sulla versione del prodotto corrente.

To learn more, visit the [ Generator or Producer Name Included in Output Documents ][Generator or Producer Name Included in Output Documents] documentation article.

 **Examples:** 

Mostra come visualizzare le informazioni sulla versione installata di **Aspose.Words**.

```

 System.out.println(MessageFormat.format("I am currently using {0}, version number {1}!", BuildVersionInfo.getProduct(), BuildVersionInfo.getVersion()));
 
```


[Generator or Producer Name Included in Output Documents]: https://docs.aspose.com/words/java/generator-or-producer-name-included-in-output-documents/
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [getProduct()](#getProduct) | Ottiene il nome completo del prodotto. |
| [getVersion()](#getVersion) | Ottiene la versione del prodotto. |
### getProduct() {#getProduct}
```
public static String getProduct()
```


Ottiene il nome completo del prodotto.

 **Examples:** 

Mostra come visualizzare le informazioni sulla versione installata di **Aspose.Words**.

```

 System.out.println(MessageFormat.format("I am currently using {0}, version number {1}!", BuildVersionInfo.getProduct(), BuildVersionInfo.getVersion()));
 
```

**Returns:**
java.lang.String - Il nome completo del prodotto.
### getVersion() {#getVersion}
```
public static String getVersion()
```


Ottiene la versione del prodotto.

 **Remarks:** 

La versione del prodotto è nel formato "Major.Minor.Hotfix.0".

 **Examples:** 

Mostra come visualizzare le informazioni sulla versione installata di **Aspose.Words**.

```

 System.out.println(MessageFormat.format("I am currently using {0}, version number {1}!", BuildVersionInfo.getProduct(), BuildVersionInfo.getVersion()));
 
```

**Returns:**
java.lang.String - La versione del prodotto.
