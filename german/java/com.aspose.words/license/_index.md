---
title: "Lizenz"
linktitle: "Lizenz"
second_title: "Aspose.Words für Java"
description: "Stellt Methoden bereit, um die Komponente in Java zu lizenzieren."
type: docs
weight: 421
url: /de/java/com.aspose.words/license/
---

**Inheritance:**
java.lang.Object
```
public class License
```

Stellt Methoden zur Lizenzierung der Komponente bereit.

Um mehr zu erfahren, besuchen Sie den [ Lizenzierung und Abonnement ][Licensing and Subscription] Dokumentationsartikel.

 **Examples:** 

Zeigt, wie man eine Lizenz für Aspose.Words mit einer Lizenzdatei im lokalen Dateisystem initialisiert.

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
## Konstruktoren

| Konstruktor | Beschreibung |
| --- | --- |
| [License()](#License) | Initialisiert eine neue Instanz dieser Klasse. |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [setLicense(InputStream stream)](#setLicense-java.io.InputStream) |  |
| [setLicense(String licenseName)](#setLicense-java.lang.String) | Lizenziert die Komponente. |
### License() {#License}
```
public License()
```


Initialisiert eine neue Instanz dieser Klasse.

 **Examples:** 

Zeigt, wie man eine Lizenz für Aspose.Words mit einer Lizenzdatei im lokalen Dateisystem initialisiert.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| stream | java.io.InputStream |  |

### setLicense(String licenseName) {#setLicense-java.lang.String}
```
public void setLicense(String licenseName)
```


Lizenziert die Komponente.

 **Remarks:** 

Versucht, die Lizenz an den folgenden Orten zu finden:

1. Expliziter Pfad.

2. Der Ordner, der die Aspose-Komponenten‑JAR‑Datei enthält.

3. Der Ordner, der die JAR‑Datei des aufrufenden Clients enthält.

 **Examples:** 

Zeigt, wie man eine Lizenz für Aspose.Words mit einer Lizenzdatei im lokalen Dateisystem initialisiert.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| licenseName | java.lang.String | Kann ein voller oder kurzer Dateiname sein. Verwenden Sie einen leeren String, um in den Evaluierungsmodus zu wechseln. |

