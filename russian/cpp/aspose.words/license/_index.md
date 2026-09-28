---
title: "Aspose::Words::License класс"
linktitle: "License"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::License class. Предоставляет методы для лицензирования компонента. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 39000
url: /ru/cpp/aspose.words/license/
---
## License class


Предоставляет методы лицензирования компонента. Чтобы узнать больше, посетите статью документации [Licensing and Subscription](https://docs.aspose.com/words/cpp/licensing/).

```cpp
class License : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [License](./license/)() | Инициализирует новый экземпляр этого класса. |
| [SetLicense](./setlicense/)(const System::String\&) | Лицензирует компонент. |
| [SetLicense](./setlicense/)(const System::SharedPtr\<System::IO::Stream\>\&) | Лицензирует компонент. |
| [SetLicense](./setlicense/)(std::basic_istream\<CharType, Traits\>\&) |  |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
