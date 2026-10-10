---
title: "Licencia"
linktitle: "Licencia"
second_title: "Aspose.Words para Java"
description: "Proporciona métodos para licenciar el componente en Java."
type: docs
weight: 421
url: /es/java/com.aspose.words/license/
---

**Inheritance:**
java.lang.Object
```
public class License
```

Proporciona métodos para licenciar el componente.

Para obtener más información, visite el [ Licensing and Subscription ][Licensing and Subscription] artículo de documentación.

 **Examples:** 

Muestra cómo inicializar una licencia para Aspose.Words usando un archivo de licencia en el sistema de archivos local.

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
## Constructores

| Constructor | Descripción |
| --- | --- |
| [License()](#License) | Inicializa una nueva instancia de esta clase. |
## Métodos

| Método | Descripción |
| --- | --- |
| [setLicense(InputStream stream)](#setLicense-java.io.InputStream) |  |
| [setLicense(String licenseName)](#setLicense-java.lang.String) | Licencia el componente. |
### License() {#License}
```
public License()
```


Inicializa una nueva instancia de esta clase.

 **Examples:** 

Muestra cómo inicializar una licencia para Aspose.Words usando un archivo de licencia en el sistema de archivos local.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| stream | java.io.InputStream |  |

### setLicense(String licenseName) {#setLicense-java.lang.String}
```
public void setLicense(String licenseName)
```


Licencia el componente.

 **Remarks:** 

Intenta encontrar la licencia en las siguientes ubicaciones:

1. Ruta explícita.

2. La carpeta que contiene el archivo JAR del componente Aspose.

3. La carpeta que contiene el archivo JAR llamado por el cliente.

 **Examples:** 

Muestra cómo inicializar una licencia para Aspose.Words usando un archivo de licencia en el sistema de archivos local.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| licenseName | java.lang.String | Puede ser un nombre de archivo completo o corto. Use una cadena vacía para cambiar al modo de evaluación. |

