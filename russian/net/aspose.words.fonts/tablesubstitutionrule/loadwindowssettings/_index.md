---
title: TableSubstitutionRule.LoadWindowsSettings
linktitle: LoadWindowsSettings
articleTitle: LoadWindowsSettings
second_title: Aspose.Words для .NET
description: Легко загружайте предопределенные настройки подстановки таблиц для Windows с помощью метода LoadWindowsSettings. Оптимизируйте свой рабочий процесс сегодня!
type: docs
weight: 60
url: /ru/net/aspose.words.fonts/tablesubstitutionrule/loadwindowssettings/
---
## TableSubstitutionRule.LoadWindowsSettings method

Загружает предопределенные настройки подстановки таблиц для платформы Windows.

```csharp
public void LoadWindowsSettings()
```

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

* class [TableSubstitutionRule](../)
* пространство имен [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* сборка [Aspose.Words](../../../)
