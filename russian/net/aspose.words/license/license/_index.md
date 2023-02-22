---
title: License.License
second_title: Справочник по API Aspose.Words для .NET
description: License строитель. Инициализирует новый экземпляр этого класса.
type: docs
weight: 10
url: /ru/net/aspose.words/license/license/
---
## License constructor

Инициализирует новый экземпляр этого класса.

```csharp
public License()
```

### Примеры

Показывает, как инициализировать лицензию для Aspose.Words, используя файл лицензии в локальной файловой системе.

```csharp
// Установите лицензию для нашего продукта Aspose.Words, передав имя файла локальной файловой системы действительного файла лицензии.
string licenseFileName = Path.Combine(LicenseDir, "Aspose.Words.NET.lic");

License license = new License();
license.SetLicense(licenseFileName);

// Создаем копию нашего файла лицензии в папке бинарных файлов нашего приложения.
string licenseCopyFileName = Path.Combine(AssemblyDir, "Aspose.Words.NET.lic");
File.Copy(licenseFileName, licenseCopyFileName);

// Если мы передаем имя файла без пути,
// SetLicense будет искать этот файл в нескольких местах локальной файловой системы.
// Одним из таких мест будет папка «bin», содержащая копию нашего файла лицензии.
license.SetLicense("Aspose.Words.NET.lic");
```

### Смотрите также

* class [License](../)
* пространство имен [Aspose.Words](../../license/)
* сборка [Aspose.Words](../../../)


