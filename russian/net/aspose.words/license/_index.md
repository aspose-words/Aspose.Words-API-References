---
title: Class License
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.License сорт. Предоставляет методы лицензирования компонента.
type: docs
weight: 3420
url: /ru/net/aspose.words/license/
---
## License class

Предоставляет методы лицензирования компонента.

Чтобы узнать больше, посетите[Лицензирование и подписка](https://docs.aspose.com/words/net/licensing/) статья документации.

```csharp
public class License
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [License](license/)() | Инициализирует новый экземпляр этого класса. |

## Методы

| Имя | Описание |
| --- | --- |
| [SetLicense](../../aspose.words/license/setlicense/#setlicense)(Stream) | Лицензиирует компонент. |
| [SetLicense](../../aspose.words/license/setlicense/#setlicense_1)(string) | Лицензиирует компонент. |

### Примеры

Показывает, как инициализировать лицензию для Aspose.Words с использованием файла лицензии в локальной файловой системе.

```csharp
// Установите лицензию для нашего продукта Aspose.Words, передав имя файла локальной файловой системы действительного файла лицензии.
string licenseFileName = Path.Combine(LicenseDir, "Aspose.Words.NET.lic");

License license = new License();
license.SetLicense(licenseFileName);

// Создайте копию нашего файла лицензии в папке двоичных файлов нашего приложения.
string licenseCopyFileName = Path.Combine(AssemblyDir, "Aspose.Words.NET.lic");
File.Copy(licenseFileName, licenseCopyFileName);

// Если мы передаем имя файла без пути,
// SetLicense будет искать этот файл в нескольких местах локальной файловой системы.
// Одним из этих мест будет папка «bin», содержащая копию нашего файла лицензии.
license.SetLicense("Aspose.Words.NET.lic");
```

### Смотрите также

* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)


