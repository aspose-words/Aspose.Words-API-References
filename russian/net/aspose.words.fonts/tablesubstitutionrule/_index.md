---
title: Class TableSubstitutionRule
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Fonts.TableSubstitutionRule сорт. Правило замены шрифта таблицы.
type: docs
weight: 3060
url: /ru/net/aspose.words.fonts/tablesubstitutionrule/
---
## TableSubstitutionRule class

Правило замены шрифта таблицы.

Чтобы узнать больше, посетите[Работа со шрифтами](https://docs.aspose.com/words/net/working-with-fonts/) статья документации.

```csharp
public class TableSubstitutionRule : FontSubstitutionRule
```

## Характеристики

| Имя | Описание |
| --- | --- |
| virtual [Enabled](../../aspose.words.fonts/fontsubstitutionrule/enabled/) { get; set; } | Указывает, включено правило или нет. |

## Методы

| Имя | Описание |
| --- | --- |
| [AddSubstitutes](../../aspose.words.fonts/tablesubstitutionrule/addsubstitutes/)(string, params string[]) | Добавляет замещающие имена шрифтов для данного исходного имени шрифта. |
| [GetSubstitutes](../../aspose.words.fonts/tablesubstitutionrule/getsubstitutes/)(string) | Возвращает массив, содержащий имена замещающих шрифтов для указанного исходного имени шрифта. |
| [Load](../../aspose.words.fonts/tablesubstitutionrule/load/#load)(Stream) | Загружает настройки подстановки таблиц из XML-потока. |
| [Load](../../aspose.words.fonts/tablesubstitutionrule/load/#load_1)(string) | Загружает настройки подстановки таблиц из XML-файла. |
| [LoadAndroidSettings](../../aspose.words.fonts/tablesubstitutionrule/loadandroidsettings/)() | Загружает предопределенные настройки замены таблиц для платформы Android. |
| [LoadLinuxSettings](../../aspose.words.fonts/tablesubstitutionrule/loadlinuxsettings/)() | Загружает предопределенные настройки подстановки таблиц для платформы Linux. |
| [LoadWindowsSettings](../../aspose.words.fonts/tablesubstitutionrule/loadwindowssettings/)() | Загружает предопределенные параметры замены таблиц для платформы Windows. |
| [Save](../../aspose.words.fonts/tablesubstitutionrule/save/#save)(Stream) | Сохраняет текущие настройки замены таблицы в поток. |
| [Save](../../aspose.words.fonts/tablesubstitutionrule/save/#save_1)(string) | Сохраняет текущие настройки подстановки таблицы в файл. |
| [SetSubstitutes](../../aspose.words.fonts/tablesubstitutionrule/setsubstitutes/)(string, params string[]) | Переопределить имена замещающих шрифтов для данного исходного имени шрифта. |

### Примечания

Это правило определяет список имен замещающих шрифтов, которые будут использоваться, если исходный шрифт недоступен. Замены будут проверяться для имени шрифта и[`AltName`](../fontinfo/altname/) (если есть).

### Примеры

Показывает, как получить доступ к таблицам замены шрифтов для Windows и Linux.

```csharp
Document doc = new Document();
FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;

// Создаем новое правило подстановки таблиц и загружаем таблицу подстановки шрифтов Microsoft Windows по умолчанию.
TableSubstitutionRule tableSubstitutionRule = fontSettings.SubstitutionSettings.TableSubstitution;
tableSubstitutionRule.LoadWindowsSettings();

// В Windows заменой шрифта «Times New Roman CE» по умолчанию является «Times New Roman».
Assert.AreEqual(new[] {"Times New Roman"},
    tableSubstitutionRule.GetSubstitutes("Times New Roman CE").ToArray());

// Мы можем сохранить таблицу в виде XML-документа.
tableSubstitutionRule.Save(ArtifactsDir + "FontSettings.TableSubstitutionRule.Windows.xml");

// В Linux есть своя таблица подстановок.
// Существует несколько шрифтов-заменителей «Times New Roman CE».
// Если первая замена "FreeSerif" также недоступна,
// это правило будет циклически перебирать остальные в массиве, пока не найдет доступное.
tableSubstitutionRule.LoadLinuxSettings();
Assert.AreEqual(new[] {"FreeSerif", "Liberation Serif", "DejaVu Serif"},
    tableSubstitutionRule.GetSubstitutes("Times New Roman CE").ToArray());

// Сохраняем таблицу подстановок Linux в виде XML-документа с использованием потока.
using (FileStream fileStream = new FileStream(ArtifactsDir + "FontSettings.TableSubstitutionRule.Linux.xml",
    FileMode.Create))
{
    tableSubstitutionRule.Save(fileStream);
}
```

### Смотрите также

* class [FontSubstitutionRule](../fontsubstitutionrule/)
* пространство имен [Aspose.Words.Fonts](../../aspose.words.fonts/)
* сборка [Aspose.Words](../../)


