---
title: "Constructor Aspose::Words::License::License"
linktitle: "License"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Constructor Aspose::Words::License::License. Inicializa una nueva instancia de esta clase en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words/license/license/
---
## License::License constructor


Inicializa una nueva instancia de esta clase.

```cpp
Aspose::Words::License::License()
```


## Ejemplos



Muestra cómo inicializar una licencia para Aspose.Words usando un archivo de licencia en el sistema de archivos local.
```cpp
System::String testLicenseFileName = u"Aspose.Words.Cpp.lic";

// Establezca la licencia para nuestro producto Aspose.Words pasando el nombre de archivo del sistema de archivos local de un archivo de licencia válido.
System::String licenseFileName = System::IO::Path::Combine(get_LicenseDir(), testLicenseFileName);

auto license = System::MakeObject<Aspose::Words::License>();
license->SetLicense(licenseFileName);

// Cree una copia de nuestro archivo de licencia en la carpeta binaria de nuestra aplicación.
System::String licenseCopyFileName = System::IO::Path::Combine(get_AssemblyDir(), testLicenseFileName);
System::IO::File::Copy(licenseFileName, licenseCopyFileName);

// Si pasamos el nombre de un archivo sin una ruta,
// el SetLicense buscará varias ubicaciones del sistema de archivos local para este archivo.
// Una de esas ubicaciones será la carpeta "bin", que contiene una copia de nuestro archivo de licencia.
license->SetLicense(testLicenseFileName);
```

## Ver también

* Class [License](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
