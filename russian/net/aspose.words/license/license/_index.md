---
title: License
linktitle: License
articleTitle: License
second_title: Aspose.Words для .NET
description: License строитель. Инициализирует новый экземпляр этого класса на С#.
type: docs
weight: 10
url: /ru/net/aspose.words/license/license/
---
## License constructor

Инициализирует новый экземпляр этого класса.

```csharp
public License()
```

## Примеры

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

* class [License](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
