---
title: "Aspose::Words::License clase"
linktitle: "License"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::License class. Proporciona métodos para licenciar el componente. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 39000
url: /es/cpp/aspose.words/license/
---
## License class


Proporciona métodos para licenciar el componente. Para obtener más información, visite el artículo de documentación [Licensing and Subscription](https://docs.aspose.com/words/cpp/licensing/).

```cpp
class License : public System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [License](./license/)() | Inicializa una nueva instancia de esta clase. |
| [SetLicense](./setlicense/)(const System::String\&) | Licencia el componente. |
| [SetLicense](./setlicense/)(const System::SharedPtr\<System::IO::Stream\>\&) | Licencia el componente. |
| [SetLicense](./setlicense/)(std::basic_istream\<CharType, Traits\>\&) |  |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
