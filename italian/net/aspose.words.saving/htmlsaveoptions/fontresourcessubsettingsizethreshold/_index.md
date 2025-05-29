---
title: HtmlSaveOptions.FontResourcesSubsettingSizeThreshold
linktitle: FontResourcesSubsettingSizeThreshold
articleTitle: FontResourcesSubsettingSizeThreshold
second_title: Aspose.Words per .NET
description: Ottimizza i tuoi file HTML, MHTML o EPUB con la proprietà FontResourcesSubsettingSizeThreshold, garantendo una gestione efficiente delle risorse dei font. Valore predefinito: 0.
type: docs
weight: 290
url: /it/net/aspose.words.saving/htmlsaveoptions/fontresourcessubsettingsizethreshold/
---
## HtmlSaveOptions.FontResourcesSubsettingSizeThreshold property

Controlla quali risorse di font necessitano di sottoinsiemi quando si salva in HTML, MHTML o EPUB. L'impostazione predefinita è`0` .

```csharp
public int FontResourcesSubsettingSizeThreshold { get; set; }
```

## Osservazioni

[`ExportFontResources`](../exportfontresources/) Consente l'esportazione dei font come file sussidiari o come parti del pacchetto output . Se il documento utilizza molti font, soprattutto con un numero elevato di glifi, le dimensioni dell'output possono aumentare significativamente. Il sottoinsieme dei font riduce le dimensioni della risorsa font esportata filtrando i glifi che non sono utilizzati dal documento corrente.

Il sottoinsieme dei font funziona come segue:

* Per impostazione predefinita, tutti i font esportati vengono suddivisi in sottoinsiemi.
* Collocamento`FontResourcesSubsettingSizeThreshold` su un valore positivo indica ad Aspose.Words di creare un sottoinsieme dei font la cui dimensione del file è maggiore del valore specificato.
* Impostazione della proprietà suMaxValue sopprime il sottoinsieme dei font.

**Importante!**Quando si esportano risorse font, è necessario considerare le questioni relative alla licenza dei font. Gli autori che desiderano utilizzare font specifici tramite un meccanismo di download devono sempre verificare attentamente che l'uso previsto rientri nell'ambito della licenza. Molti font commerciali attualmente non consentono il download dal web dei loro font in alcun formato. I contratti di licenza che coprono alcuni font specificano specificamente che l'utilizzo tramite**@font-face** rules nei fogli di stile CSS non è consentito. Anche la creazione di sottoinsiemi di font può violare i termini di licenza.

## Esempi

Mostra come lavorare con i sottoinsiemi di font.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Times New Roman";
builder.Writeln("Hello world!");
builder.Font.Name = "Courier New";
builder.Writeln("Hello world!");

// Quando salviamo il documento in HTML, possiamo passare un oggetto SaveOptions per configurare il sottoinsieme dei font.
// Supponiamo di impostare il flag "ExportFontResources" su "true" e di assegnare un nome a una cartella nella proprietà "FontsFolder".
// In tal caso, l'operazione di salvataggio creerà quella cartella e inserirà un file .ttf al suo interno
// quella cartella per ogni font utilizzato dal nostro documento.
// Ogni file .ttf conterrà l'intero set di glifi di quel font,
// che potrebbe potenzialmente generare un file di grandi dimensioni che accompagna il documento.
// Quando applichiamo il sottoinsieme a un font, i suoi dati grezzi esportati conterranno solo i glifi che il documento contiene
// usando invece dell'intero set di glifi. Se il testo nel nostro documento utilizza solo una piccola frazione del font
// set di glifi, quindi il sottoinsieme ridurrà significativamente la dimensione dei nostri documenti di output.
// Possiamo usare la proprietà "FontResourcesSubsettingSizeThreshold" per definire la dimensione del file .ttf, in byte.
 // Se un font esportato crea un file di dimensioni maggiori, l'operazione di salvataggio applicherà un sottoinsieme a quel font.
// Impostando una soglia pari a 0 si applica il sottoinsieme a tutti i font,
// e impostandolo su "int.MaxValue" si disabilita di fatto il sottoinsieme.
string fontsFolder = ArtifactsDir + "HtmlSaveOptions.FontSubsetting.Fonts";

HtmlSaveOptions options = new HtmlSaveOptions
{
    ExportFontResources = true,
    FontsFolder = fontsFolder,
    FontResourcesSubsettingSizeThreshold = fontResourcesSubsettingSizeThreshold
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.FontSubsetting.html", options);

string[] fontFileNames = Directory.GetFiles(fontsFolder).Where(s => s.EndsWith(".ttf")).ToArray();

Assert.AreEqual(3, fontFileNames.Length);

foreach (string filename in fontFileNames)
{
    // Per impostazione predefinita, i file .ttf per ciascuno dei nostri tre font saranno più grandi di 700 MB.
    // Il sottoinsieme li ridurrà tutti a meno di 30 MB.
    FileInfo fontFileInfo = new FileInfo(filename);

    Assert.True(fontFileInfo.Length > 700000 || fontFileInfo.Length < 30000);
    Assert.True(Math.Max(fontResourcesSubsettingSizeThreshold, 30000) > new FileInfo(filename).Length);
}
```

### Guarda anche

* class [HtmlSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
