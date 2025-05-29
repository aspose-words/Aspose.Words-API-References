---
title: TableSubstitutionRule Class
linktitle: TableSubstitutionRule
articleTitle: TableSubstitutionRule
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Fonts.TableSubstitutionRule для эффективного управления шрифтами и бесшовного форматирования текста в ваших документах.
type: docs
weight: 3490
url: /ru/net/aspose.words.fonts/tablesubstitutionrule/
---
## TableSubstitutionRule class

Правило замены шрифта таблицы.

Чтобы узнать больше, посетите[Работа со шрифтами](https://docs.aspose.com/words/net/working-with-fonts/) документальная статья.

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
| [AddSubstitutes](../../aspose.words.fonts/tablesubstitutionrule/addsubstitutes/)(*string, params string[]*) | Добавляет заменяющие имена шрифтов для указанного исходного имени шрифта. |
| [GetSubstitutes](../../aspose.words.fonts/tablesubstitutionrule/getsubstitutes/)(*string*) | Возвращает массив, содержащий заменяющие имена шрифтов для указанного исходного имени шрифта. |
| [Load](../../aspose.words.fonts/tablesubstitutionrule/load/#load)(*Stream*) | Загружает настройки подстановки таблицы из потока XML. |
| [Load](../../aspose.words.fonts/tablesubstitutionrule/load/#load_1)(*string*) | Загружает настройки подстановки таблицы из XML-файла. |
| [LoadAndroidSettings](../../aspose.words.fonts/tablesubstitutionrule/loadandroidsettings/)() | Загружает предопределенные настройки подстановки таблиц для платформы Android. |
| [LoadLinuxSettings](../../aspose.words.fonts/tablesubstitutionrule/loadlinuxsettings/)() | Загружает предопределенные настройки подстановки таблиц для платформы Linux. |
| [LoadWindowsSettings](../../aspose.words.fonts/tablesubstitutionrule/loadwindowssettings/)() | Загружает предопределенные настройки подстановки таблиц для платформы Windows. |
| [Save](../../aspose.words.fonts/tablesubstitutionrule/save/#save)(*Stream*) | Сохраняет текущие настройки подстановки таблицы в stream. |
| [Save](../../aspose.words.fonts/tablesubstitutionrule/save/#save_1)(*string*) | Сохраняет текущие настройки подстановки таблицы в файл. |
| [SetSubstitutes](../../aspose.words.fonts/tablesubstitutionrule/setsubstitutes/)(*string, params string[]*) | Переопределить заменяющие имена шрифтов для указанного исходного имени шрифта. |

## Примечания

Это правило определяет список имен заменяющих шрифтов, которые будут использоваться, если исходный шрифт недоступен. Заменители будут проверяться на наличие имени шрифта и[`AltName`](../fontinfo/altname/) (если есть).

## Примеры

Показывает, как получить доступ к таблицам замены шрифтов для Windows и Linux.

```csharp
Document doc = new Document();
FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;

// Создаем новое правило подстановки таблицы и загружаем таблицу подстановки шрифтов Microsoft Windows по умолчанию.
TableSubstitutionRule tableSubstitutionRule = fontSettings.SubstitutionSettings.TableSubstitution;
tableSubstitutionRule.LoadWindowsSettings();

// В Windows заменой шрифта «Times New Roman CE» по умолчанию является «Times New Roman».
Assert.AreEqual(new[] {"Times New Roman"},
    tableSubstitutionRule.GetSubstitutes("Times New Roman CE").ToArray());

// Мы можем сохранить таблицу в виде XML-документа.
tableSubstitutionRule.Save(ArtifactsDir + "FontSettings.TableSubstitutionRule.Windows.xml");

// В Linux есть собственная таблица замен.
// Существует несколько альтернативных шрифтов для «Times New Roman CE».
// Если первая замена, "FreeSerif", также недоступна,
// это правило будет циклически перебирать остальные элементы массива, пока не найдет доступный.
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

* class [FontSubstitutionRule](../fontsubstitutionrule/)
* пространство имен [Aspose.Words.Fonts](../../aspose.words.fonts/)
* сборка [Aspose.Words](../../)
