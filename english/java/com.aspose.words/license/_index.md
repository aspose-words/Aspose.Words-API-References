---
title: License
linktitle: License
second_title: Aspose.Words for Java
description: Provides methods to license the component in Java.
type: docs
weight: 410
url: /java/com.aspose.words/license/
---

**Inheritance:**
java.lang.Object
```
public class License
```

Provides methods to license the component.

To learn more, visit the [ Licensing and Subscription ][Licensing and Subscription] documentation article.

 **Examples:** 

Shows how initialize a license for Aspose.Words using a license file in the local file system.

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
## Constructors

| Constructor | Description |
| --- | --- |
| [License()](#License) | Initializes a new instance of this class. |
## Methods

| Method | Description |
| --- | --- |
| [setLicense(InputStream stream)](#setLicense-java.io.InputStream) |  |
| [setLicense(String licenseName)](#setLicense-java.lang.String) | Licenses the component. |
### License() {#License}
```
public License()
```


Initializes a new instance of this class.

 **Examples:** 

Shows how initialize a license for Aspose.Words using a license file in the local file system.

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
| Parameter | Type | Description |
| --- | --- | --- |
| stream | java.io.InputStream |  |

### setLicense(String licenseName) {#setLicense-java.lang.String}
```
public void setLicense(String licenseName)
```


Licenses the component.

 **Remarks:** 

Tries to find the license in the following locations:

1. Explicit path.

2. The folder that contains the Aspose component JAR file.

3. The folder that contains the client's calling JAR file.

 **Examples:** 

Shows how initialize a license for Aspose.Words using a license file in the local file system.

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
| Parameter | Type | Description |
| --- | --- | --- |
| licenseName | java.lang.String | Can be a full or short file name. Use an empty string to switch to evaluation mode. |

