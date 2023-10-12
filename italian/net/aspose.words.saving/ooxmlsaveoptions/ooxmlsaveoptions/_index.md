---
title: OoxmlSaveOptions.OoxmlSaveOptions
second_title: Aspose.Words per .NET API Reference
description: OoxmlSaveOptions costruttore. Inizializza una nuova istanza di questa classe che può essere utilizzata per salvare un documento nel fileDocx formato.
type: docs
weight: 10
url: /it/net/aspose.words.saving/ooxmlsaveoptions/ooxmlsaveoptions/
---
## OoxmlSaveOptions() {#constructor}

Inizializza una nuova istanza di questa classe che può essere utilizzata per salvare un documento nel fileDocx formato.

```csharp
public OoxmlSaveOptions()
```

### Esempi

Mostra come impostare una specifica di conformità OOXML a cui aderire un documento salvato.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Se configuriamo le opzioni di compatibilità per conformarsi a Microsoft Word 2003,
// l'inserimento di un'immagine ne definirà la forma utilizzando VML.
doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2003);
builder.InsertImage(ImageDir + "Transparent background logo.png");

Assert.AreEqual(ShapeMarkupLanguage.Vml, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).MarkupLanguage);

// Lo standard OOXML "ISO/IEC 29500:2008" non supporta le forme VML.
// Se impostiamo la proprietà "Compliance" dell'oggetto SaveOptions su "OoxmlCompliance.Iso29500_2008_Strict",
 // qualsiasi documento che salviamo mentre passiamo questo oggetto dovrà seguire quello standard.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions
{
    Compliance = OoxmlCompliance.Iso29500_2008_Strict,
    SaveFormat = SaveFormat.Docx
};

doc.Save(ArtifactsDir + "OoxmlSaveOptions.Iso29500Strict.docx", saveOptions);

// Il nostro documento salvato definisce la forma utilizzando DML per aderire allo standard OOXML "ISO/IEC 29500:2008".
doc = new Document(ArtifactsDir + "OoxmlSaveOptions.Iso29500Strict.docx");

Assert.AreEqual(ShapeMarkupLanguage.Dml, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).MarkupLanguage);
```

### Guarda anche

* class [OoxmlSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../ooxmlsaveoptions/)
* assemblea [Aspose.Words](../../../)

---

## OoxmlSaveOptions(SaveFormat) {#constructor_1}

Inizializza una nuova istanza di questa classe che può essere utilizzata per salvare un documento nel fileDocx , Docm ,Dotx ,Dotm oppure FlatOpc formato.

```csharp
public OoxmlSaveOptions(SaveFormat saveFormat)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| saveFormat | SaveFormat | Può essereDocx ,Docm , Dotx ,Dotm OFlatOpc . |

### Esempi

Mostra come supportare i caratteri di controllo legacy durante la conversione in .docx.

```csharp
Document doc = new Document(MyDir + "Legacy control character.doc");

// Quando salviamo il documento in un formato OOXML, possiamo creare un oggetto OoxmlSaveOptions
// e poi passarlo al metodo di salvataggio del documento per modificare il modo in cui salviamo il documento.
// Imposta la proprietà "KeepLegacyControlChars" su "true" per preservarla
// il carattere legacy "ShortDateTime" durante il salvataggio.
// Imposta la proprietà "KeepLegacyControlChars" su "false" per rimuoverla
// il carattere legacy "ShortDateTime" dal documento di output.
OoxmlSaveOptions so = new OoxmlSaveOptions(SaveFormat.Docx);
so.KeepLegacyControlChars = keepLegacyControlChars;

doc.Save(ArtifactsDir + "OoxmlSaveOptions.KeepLegacyControlChars.docx", so);

doc = new Document(ArtifactsDir + "OoxmlSaveOptions.KeepLegacyControlChars.docx");

Assert.AreEqual(keepLegacyControlChars ? "\u0013date \\@ \"MM/dd/yyyy\"\u0014\u0015\f" : "\u001e\f",
    doc.FirstSection.Body.GetText());
```

### Guarda anche

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [OoxmlSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../ooxmlsaveoptions/)
* assemblea [Aspose.Words](../../../)


