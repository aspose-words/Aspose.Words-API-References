---
title: "Метод Aspose::Words::License::SetLicense"
linktitle: "SetLicense"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::License::SetLicense. Лицензирует компонент в C++."
type: docs
weight: 5000
url: /ru/cpp/aspose.words/license/setlicense/
---
## License::SetLicense(const System::SharedPtr\<System::IO::Stream\>\&) method


Лицензирует компонент.

```cpp
void Aspose::Words::License::SetLicense(const System::SharedPtr<System::IO::Stream> &stream)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| stream | const System::SharedPtr\<System::IO::Stream\>\& | Поток, содержащий лицензию. |
## Примечания


Используйте этот метод для загрузки лицензии из потока.

## Примеры



Показывает, как инициализировать лицензию для Aspose.Words из потока.
```cpp
System::String testLicenseFileName = u"Aspose.Words.Cpp.lic";
// Установите лицензию для нашего продукта Aspose.Words, передав поток с действительным файлом лицензии в нашей локальной файловой системе.
{
    System::SharedPtr<System::IO::Stream> myStream = System::IO::File::OpenRead(System::IO::Path::Combine(get_LicenseDir(), testLicenseFileName));
    auto license = System::MakeObject<Aspose::Words::License>();
    license->SetLicense(myStream);
}
```

## См. также

* Class [License](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## License::SetLicense(const System::String\&) method


Лицензирует компонент.

```cpp
void Aspose::Words::License::SetLicense(const System::String &licenseName)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| licenseName | const System::String\& | Может быть полным или коротким именем файла. Используйте пустую строку, чтобы переключиться в режим оценки. |
## Примечания


Пытается найти лицензию в следующих местах:

1. Явный путь.
1. Папка, содержащая библиотеку Aspose.Words.
1. Папка, содержащая приложение клиента.



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
## License::SetLicense(std::basic_istream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> void Aspose::Words::License::SetLicense(std::basic_istream<CharType, Traits> &stream)
```

## См. также

* Class [License](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
