---
title: "Lisans"
linktitle: "Lisans"
second_title: "Aspose.Words Java için"
description: "Java'da bileşeni lisanslamak için yöntemler sağlar."
type: docs
weight: 421
url: /tr/java/com.aspose.words/license/
---

**Inheritance:**
java.lang.Object
```
public class License
```

Bileşeni lisanslamak için yöntemler sağlar.

Daha fazla bilgi edinmek için, [ Licensing and Subscription ][Licensing and Subscription] dokümantasyon makalesini ziyaret edin.

 **Examples:** 

Yerel dosya sistemindeki bir lisans dosyası kullanarak Aspose.Words için bir lisansın nasıl başlatılacağını gösterir.

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
## Yapıcılar

| Yapıcı | Açıklama |
| --- | --- |
| [License()](#License) | Bu sınıfın yeni bir örneğini başlatır. |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [setLicense(InputStream stream)](#setLicense-java.io.InputStream) |  |
| [setLicense(String licenseName)](#setLicense-java.lang.String) | Bileşeni lisanslar. |
### License() {#License}
```
public License()
```


Bu sınıfın yeni bir örneğini başlatır.

 **Examples:** 

Yerel dosya sistemindeki bir lisans dosyası kullanarak Aspose.Words için bir lisansın nasıl başlatılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| stream | java.io.InputStream |  |

### setLicense(String licenseName) {#setLicense-java.lang.String}
```
public void setLicense(String licenseName)
```


Bileşeni lisanslar.

 **Remarks:** 

Lisansı aşağıdaki konumlarda bulmaya çalışır:

1. Açık yol.

2. Aspose bileşeni JAR dosyasını içeren klasör.

3. İstemcinin çağıran JAR dosyasını içeren klasör.

 **Examples:** 

Yerel dosya sistemindeki bir lisans dosyası kullanarak Aspose.Words için bir lisansın nasıl başlatılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| licenseName | java.lang.String | Tam veya kısa bir dosya adı olabilir. Değerlendirme moduna geçmek için boş bir dize kullanın. |

