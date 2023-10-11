---
title: Enum WarningType
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.WarningType перечисление. Указывает тип предупреждения выдаваемого Aspose.Words во время загрузки или сохранения документа.
type: docs
weight: 6660
url: /ru/net/aspose.words/warningtype/
---
## WarningType enumeration

Указывает тип предупреждения, выдаваемого Aspose.Words во время загрузки или сохранения документа.

```csharp
[Flags]
public enum WarningType
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| DataLossCategory | `FF` | Некоторый текст/символ/изображение или другие данные будут отсутствовать либо в дереве документа после загрузки, , либо в созданном документе после сохранения. |
| DataLoss | `1` | Общая потеря данных, без конкретного кода. |
| MajorFormattingLossCategory | `FF00` | Полученный документ или определенное место в нем могут существенно отличаться по сравнению с исходным документом. |
| MajorFormattingLoss | `100` | Общая основная потеря форматирования, без конкретного кода. |
| MinorFormattingLossCategory | `FF0000` | Результирующий документ или определенное место в нем могут выглядеть несколько иначе по сравнению с исходным документом. |
| MinorFormattingLoss | `10000` | Общая незначительная потеря форматирования, без специального кода. |
| FontSubstitution | `20000` | Шрифт заменен. |
| FontEmbedding | `40000` | Потеря информации о встроенном шрифте во время сохранения документа. |
| UnexpectedContentCategory | `F000000` | Некоторое содержимое исходного документа не может быть распознано (т.е. не поддерживается), это может или не может вызвать проблемы или привести к потере данных/форматирования. |
| UnexpectedContent | `1000000` | Общий непредвиденный контент, без конкретного кода. |
| Hint | `10000000` | Сообщает о потенциальной проблеме или предлагает улучшение. |

### Примеры

Показывает, как настроить свойство для поиска ближайшего соответствия отсутствующему шрифту из доступных источников шрифтов.

```csharp
public void EnableFontSubstitution()
{
    // Откройте документ, содержащий текст, отформатированный шрифтом, которого нет ни в одном из наших источников шрифтов.
    Document doc = new Document(MyDir + "Missing font.docx");

    // Назначаем обратный вызов для обработки предупреждений о замене шрифта.
    HandleDocumentSubstitutionWarnings substitutionWarningHandler = new HandleDocumentSubstitutionWarnings();
    doc.WarningCallback = substitutionWarningHandler;

    // Установить имя шрифта по умолчанию и включить подстановку шрифтов.
    FontSettings fontSettings = new FontSettings();
    fontSettings.SubstitutionSettings.DefaultFontSubstitution.DefaultFontName = "Arial";
    ;
    fontSettings.SubstitutionSettings.FontInfoSubstitution.Enabled = true;

    // После замены шрифта следует использовать оригинальные метрики шрифта.
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

    Assert.That(substitutionWarningHandler.FontWarnings, Is.Empty);
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

* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)


