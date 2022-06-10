---
title: WarningCallback
second_title: Справочник по API Aspose.Words для .NET
description: Вызывается во время различных процедур обработки документов при обнаружении проблемы которая может привести к потере точности данных или форматирования.
type: docs
weight: 90
url: /ru/net/aspose.words/documentbase/warningcallback/
---
## DocumentBase.WarningCallback property

Вызывается во время различных процедур обработки документов при обнаружении проблемы, которая может привести к потере точности данных или форматирования.

```csharp
public IWarningCallback WarningCallback { get; set; }
```

### Примечания

Документ может генерировать предупреждения на любом этапе своего существования, поэтому важно настроить обратный вызов предупреждения как как можно раньше, чтобы избежать потери предупреждений. Например, такие свойства, как[`PageCount`](../../document/pagecount) фактически создают макет документа, который используется в дальнейшем для рендеринга, и предупреждения макета могут быть потеряны, если::Обратный вызов:47:::warning указывается только для последующих вызовов рендеринга.

### Примеры

Показывает, как использовать интерфейс IWarningCallback для мониторинга предупреждений о замене шрифта.

```csharp
[Test]
public void EnableFontSubstitution()
{
    // Откройте документ, содержащий текст, отформатированный шрифтом, которого нет ни в одном из наших источников шрифтов.
    Document doc = new Document(MyDir + "Missing font.docx");

    // Назначаем обратный вызов для обработки предупреждений о замене шрифта.
    HandleDocumentSubstitutionWarnings substitutionWarningHandler = new HandleDocumentSubstitutionWarnings();
    doc.WarningCallback = substitutionWarningHandler;

    // Установите имя шрифта по умолчанию и включите замену шрифта.
    FontSettings fontSettings = new FontSettings();
    fontSettings.SubstitutionSettings.DefaultFontSubstitution.DefaultFontName = "Arial";
    ;
    fontSettings.SubstitutionSettings.FontInfoSubstitution.Enabled = true;

    // Мы получим предупреждение о замене шрифта, если сохраним документ с отсутствующим шрифтом.
    doc.FontSettings = fontSettings;
    doc.Save(ArtifactsDir + "FontSettings.EnableFontSubstitution.pdf");

    using (IEnumerator<WarningInfo> warnings = substitutionWarningHandler.FontWarnings.GetEnumerator())
        while (warnings.MoveNext())
            Console.WriteLine(warnings.Current.Description);

    // Мы также можем проверять предупреждения в коллекции и очищать их.
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
    /// Вызывается каждый раз, когда возникает предупреждение во время загрузки/сохранения.
    /// </summary>
    public void Warning(WarningInfo info)
    {
        if (info.WarningType == WarningType.FontSubstitution)
            FontWarnings.Warning(info);
    }

    public WarningInfoCollection FontWarnings = new WarningInfoCollection();
}
```

Показывает, как установить свойство для поиска ближайшего соответствия отсутствующему шрифту из доступных источников шрифтов.

```csharp
[Test]
public void EnableFontSubstitution()
{
    // Откройте документ, содержащий текст, отформатированный шрифтом, которого нет ни в одном из наших источников шрифтов.
    Document doc = new Document(MyDir + "Missing font.docx");

    // Назначаем обратный вызов для обработки предупреждений о замене шрифта.
    HandleDocumentSubstitutionWarnings substitutionWarningHandler = new HandleDocumentSubstitutionWarnings();
    doc.WarningCallback = substitutionWarningHandler;

    // Установите имя шрифта по умолчанию и включите замену шрифта.
    FontSettings fontSettings = new FontSettings();
    fontSettings.SubstitutionSettings.DefaultFontSubstitution.DefaultFontName = "Arial";
    ;
    fontSettings.SubstitutionSettings.FontInfoSubstitution.Enabled = true;

    // Мы получим предупреждение о замене шрифта, если сохраним документ с отсутствующим шрифтом.
    doc.FontSettings = fontSettings;
    doc.Save(ArtifactsDir + "FontSettings.EnableFontSubstitution.pdf");

    using (IEnumerator<WarningInfo> warnings = substitutionWarningHandler.FontWarnings.GetEnumerator())
        while (warnings.MoveNext())
            Console.WriteLine(warnings.Current.Description);

    // Мы также можем проверять предупреждения в коллекции и очищать их.
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
    /// Вызывается каждый раз, когда возникает предупреждение во время загрузки/сохранения.
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

* interface [IWarningCallback](../../iwarningcallback)
* class [DocumentBase](../../documentbase)
* пространство имен [Aspose.Words](../../documentbase)
* сборка [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
