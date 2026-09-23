---
title: "License"
linktitle: "License"
second_title: "Aspose.Words pour Java"
description: "Fournit des méthodes pour licencier le composant en Java."
type: docs
weight: 421
url: /fr/java/com.aspose.words/license/
---

**Inheritance:**
java.lang.Object
```
public class License
```

Fournit des méthodes pour licencier le composant.

Pour en savoir plus, consultez le [ Licensing and Subscription ][Licensing and Subscription] article de documentation.

 **Examples:** 

Montre comment initialiser une licence pour Aspose.Words en utilisant un fichier de licence dans le système de fichiers local.

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
| [License()](#License) | Initialise une nouvelle instance de cette classe. |
## Méthodes

| Méthode | Description |
| --- | --- |
| [setLicense(InputStream stream)](#setLicense-java.io.InputStream) |  |
| [setLicense(String licenseName)](#setLicense-java.lang.String) | Licence le composant. |
### License() {#License}
```
public License()
```


Initialise une nouvelle instance de cette classe.

 **Examples:** 

Montre comment initialiser une licence pour Aspose.Words en utilisant un fichier de licence dans le système de fichiers local.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| stream | java.io.InputStream |  |

### setLicense(String licenseName) {#setLicense-java.lang.String}
```
public void setLicense(String licenseName)
```


Licence le composant.

 **Remarks:** 

Tente de trouver la licence aux emplacements suivants :

1. Chemin explicite.

2. Le dossier qui contient le fichier JAR du composant Aspose.

3. Le dossier qui contient le fichier JAR appelé par le client.

 **Examples:** 

Montre comment initialiser une licence pour Aspose.Words en utilisant un fichier de licence dans le système de fichiers local.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| licenseName | java.lang.String | Peut être un nom de fichier complet ou court. Utilisez une chaîne vide pour passer en mode d'évaluation. |

