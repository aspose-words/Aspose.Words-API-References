---
title: "Лицензия"
linktitle: "Лицензия"
second_title: "Aspose.Words для Java"
description: "Предоставляет методы для лицензирования компонента в Java."
type: docs
weight: 421
url: /ru/java/com.aspose.words/license/
---

**Inheritance:**
java.lang.Object
```
public class License
```

Предоставляет методы для лицензирования компонента.

Чтобы узнать больше, посетите [ Licensing and Subscription ][Licensing and Subscription] статью документации.

 **Examples:** 

Показывает, как инициализировать лицензию для Aspose.Words, используя файл лицензии в локальной файловой системе.

```

 // Set the license for our Aspose.Words product by passing the local file system filename of a valid license file.
 Path licenseFileName = Paths.get(getLicenseDir(), "Aspose.Words.Java.lic");

 License license = new License();
 license.setLicense(licenseFileName.toString());

 // Create a copy of our license file in the binaries folder of our application.
 Path licenseCopyFileName = Paths.get(System.getProperty("user.dir"), "Aspose.Words.Java.lic");
 FileUtils.copyFile(new File(licenseFileName.toString()), new File(licenseCopyFileName.toString()));

 // If we pass a file's name without a path,
 // the SetLicense will search several local file system locations for this file.
 // One of those locations will be the "bin" folder, which contains a copy of our license file.
 license.setLicense("Aspose.Words.Java.lic");
 
```


[Licensing and Subscription]: https://docs.aspose.com/words/java/licensing/
## Конструкторы

| Конструктор | Описание |
| --- | --- |
| [License()](#License) | Инициализирует новый экземпляр этого класса. |
## Методы

| Метод | Описание |
| --- | --- |
| [setLicense(InputStream stream)](#setLicense-java.io.InputStream) |  |
| [setLicense(String licenseName)](#setLicense-java.lang.String) | Лицензирует компонент. |
### License() {#License}
```
public License()
```


Инициализирует новый экземпляр этого класса.

 **Examples:** 

Показывает, как инициализировать лицензию для Aspose.Words, используя файл лицензии в локальной файловой системе.

```

 // Set the license for our Aspose.Words product by passing the local file system filename of a valid license file.
 Path licenseFileName = Paths.get(getLicenseDir(), "Aspose.Words.Java.lic");

 License license = new License();
 license.setLicense(licenseFileName.toString());

 // Create a copy of our license file in the binaries folder of our application.
 Path licenseCopyFileName = Paths.get(System.getProperty("user.dir"), "Aspose.Words.Java.lic");
 FileUtils.copyFile(new File(licenseFileName.toString()), new File(licenseCopyFileName.toString()));

 // If we pass a file's name without a path,
 // the SetLicense will search several local file system locations for this file.
 // One of those locations will be the "bin" folder, which contains a copy of our license file.
 license.setLicense("Aspose.Words.Java.lic");
 
```

### setLicense(InputStream stream) {#setLicense-java.io.InputStream}
```
public void setLicense(InputStream stream)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| stream | java.io.InputStream |  |

### setLicense(String licenseName) {#setLicense-java.lang.String}
```
public void setLicense(String licenseName)
```


Лицензирует компонент.

 **Remarks:** 

Пытается найти лицензию в следующих местах:

1. Явный путь.

2. Папка, содержащая JAR‑файл компонента Aspose.

3. Папка, содержащая JAR‑файл, вызываемый клиентом.

 **Examples:** 

Показывает, как инициализировать лицензию для Aspose.Words, используя файл лицензии в локальной файловой системе.

```

 // Set the license for our Aspose.Words product by passing the local file system filename of a valid license file.
 Path licenseFileName = Paths.get(getLicenseDir(), "Aspose.Words.Java.lic");

 License license = new License();
 license.setLicense(licenseFileName.toString());

 // Create a copy of our license file in the binaries folder of our application.
 Path licenseCopyFileName = Paths.get(System.getProperty("user.dir"), "Aspose.Words.Java.lic");
 FileUtils.copyFile(new File(licenseFileName.toString()), new File(licenseCopyFileName.toString()));

 // If we pass a file's name without a path,
 // the SetLicense will search several local file system locations for this file.
 // One of those locations will be the "bin" folder, which contains a copy of our license file.
 license.setLicense("Aspose.Words.Java.lic");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| licenseName | java.lang.String | Может быть полным или коротким именем файла. Используйте пустую строку, чтобы переключиться в режим оценки. |

