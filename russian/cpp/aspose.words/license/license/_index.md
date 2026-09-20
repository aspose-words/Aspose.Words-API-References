---
title: "Aspose::Words::License::License конструктор"
linktitle: "License"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::License::License конструктор. Инициализирует новый экземпляр этого класса в C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words/license/license/
---
## License::License constructor


Инициализирует новый экземпляр этого класса.

```cpp
Aspose::Words::License::License()
```


## Примеры



Показывает, как инициализировать лицензию для Aspose.Words, используя файл лицензии в локальной файловой системе.
```cpp
System::String testLicenseFileName = u"Aspose.Words.Cpp.lic";

// Установите лицензию для нашего продукта Aspose.Words, передав имя файла действующей лицензии из локальной файловой системы.
System::String licenseFileName = System::IO::Path::Combine(get_LicenseDir(), testLicenseFileName);

auto license = System::MakeObject<Aspose::Words::License>();
license->SetLicense(licenseFileName);

// Создайте копию нашего файла лицензии в папке binaries вашего приложения.
System::String licenseCopyFileName = System::IO::Path::Combine(get_AssemblyDir(), testLicenseFileName);
System::IO::File::Copy(licenseFileName, licenseCopyFileName);

// Если передать имя файла без пути,
// метод SetLicense будет искать этот файл в нескольких локальных расположениях файловой системы.
// Одно из этих расположений будет папка "bin", которая содержит копию нашего файла лицензии.
license->SetLicense(testLicenseFileName);
```

## См. также

* Class [License](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
