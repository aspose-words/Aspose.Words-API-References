---
title: FontInfoSubstitutionRule Class
linktitle: FontInfoSubstitutionRule
articleTitle: FontInfoSubstitutionRule
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Fonts.FontInfoSubstitutionRule, чтобы оптимизировать управление шрифтами в ваших документах с помощью возможностей бесшовной замены.
type: docs
weight: 3370
url: /ru/net/aspose.words.fonts/fontinfosubstitutionrule/
---
## FontInfoSubstitutionRule class

Правило подстановки информации о шрифте.

Чтобы узнать больше, посетите[Работа со шрифтами](https://docs.aspose.com/words/net/working-with-fonts/) документальная статья.

```csharp
public class FontInfoSubstitutionRule : FontSubstitutionRule
```

## Характеристики

| Имя | Описание |
| --- | --- |
| virtual [Enabled](../../aspose.words.fonts/fontsubstitutionrule/enabled/) { get; set; } | Указывает, включено правило или нет. |

## Примечания

Согласно этому правилу Aspose.Words оценивает все связанные поля в[`FontInfo`](../fontinfo/) (Panose, Sig и т. д.) for отсутствующий шрифт и находит ближайшее соответствие среди доступных источников шрифтов. Если[`FontInfo`](../fontinfo/) не доступен для отсутствующего шрифта, то ничего не будет сделано.

## Примеры

Показывает, как задать свойство для поиска наиболее близкого соответствия отсутствующему шрифту из доступных источников шрифтов.

```csharp
public void EnableFontSubstitution()
{
    // Открываем документ, содержащий текст, отформатированный шрифтом, которого нет ни в одном из наших источников шрифтов.
    Document doc = new Document(MyDir + "Missing font.docx");

    // Назначаем обратный вызов для обработки предупреждений о замене шрифтов.
    HandleDocumentSubstitutionWarnings substitutionWarningHandler = new HandleDocumentSubstitutionWarnings();
    doc.WarningCallback = substitutionWarningHandler;

    // Задаем имя шрифта по умолчанию и включаем замену шрифта.
    FontSettings fontSettings = new FontSettings();
    fontSettings.SubstitutionSettings.DefaultFontSubstitution.DefaultFontName = "Arial";
    ;
    fontSettings.SubstitutionSettings.FontInfoSubstitution.Enabled = true;

    // После замены шрифта следует использовать метрики исходного шрифта.
    doc.LayoutOptions.KeepOriginalFontMetrics = true;

    // Мы получим предупреждение о замене шрифта, если сохраним документ с отсутствующим шрифтом.
    doc.FontSettings = fontSettings;
    doc.Save(ArtifactsDir + "FontSettings.EnableFontSubstitution.pdf");

    using (IEnumerator<WarningInfo> warnings = substitutionWarningHandler.FontWarnings.GetEnumerator())
        while (warnings.MoveNext())
            Console.WriteLine(warnings.Current.Description);

    // Мы также можем проверить предупреждения в коллекции и очистить их.
    Assert.AreEqual(WarningSource.Layout, substitutionWarningHandler.FontWarnings[0].Source);
    Assert.AreEqual(
        "Font '28 Days Later' has not been found. Using 'Calibri' font instead. Reason: alternative name from document.",
        substitutionWarningHandler.FontWarnings[0].Description);

    substitutionWarningHandler.FontWarnings.Clear();

    Assert.AreEqual(0, substitutionWarningHandler.FontWarnings.Count);
}

public class HandleDocumentSubstitutionWarnings : IWarningCallback
{
    /// <summary>
    /// Вызывается каждый раз, когда во время загрузки/сохранения возникает предупреждение.
    /// </summary>
    public void Warning(WarningInfo info)
    {
        if (info.WarningType == WarningType.FontSubstitution)
            FontWarnings.Warning(info);
    }

    public WarningInfoCollection FontWarnings = new WarningInfoCollection();
}
```

### Смотрите также

* class [FontSubstitutionRule](../fontsubstitutionrule/)
* пространство имен [Aspose.Words.Fonts](../../aspose.words.fonts/)
* сборка [Aspose.Words](../../)
