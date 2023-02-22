---
title: Interface IWarningCallback
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.IWarningCallback интерфейс. Реализуйте этот интерфейс если вы хотите чтобы ваш собственный пользовательский метод вызывал предупреждения о потере точности которые могут возникнуть во время загрузки или сохранения документа.
type: docs
weight: 3010
url: /ru/net/aspose.words/iwarningcallback/
---
## IWarningCallback interface

Реализуйте этот интерфейс, если вы хотите, чтобы ваш собственный пользовательский метод вызывал предупреждения о потере точности, которые могут возникнуть во время загрузки или сохранения документа.

```csharp
public interface IWarningCallback
```

## Методы

| Имя | Описание |
| --- | --- |
| [Warning](../../aspose.words/iwarningcallback/warning/)(WarningInfo) | Aspose.Words вызывает этот метод, когда во время загрузки документа или сохранения возникает проблема, которая может привести к потере форматирования или точности данных. |

### Примеры

Показывает, как использовать интерфейс IWarningCallback для отслеживания предупреждений о замене шрифта.

```csharp
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

    // При рендеринге документа негде будет найти шрифт "Times New Roman".
    // Это вызовет предупреждение о замене шрифта, которое обнаружит наш обратный вызов.
    doc.Save(ArtifactsDir + "FontSettings.SubstitutionWarning.pdf");

    FontSettings.DefaultInstance.SetFontsSources(originalFontSources);

    Assert.True(callback.FontSubstitutionWarnings[0].Description
        .Equals(
            "Font 'Times New Roman' has not been found. Using 'Fanwood' font instead. Reason: first available font."));
}

private class FontSubstitutionWarningCollector : IWarningCallback
{
    /// <summary>
    /// Вызывается каждый раз, когда возникает предупреждение во время загрузки/сохранения.
    /// </summary>
    public void Warning(WarningInfo info)
    {
        if (info.WarningType == WarningType.FontSubstitution)
            FontSubstitutionWarnings.Warning(info);
    }

    public WarningInfoCollection FontSubstitutionWarnings = new WarningInfoCollection();
}
```

В шоу добавлен резервный вариант рендеринга растровых изображений и изменен тип предупреждений о неподдерживаемых записях метафайлов.

```csharp
{
    Document doc = new Document(MyDir + "WMF with image.docx");

    MetafileRenderingOptions metafileRenderingOptions = new MetafileRenderingOptions();

    // Установите для свойства "EmulateRasterOperations" значение "false", чтобы вернуться к растровому изображению, когда
    // он встречает метафайл, для которого потребуются растровые операции для отображения в выходном PDF-файле.
    metafileRenderingOptions.EmulateRasterOperations = false;

    // Установите для свойства «RenderingMode» значение «VectorWithFallback», чтобы попытаться отобразить каждый метафайл с использованием векторной графики.
    metafileRenderingOptions.RenderingMode = MetafileRenderingMode.VectorWithFallback;

    // Создаем объект "PdfSaveOptions", который мы можем передать в метод "Сохранить" документа
    // для изменения того, как этот метод преобразует документ в .PDF и применяет конфигурацию
    // в нашем объекте MetafileRenderingOptions для операции сохранения.
    PdfSaveOptions saveOptions = new PdfSaveOptions();
    saveOptions.MetafileRenderingOptions = metafileRenderingOptions;

    HandleDocumentWarnings callback = new HandleDocumentWarnings();
    doc.WarningCallback = callback;

    doc.Save(ArtifactsDir + "PdfSaveOptions.HandleBinaryRasterWarnings.pdf", saveOptions);

    Assert.AreEqual(1, callback.Warnings.Count);
    Assert.AreEqual("'R2_XORPEN' binary raster operation is partly supported.",
        callback.Warnings[0].Description);
}

/// <summary>
/// Выводит и собирает предупреждения о потере форматирования, возникающие при сохранении документа.
/// </summary>
public class HandleDocumentWarnings : IWarningCallback
{
    public void Warning(WarningInfo info)
    {
        if (info.WarningType == WarningType.MinorFormattingLoss)
        {
            Console.WriteLine("Unsupported operation: " + info.Description);
            Warnings.Warning(info);
        }
    }

    public WarningInfoCollection Warnings = new WarningInfoCollection();
}
```

Показывает, как задать свойство для поиска ближайшего соответствия отсутствующему шрифту из доступных источников шрифтов.

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

* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)


