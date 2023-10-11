---
title: FontSettings.DefaultInstance
second_title: Справочник по API Aspose.Words для .NET
description: FontSettings свойство. Статические настройки шрифта по умолчанию.
type: docs
weight: 20
url: /ru/net/aspose.words.fonts/fontsettings/defaultinstance/
---
## FontSettings.DefaultInstance property

Статические настройки шрифта по умолчанию.

```csharp
public static FontSettings DefaultInstance { get; }
```

### Примечания

Этот экземпляр используется в документе по умолчанию, если только[`FontSettings`](../../../aspose.words/document/fontsettings/) указано.

### Примеры

Показывает, как настроить экземпляр параметров шрифта по умолчанию.

```csharp
// Настраиваем экземпляр настроек шрифта по умолчанию для использования шрифта «Courier New»
// в качестве резервной замены, когда мы пытаемся использовать неизвестный шрифт.
FontSettings.DefaultInstance.SubstitutionSettings.DefaultFontSubstitution.DefaultFontName = "Courier New";

Assert.True(FontSettings.DefaultInstance.SubstitutionSettings.DefaultFontSubstitution.Enabled);

Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Non-existent font";
builder.Write("Hello world!");

// В этом документе нет конфигурации FontSettings. Когда мы рендерим документ,
// экземпляр FontSettings по умолчанию разрешит отсутствующий шрифт.
// Aspose.Words будет использовать «Courier New» для отображения текста, использующего неизвестный шрифт.
Assert.Null(doc.FontSettings);

doc.Save(ArtifactsDir + "FontSettings.DefaultFontInstance.pdf");
```

Показывает, как использовать интерфейс IWarningCallback для отслеживания предупреждений о подмене шрифтов.

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

    // В целях тестирования мы настроим Aspose.Words искать шрифты только в несуществующей папке.
    FontSettings.DefaultInstance.SetFontsFolder(string.Empty, false);

    // При рендеринге документа шрифт Times New Roman найти будет негде.
    // Это вызовет предупреждение о замене шрифта, которое обнаружит наш обратный вызов.
    doc.Save(ArtifactsDir + "FontSettings.SubstitutionWarning.pdf");

    FontSettings.DefaultInstance.SetFontsSources(originalFontSources);

    Assert.True(callback.FontSubstitutionWarnings[0].WarningType == WarningType.FontSubstitution);
    Assert.True(callback.FontSubstitutionWarnings[0].Description
        .Equals(
            "Font 'Times New Roman' has not been found. Using 'Fanwood' font instead. Reason: first available font.", StringComparison.Ordinal));
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

### Смотрите также

* class [FontSettings](../)
* пространство имен [Aspose.Words.Fonts](../../fontsettings/)
* сборка [Aspose.Words](../../../)


