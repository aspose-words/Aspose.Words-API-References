---
title: "BuildVersionInfo"
linktitle: "BuildVersionInfo"
second_title: "Aspose.Words для Java"
description: "Provides information about the current product name and version in Java."
type: docs
weight: 51
url: /ru/java/com.aspose.words/buildversioninfo/
---

**Inheritance:**
java.lang.Object
```
public class BuildVersionInfo
```

Предоставляет информацию о текущем названии продукта и его версии.

Чтобы узнать больше, посетите [ Generator or Producer Name Included in Output Documents ][Generator or Producer Name Included in Output Documents] статью документации.

 **Examples:** 

Показывает, как отобразить информацию о установленной версии Aspose.Words.

```

 System.out.println(MessageFormat.format("I am currently using {0}, version number {1}!", BuildVersionInfo.getProduct(), BuildVersionInfo.getVersion()));
 
```


[Generator or Producer Name Included in Output Documents]: https://docs.aspose.com/words/java/generator-or-producer-name-included-in-output-documents/
## Методы

| Метод | Описание |
| --- | --- |
| [getProduct()](#getProduct) | Получает полное название продукта. |
| [getVersion()](#getVersion) | Получает версию продукта. |
### getProduct() {#getProduct}
```
public static String getProduct()
```


Получает полное название продукта.

 **Examples:** 

Показывает, как отобразить информацию о установленной версии Aspose.Words.

```

 System.out.println(MessageFormat.format("I am currently using {0}, version number {1}!", BuildVersionInfo.getProduct(), BuildVersionInfo.getVersion()));
 
```

**Returns:**
java.lang.String - Полное название продукта.
### getVersion() {#getVersion}
```
public static String getVersion()
```


Получает версию продукта.

 **Remarks:** 

Версия продукта имеет формат "Major.Minor.Hotfix.0".

 **Examples:** 

Показывает, как отобразить информацию о установленной версии Aspose.Words.

```

 System.out.println(MessageFormat.format("I am currently using {0}, version number {1}!", BuildVersionInfo.getProduct(), BuildVersionInfo.getVersion()));
 
```

**Returns:**
java.lang.String - Версия продукта.
