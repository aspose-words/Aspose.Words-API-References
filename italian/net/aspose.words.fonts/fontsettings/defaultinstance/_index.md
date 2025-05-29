---
title: FontSettings.DefaultInstance
linktitle: DefaultInstance
articleTitle: DefaultInstance
second_title: Aspose.Words per .NET
description: Scopri la proprietà FontSettings DefaultInstance per una gestione semplificata dei font statici. Ottimizza il tuo design con impostazioni predefinite personalizzabili!
type: docs
weight: 20
url: /it/net/aspose.words.fonts/fontsettings/defaultinstance/
---
## FontSettings.DefaultInstance property

Impostazioni predefinite statiche del font.

```csharp
public static FontSettings DefaultInstance { get; }
```

## Osservazioni

Questa istanza viene utilizzata per impostazione predefinita in un documento a meno che[`FontSettings`](../../../aspose.words/document/fontsettings/) è specificato.

## Esempi

Mostra come configurare l'istanza delle impostazioni predefinite del font.

```csharp
// Configura l'istanza delle impostazioni del font predefinito per utilizzare il font "Courier New"
// come sostituto di backup quando si tenta di utilizzare un font sconosciuto.
FontSettings.DefaultInstance.SubstitutionSettings.DefaultFontSubstitution.DefaultFontName = "Courier New";

Assert.True(FontSettings.DefaultInstance.SubstitutionSettings.DefaultFontSubstitution.Enabled);

Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Non-existent font";
builder.Write("Hello world!");

// Questo documento non ha una configurazione FontSettings. Quando eseguiamo il rendering del documento,
// l'istanza predefinita di FontSettings risolverà il problema del font mancante.
// Aspose.Words utilizzerà "Courier New" per visualizzare il testo che utilizza il font sconosciuto.
Assert.Null(doc.FontSettings);

doc.Save(ArtifactsDir + "FontSettings.DefaultFontInstance.pdf");
```

Mostra come utilizzare l'interfaccia IWarningCallback per monitorare gli avvisi di sostituzione dei font.

```csharp
public void SubstitutionWarning()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Font.Name = "Times New Roman";
    builder.Writeln("Hello world!");

    FontSubstitutionWarningCollector callback = new FontSubstitutionWarningCollector();
    doc.WarningCallback = callback;

    // Memorizza la raccolta corrente di sorgenti di font, che sarà la sorgente di font predefinita per ogni documento
    // per il quale non specifichiamo una sorgente font diversa.
    FontSourceBase[] originalFontSources = FontSettings.DefaultInstance.GetFontsSources();

    // A scopo di test, imposteremo Aspose.Words in modo che cerchi i font solo in una cartella che non esiste.
    FontSettings.DefaultInstance.SetFontsFolder(string.Empty, false);

    // Durante il rendering del documento, non sarà possibile trovare il font "Times New Roman".
    // Ciò genererà un avviso di sostituzione del font, che verrà rilevato dal nostro callback.
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
    /// Chiamato ogni volta che si verifica un avviso durante il caricamento/salvataggio.
    /// </summary>
    public void Warning(WarningInfo info)
    {
        if (info.WarningType == WarningType.FontSubstitution)
            FontSubstitutionWarnings.Warning(info);
    }

    public WarningInfoCollection FontSubstitutionWarnings = new WarningInfoCollection();
}
```

### Guarda anche

* class [FontSettings](../)
* spazio dei nomi [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* assemblea [Aspose.Words](../../../)
