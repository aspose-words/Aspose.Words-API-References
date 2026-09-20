---
title: "Método Aspose::Words::License::SetLicense"
linktitle: "SetLicense"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::License::SetLicense. Licencia el componente en C++."
type: docs
weight: 5000
url: /es/cpp/aspose.words/license/setlicense/
---
## License::SetLicense(const System::SharedPtr\<System::IO::Stream\>\&) method


Licencia el componente.

```cpp
void Aspose::Words::License::SetLicense(const System::SharedPtr<System::IO::Stream> &stream)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| flujo | const System::SharedPtr\<System::IO::Stream\>\& | Un flujo que contiene la licencia. |
## Observaciones


Use este método para cargar una licencia desde un flujo.

## Ejemplos



Muestra cómo inicializar una licencia para Aspose.Words desde un flujo.
```cpp
System::String testLicenseFileName = u"Aspose.Words.Cpp.lic";
// Establezca la licencia para nuestro producto Aspose.Words pasando un flujo con un archivo de licencia válido en nuestro sistema de archivos local.
{
    System::SharedPtr<System::IO::Stream> myStream = System::IO::File::OpenRead(System::IO::Path::Combine(get_LicenseDir(), testLicenseFileName));
    auto license = System::MakeObject<Aspose::Words::License>();
    license->SetLicense(myStream);
}
```

## Ver también

* Class [License](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## License::SetLicense(const System::String\&) method


Licencia el componente.

```cpp
void Aspose::Words::License::SetLicense(const System::String &licenseName)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| licenseName | const System::String\& | Puede ser un nombre de archivo completo o corto. Use una cadena vacía para cambiar al modo de evaluación. |
## Observaciones


Intenta encontrar la licencia en las siguientes ubicaciones:

1. Ruta explícita.
1. La carpeta que contiene la biblioteca Aspose.Words.
1. La carpeta que contiene la aplicación del cliente.



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
## License::SetLicense(std::basic_istream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> void Aspose::Words::License::SetLicense(std::basic_istream<CharType, Traits> &stream)
```

## Ver también

* Class [License](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
