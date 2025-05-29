---
title: DocumentBase.WarningCallback
linktitle: WarningCallback
articleTitle: WarningCallback
second_title: Aspose.Words для .NET
description: Откройте для себя свойство DocumentBase WarningCallback, которое имеет решающее значение для обеспечения целостности данных во время обработки документов путем обнаружения потенциальных проблем форматирования.
type: docs
weight: 100
url: /ru/net/aspose.words/documentbase/warningcallback/
---
## DocumentBase.WarningCallback property

Вызывается во время различных процедур обработки документов при обнаружении проблемы, которая может привести к потере точности данных или форматирования.

```csharp
public IWarningCallback WarningCallback { get; set; }
```

## Примечания

Документ может генерировать предупреждения на любом этапе своего существования, поэтому важно настроить обратный вызов предупреждения as как можно раньше, чтобы избежать потери предупреждений. Например, такие свойства, как[`PageCount`](../../document/pagecount/) фактически создает макет документа, который позже используется для рендеринга, и предупреждения о макете могут быть потеряны, если обратный вызов предупреждения указан только для вызовов рендеринга позже.

## Примеры

Показывает, как использовать интерфейс IWarningCallback для мониторинга предупреждений о замене шрифтов.

```csharp
public void SubstitutionWarning()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Font.Name = "Times New Roman";
    builder.Writeln("Hello world!");

    FontSubstitutionWarningCollector callback = new FontSubstitutionWarningCollector();
    doc.WarningCallback = callback;

    // Сохраняем текущую коллекцию источников шрифтов, которая будет источником шрифтов по умолчанию для каждого документа
    // для которого мы не указываем другой источник шрифта.
    FontSourceBase[] originalFontSources = FontSettings.DefaultInstance.GetFontsSources();

    // В целях тестирования мы настроим Aspose.Words на поиск шрифтов только в несуществующей папке.
    FontSettings.DefaultInstance.SetFontsFolder(string.Empty, false);

    // При отображении документа шрифт «Times New Roman» будет негде найти.
    // Это вызовет предупреждение о замене шрифта, которое обнаружит наш обратный вызов.
    doc.Save(ArtifactsDir + "FontSettings.SubstitutionWarning.pdf");

    FontSettings.DefaultInstance.SetFontsSources(originalFontSources);

    Assert.True(callback.FontSubstitutionWarnings[0].WarningType == WarningType.FontSubstitution);
    Assert.True(callback.FontSubstitutionWarnings[0].Description
        .Equals(
            "Font 'Times New Roman' has not been found. Using 'Fanwood' font instead. Reason: first available font."));
}

private class FontSubstitutionWarningCollector : IWarningCallback
{
    /// <summary>
    /// Вызывается каждый раз, когда во время загрузки/сохранения возникает предупреждение.
    /// </summary>
    public void Warning(WarningInfo info)
    {
        if (info.WarningType == WarningType.FontSubstitution)
            FontSubstitutionWarnings.Warning(info);
    }

    public WarningInfoCollection FontSubstitutionWarnings = new WarningInfoCollection();
}
```

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

* interface [IWarningCallback](../../iwarningcallback/)
* class [DocumentBase](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
