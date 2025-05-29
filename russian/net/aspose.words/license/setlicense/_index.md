---
title: License.SetLicense
linktitle: SetLicense
articleTitle: SetLicense
second_title: Aspose.Words для .NET
description: Легко лицензируйте свои компоненты с помощью нашего метода SetLicense. Разблокируйте полную функциональность и улучшите потенциал своего проекта сегодня!
type: docs
weight: 20
url: /ru/net/aspose.words/license/setlicense/
---
## SetLicense(*string*) {#setlicense_1}

Лицензирует компонент.

```csharp
public void SetLicense(string licenseName)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| licenseName | String | Может быть полным или коротким именем файла или именем встроенного ресурса. Используйте пустую строку для переключения в режим оценки. |

## Примечания

Пытается найти лицензию в следующих местах:

1. Явный путь.

2. Папка, содержащая сборку компонента Aspose.

3. Папка, содержащая вызывающую сборку клиента.

4. Папка, содержащая входную (стартовую) сборку.

5. Встроенный ресурс в вызывающую сборку клиента.

**Примечание:**В .NET Compact Framework пытается найти лицензию только в следующих местах:

1. Явный путь.

2. Встроенный ресурс в вызывающую сборку клиента.

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

---

## SetLicense(*Stream*) {#setlicense}

Лицензирует компонент.

```csharp
public void SetLicense(Stream stream)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| stream | Stream | Поток, содержащий лицензию. |

## Примечания

Используйте этот метод для загрузки лицензии из потока.

## Примеры

Показывает, как инициализировать лицензию для Aspose.Words из потока.

```csharp
// Устанавливаем лицензию для нашего продукта Aspose.Words, передавая поток для действительного файла лицензии в нашей локальной файловой системе.
using (Stream myStream = File.OpenRead(Path.Combine(LicenseDir, "Aspose.Words.NET.lic")))
{
    License license = new License();
    license.SetLicense(myStream);
}
```

### Смотрите также

* class [License](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
