---
title: FontSettings.DefaultInstance
linktitle: DefaultInstance
articleTitle: DefaultInstance
second_title: Aspose.Words per .NET
description: FontSettings DefaultInstance proprietà. Impostazioni carattere predefinite statiche in C#.
type: docs
weight: 20
url: /it/net/aspose.words.fonts/fontsettings/defaultinstance/
---
## FontSettings.DefaultInstance property

Impostazioni carattere predefinite statiche.

```csharp
public static FontSettings DefaultInstance { get; }
```

## Osservazioni

Questa istanza viene utilizzata per impostazione predefinita in un documento a meno che[`FontSettings`](../../../aspose.words/document/fontsettings/) è specificato.

## Esempi

Mostra come configurare l'istanza delle impostazioni dei caratteri predefinita.

```csharp
// Configura l'istanza delle impostazioni del carattere predefinito per utilizzare il carattere "Courier New".
// come sostituto di backup quando proviamo a utilizzare un carattere sconosciuto.
FontSettings.DefaultInstance.SubstitutionSettings.DefaultFontSubstitution.DefaultFontName = "Courier New";

Assert.True(FontSettings.DefaultInstance.SubstitutionSettings.DefaultFontSubstitution.Enabled);

Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Non-existent font";
builder.Write("Hello world!");

// Questo documento non ha una configurazione FontSettings. Quando rendiamo il documento,
// l'istanza FontSettings predefinita risolverà il carattere mancante.
// Aspose.Words utilizzerà "Courier New" per eseguire il rendering del testo che utilizza il carattere sconosciuto.
Assert.Null(doc.FontSettings);

doc.Save(ArtifactsDir + "FontSettings.DefaultFontInstance.pdf");
```

Mostra come utilizzare l'interfaccia IWarningCallback per monitorare gli avvisi di sostituzione dei caratteri.

```csharp
public void SubstitutionWarning()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Font.Name = "Times New Roman";
    builder.Writeln("Hello world!");

    FontSubstitutionWarningCollector callback = new FontSubstitutionWarningCollector();
    doc.WarningCallback = callback;

    // Memorizza la raccolta corrente di fonti di carattere, che sarà la fonte di carattere predefinita per ogni documento
    // per il quale non specifichiamo una fonte di carattere diversa.
    FontSourceBase[] originalFontSources = FontSettings.DefaultInstance.GetFontsSources();

    // A scopo di test, imposteremo Aspose.Words per cercare i caratteri solo in una cartella che non esiste.
    FontSettings.DefaultInstance.SetFontsFolder(string.Empty, false);

    // Durante il rendering del documento, non sarà possibile trovare il carattere "Times New Roman".
    // Ciò causerà un avviso di sostituzione del carattere, che il nostro callback rileverà.
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
