---
title: License
linktitle: License
articleTitle: License
second_title: Aspose.Words для .NET
description: Легко создавайте и управляйте лицензиями с помощью нашего класса конструктора. Упростите процесс лицензирования и повысьте эффективность уже сегодня!
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

* class [License](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
