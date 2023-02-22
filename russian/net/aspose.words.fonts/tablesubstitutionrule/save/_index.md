---
title: TableSubstitutionRule.Save
second_title: Справочник по API Aspose.Words для .NET
description: TableSubstitutionRule метод. Сохраняет текущие настройки подстановки таблиц в файл.
type: docs
weight: 70
url: /ru/net/aspose.words.fonts/tablesubstitutionrule/save/
---
## Save(string) {#save_1}

Сохраняет текущие настройки подстановки таблиц в файл.

```csharp
public void Save(string fileName)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | String | Имя выходного файла. |

### Примеры

Показывает, как получить доступ к таблицам замены шрифтов для Windows и Linux.

```csharp
Document doc = new Document();
FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;

// Создать новое правило подстановки таблиц и загрузить таблицу подстановки шрифтов Microsoft Windows по умолчанию.
TableSubstitutionRule tableSubstitutionRule = fontSettings.SubstitutionSettings.TableSubstitution;
tableSubstitutionRule.LoadWindowsSettings();

// В Windows заменой по умолчанию для шрифта "Times New Roman CE" является "Times New Roman".
Assert.AreEqual(new[] {"Times New Roman"},
    tableSubstitutionRule.GetSubstitutes("Times New Roman CE").ToArray());

// Мы можем сохранить таблицу в виде XML-документа.
tableSubstitutionRule.Save(ArtifactsDir + "FontSettings.TableSubstitutionRule.Windows.xml");

// В Linux есть собственная таблица подстановок.
// Существует несколько замещающих шрифтов для "Times New Roman CE".
// Если первая замена "FreeSerif" тоже недоступна,
// это правило будет циклически перебирать другие в массиве, пока не найдет доступное.
tableSubstitutionRule.LoadLinuxSettings();
Assert.AreEqual(new[] {"FreeSerif", "Liberation Serif", "DejaVu Serif"},
    tableSubstitutionRule.GetSubstitutes("Times New Roman CE").ToArray());

// Сохраняем таблицу подстановок Linux в виде XML-документа с помощью потока.
using (FileStream fileStream = new FileStream(ArtifactsDir + "FontSettings.TableSubstitutionRule.Linux.xml",
    FileMode.Create))
{
    tableSubstitutionRule.Save(fileStream);
}
```

### Смотрите также

* class [TableSubstitutionRule](../)
* пространство имен [Aspose.Words.Fonts](../../tablesubstitutionrule/)
* сборка [Aspose.Words](../../../)

---

## Save(Stream) {#save}

Сохраняет текущие настройки подстановки таблицы в поток.

```csharp
public void Save(Stream outputStream)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| outputStream | Stream | Выходной поток. |

### Примеры

Показывает, как получить доступ к таблицам замены шрифтов для Windows и Linux.

```csharp
Document doc = new Document();
FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;

// Создать новое правило подстановки таблиц и загрузить таблицу подстановки шрифтов Microsoft Windows по умолчанию.
TableSubstitutionRule tableSubstitutionRule = fontSettings.SubstitutionSettings.TableSubstitution;
tableSubstitutionRule.LoadWindowsSettings();

// В Windows заменой по умолчанию для шрифта "Times New Roman CE" является "Times New Roman".
Assert.AreEqual(new[] {"Times New Roman"},
    tableSubstitutionRule.GetSubstitutes("Times New Roman CE").ToArray());

// Мы можем сохранить таблицу в виде XML-документа.
tableSubstitutionRule.Save(ArtifactsDir + "FontSettings.TableSubstitutionRule.Windows.xml");

// В Linux есть собственная таблица подстановок.
// Существует несколько замещающих шрифтов для "Times New Roman CE".
// Если первая замена "FreeSerif" тоже недоступна,
// это правило будет циклически перебирать другие в массиве, пока не найдет доступное.
tableSubstitutionRule.LoadLinuxSettings();
Assert.AreEqual(new[] {"FreeSerif", "Liberation Serif", "DejaVu Serif"},
    tableSubstitutionRule.GetSubstitutes("Times New Roman CE").ToArray());

// Сохраняем таблицу подстановок Linux в виде XML-документа с помощью потока.
using (FileStream fileStream = new FileStream(ArtifactsDir + "FontSettings.TableSubstitutionRule.Linux.xml",
    FileMode.Create))
{
    tableSubstitutionRule.Save(fileStream);
}
```

### Смотрите также

* class [TableSubstitutionRule](../)
* пространство имен [Aspose.Words.Fonts](../../tablesubstitutionrule/)
* сборка [Aspose.Words](../../../)


