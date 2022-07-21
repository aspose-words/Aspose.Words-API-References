---
title: FontResourcesSubsettingSizeThreshold
second_title: Aspose.Words per .NET API Reference
description: Controlla quali risorse di font necessitano di sottoimpostazioni quando si salva in HTML MHTML o EPUB. Limpostazione predefinita è0 .
type: docs
weight: 300
url: /it/net/aspose.words.saving/htmlsaveoptions/fontresourcessubsettingsizethreshold/
---
## HtmlSaveOptions.FontResourcesSubsettingSizeThreshold property

Controlla quali risorse di font necessitano di sottoimpostazioni quando si salva in HTML, MHTML o EPUB. L'impostazione predefinita è`0` .

```csharp
public int FontResourcesSubsettingSizeThreshold { get; set; }
```

### Osservazioni

[`ExportFontResources`](../exportfontresources) consente di esportare i caratteri come file sussidiari o come parti del pacchetto output . Se il documento utilizza molti caratteri, in particolare con un numero elevato di glifi, la dimensione dell'output può aumentare in modo significativo . L'impostazione dei caratteri riduce la dimensione della risorsa carattere esportata filtrando i glifi che non sono utilizzati dal documento corrente.

La sottoimpostazione dei caratteri funziona come segue:

* Per impostazione predefinita, tutti i caratteri esportati sono sottoinsiemi.
* Ambientazione`FontResourcesSubsettingSizeThreshold` un valore positivo indica ad Aspose.Words di sottoporre i caratteri la cui dimensione del file è maggiore del valore specificato.
* Impostazione della proprietà suMaxValue sopprime la sottoimpostazione dei caratteri.

**Importante!** Quando si esportano risorse di font, è necessario considerare i problemi di licenza dei font. Gli autori che desiderano utilizzare caratteri specifici tramite un meccanismo di carattere scaricabile devono sempre verificare attentamente che l'uso previsto rientri nell'ambito della licenza del carattere. Molti font commerciali attualmente non consentono il download dal Web dei loro font in qualsiasi forma. Gli accordi di licenza che coprono alcuni caratteri specificano che l'utilizzo tramite **@font-face** rules nei fogli di stile CSS non è consentito. Anche le impostazioni secondarie dei caratteri possono violare i termini della licenza.

### Esempi

Mostra come lavorare con il sottoinsieme dei caratteri.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Times New Roman";
builder.Writeln("Hello world!");
builder.Font.Name = "Courier New";
builder.Writeln("Hello world!");

// Quando salviamo il documento in HTML, possiamo passare un oggetto SaveOptions configure font subsetting.
// Supponiamo di impostare il flag "ExportFontResources" su "true" e di nominare anche una cartella nella proprietà "FontsFolder".
// In tal caso, l'operazione di salvataggio creerà quella cartella e inserirà un file .ttf all'interno
// quella cartella per ogni font utilizzato dal nostro documento.
// Ogni file .ttf conterrà l'intero set di glifi di quel font,
// che potrebbe potenzialmente risultare in un file molto grande che accompagna il documento.
// Quando applichiamo un sottoinsieme a un font, i suoi dati grezzi esportati conterranno solo i glifi che è il documento
// usando invece dell'intero set di glifi. Se il testo nel nostro documento utilizza solo una piccola frazione di un font
// set di glifi, quindi l'impostazione secondaria ridurrà notevolmente le dimensioni dei nostri documenti di output.
// Possiamo usare la proprietà "FontResourcesSubsettingSizeThreshold" per definire una dimensione del file .ttf, in byte.
 // Se un font esportato crea un file di dimensioni maggiori, l'operazione di salvataggio applicherà un sottoinsieme a quel font.
// L'impostazione di una soglia di 0 applica la sottoimpostazione a tutti i caratteri,
// e impostandolo su "int.MaxValue" si disabilitano efficacemente le sottoimpostazioni.
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
    // Per impostazione predefinita, i file .ttf per ciascuno dei nostri tre caratteri supereranno i 700 MB.
    // Il sottoimpostazione li ridurrà tutti a meno di 30 MB.
    FileInfo fontFileInfo = new FileInfo(filename);

    Assert.True(fontFileInfo.Length > 700000 || fontFileInfo.Length < 30000);
    Assert.True(Math.Max(fontResourcesSubsettingSizeThreshold, 30000) > new FileInfo(filename).Length);
}
```

### Guarda anche

* class [HtmlSaveOptions](../../htmlsaveoptions)
* spazio dei nomi [Aspose.Words.Saving](../../htmlsaveoptions)
* assemblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
