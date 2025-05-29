---
title: License Class
linktitle: License
articleTitle: License
second_title: Aspose.Words для .NET
description: Раскройте весь потенциал Aspose.Words с нашим классом лицензий. Легко управляйте лицензированием для бесперебойной обработки документов и улучшенной функциональности.
type: docs
weight: 3870
url: /ru/net/aspose.words/license/
---
## License class

Предоставляет методы лицензирования компонента.

Чтобы узнать больше, посетите[Лицензирование и подписка](https://docs.aspose.com/words/net/licensing/) документальная статья.

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
| [SetLicense](../../aspose.words/license/setlicense/#setlicense)(*Stream*) | Лицензирует компонент. |
| [SetLicense](../../aspose.words/license/setlicense/#setlicense_1)(*string*) | Лицензирует компонент. |

## Примеры

Показывает, как инициализировать лицензию для Aspose.Words, используя файл лицензии в локальной файловой системе.

```csharp
// Устанавливаем лицензию для нашего продукта Aspose.Words, передавая имя файла локальной файловой системы действительного файла лицензии.
string licenseFileName = Path.Combine(LicenseDir, "Aspose.Words.NET.lic");

License license = new License();
license.SetLicense(licenseFileName);

// Создаем копию нашего файла лицензии в папке двоичных файлов нашего приложения.
string licenseCopyFileName = Path.Combine(AssemblyDir, "Aspose.Words.NET.lic");
File.Copy(licenseFileName, licenseCopyFileName);

// Если мы передадим имя файла без пути,
// SetLicense выполнит поиск этого файла в нескольких местах локальной файловой системы.
// Одним из таких мест будет папка «bin», содержащая копию нашего файла лицензии.
license.SetLicense("Aspose.Words.NET.lic");
```

### Смотрите также

* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)
