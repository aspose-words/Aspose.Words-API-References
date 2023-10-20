---
title: HtmlSaveOptions.FontResourcesSubsettingSizeThreshold
linktitle: FontResourcesSubsettingSizeThreshold
articleTitle: FontResourcesSubsettingSizeThreshold
second_title: Aspose.Words per .NET
description: HtmlSaveOptions FontResourcesSubsettingSizeThreshold proprietà. Controlla quali risorse di carattere necessitano di sottoinsiemi durante il salvataggio in HTML MHTML o EPUB. Limpostazione predefinita è0  in C#.
type: docs
weight: 290
url: /it/net/aspose.words.saving/htmlsaveoptions/fontresourcessubsettingsizethreshold/
---
## HtmlSaveOptions.FontResourcesSubsettingSizeThreshold property

Controlla quali risorse di carattere necessitano di sottoinsiemi durante il salvataggio in HTML, MHTML o EPUB. L'impostazione predefinita è`0` .

```csharp
public int FontResourcesSubsettingSizeThreshold { get; set; }
```

## Osservazioni

[`ExportFontResources`](../exportfontresources/) consente di esportare i caratteri come file sussidiari o come parti del pacchetto output . Se il documento utilizza molti caratteri, soprattutto con un numero elevato di glifi, la dimensione dell'output può aumentare in modo significativo. Il sottoinsieme dei caratteri riduce la dimensione della risorsa carattere esportata filtrando i glifi che non vengono utilizzati dal documento corrente.

Il sottoinsieme dei caratteri funziona come segue:

* Per impostazione predefinita, tutti i caratteri esportati sono suddivisi in sottoinsiemi.
* Collocamento`FontResourcesSubsettingSizeThreshold`su un valore positivo indica ad Aspose.Words di sottoimpostare i caratteri la cui dimensione del file è maggiore del valore specificato.
* Impostando la proprietà suMaxValue sopprime il sottoinsieme dei caratteri.

**Importante!** Quando si esportano risorse di caratteri, è necessario considerare i problemi di licenza dei caratteri. Gli autori che desiderano utilizzare caratteri specifici tramite un meccanismo di carattere downloadable devono sempre verificare attentamente che l'uso previsto rientri nell'ambito della licenza del carattere. Molti caratteri commerciali attualmente non consentono il download dal Web dei propri caratteri in qualsiasi forma. I contratti di licenza che coprono alcuni caratteri specificano specificamente che l'utilizzo tramite**@font-face** regole nei fogli di stile CSS non è consentito. Anche il sottoinsieme dei caratteri può violare i termini della licenza.

## Esempi

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

// Quando salviamo il documento in HTML, possiamo passare un oggetto SaveOptions per configurare il sottoinsieme dei caratteri.
// Supponiamo di impostare il flag "ExportFontResources" su "true" e di nominare anche una cartella nella proprietà "FontsFolder".
// In tal caso, l'operazione di salvataggio creerà quella cartella e inserirà al suo interno un file .ttf
// quella cartella per ogni carattere utilizzato dal nostro documento.
// Ogni file .ttf conterrà l'intero set di glifi di quel carattere,
// che potrebbe potenzialmente risultare in un file molto grande che accompagna il documento.
// Quando applichiamo il sottoinsieme a un font, i suoi dati grezzi esportati conterranno solo i glifi del documento
// utilizzando al posto dell'intero set di glifi. Se il testo nel nostro documento utilizza solo una piccola frazione di un carattere
// set di glifi, quindi il sottoinsieme ridurrà significativamente le dimensioni dei nostri documenti di output.
// Possiamo utilizzare la proprietà "FontResourcesSubsettingSizeThreshold" per definire la dimensione del file .ttf, in byte.
 // Se un font esportato crea un file di dimensioni maggiori, l'operazione di salvataggio applicherà il sottoinsieme a quel font.
// L'impostazione di una soglia pari a 0 applica il sottoimpostazione a tutti i caratteri,
// e impostandolo su "int.MaxValue" disabilita effettivamente il sottoinsieme.
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

* class [HtmlSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
