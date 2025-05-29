---
title: LoadOptions.FontSettings
linktitle: FontSettings
articleTitle: FontSettings
second_title: Aspose.Words per .NET
description: Personalizza le impostazioni del font del tuo documento con LoadOptions FontSettings per migliorare leggibilità e stile. Ottimizza i tuoi documenti senza sforzo!
type: docs
weight: 60
url: /it/net/aspose.words.loading/loadoptions/fontsettings/
---
## LoadOptions.FontSettings property

Consente di specificare le impostazioni del font del documento.

```csharp
public FontSettings FontSettings { get; set; }
```

## Osservazioni

Durante il caricamento di alcuni formati, Aspose.Words potrebbe richiedere la risoluzione dei font. Ad esempio, durante il caricamento di documenti HTML, Aspose.Words potrebbe risolvere i font per eseguire il fallback dei font.

Se impostato su`null` , impostazioni predefinite dei caratteri statici[`DefaultInstance`](../../../aspose.words.fonts/fontsettings/defaultinstance/) verrà utilizzato.

Il valore predefinito è`null`.

## Esempi

Mostra come applicare le impostazioni di sostituzione dei caratteri durante il caricamento di un documento.

```csharp
// Crea un oggetto FontSettings che sostituirà il font "Times New Roman"
// con il font "Arvo" dalla nostra cartella "MyFonts".
FontSettings fontSettings = new FontSettings();
fontSettings.SetFontsFolder(FontsDir, false);
fontSettings.SubstitutionSettings.TableSubstitution.AddSubstitutes("Times New Roman", "Arvo");

// Imposta l'oggetto FontSettings come proprietà di un oggetto LoadOptions appena creato.
LoadOptions loadOptions = new LoadOptions();
loadOptions.FontSettings = fontSettings;

// Carica il documento, quindi trasformalo in PDF con la sostituzione del font.
Document doc = new Document(MyDir + "Document.docx", loadOptions);

doc.Save(ArtifactsDir + "LoadOptions.FontSettings.pdf");
```

Mostra come designare i sostituti dei font durante il caricamento.

```csharp
LoadOptions loadOptions = new LoadOptions();
loadOptions.FontSettings = new FontSettings();

// Imposta una regola di sostituzione dei font per un oggetto LoadOptions.
// Se il documento che stiamo caricando utilizza un font che non abbiamo,
// questa regola sostituirà il font non disponibile con uno esistente.
// In questo caso, tutti gli utilizzi di "MissingFont" verranno convertiti in "Comic Sans MS".
TableSubstitutionRule substitutionRule = loadOptions.FontSettings.SubstitutionSettings.TableSubstitution;
substitutionRule.AddSubstitutes("MissingFont", "Comic Sans MS");

Document doc = new Document(MyDir + "Missing font.html", loadOptions);

// A questo punto il testo sarà ancora in "MissingFont".
// La sostituzione del font avverrà quando verrà renderizzato il documento.
Assert.AreEqual("MissingFont", doc.FirstSection.Body.FirstParagraph.Runs[0].Font.Name);

doc.Save(ArtifactsDir + "FontSettings.ResolveFontsBeforeLoadingDocument.pdf");
```

### Guarda anche

* class [FontSettings](../../../aspose.words.fonts/fontsettings/)
* class [LoadOptions](../)
* spazio dei nomi [Aspose.Words.Loading](../../../aspose.words.loading/)
* assemblea [Aspose.Words](../../../)
