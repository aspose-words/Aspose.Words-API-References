---
title: OoxmlSaveOptions.SaveFormat
linktitle: SaveFormat
articleTitle: SaveFormat
second_title: Aspose.Words per .NET
description: Scopri la proprietà SaveFormat di OoxmlSaveOptions per scegliere facilmente formati di documenti come Docx, Docm, Dotx, Dotm o FlatOpc per un salvataggio senza interruzioni.
type: docs
weight: 70
url: /it/net/aspose.words.saving/ooxmlsaveoptions/saveformat/
---
## OoxmlSaveOptions.SaveFormat property

Specifica il formato in cui il documento verrà salvato se viene utilizzato questo oggetto di opzioni di salvataggio. Può essereDocx ,Docm , Dotx ,Dotm OFlatOpc .

```csharp
public override SaveFormat SaveFormat { get; set; }
```

## Esempi

Mostra come impostare una specifica di conformità OOXML a cui deve aderire un documento salvato.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Se configuriamo le opzioni di compatibilità per essere conformi a Microsoft Word 2003,
// l'inserimento di un'immagine ne definirà la forma mediante VML.
doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2003);
builder.InsertImage(ImageDir + "Transparent background logo.png");

Assert.AreEqual(ShapeMarkupLanguage.Vml, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).MarkupLanguage);

// Lo standard OOXML "ISO/IEC 29500:2008" non supporta le forme VML.
// Se impostiamo la proprietà "Compliance" dell'oggetto SaveOptions su "OoxmlCompliance.Iso29500_2008_Strict",
 // qualsiasi documento salvato durante il passaggio di questo oggetto dovrà seguire tale standard.
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

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [OoxmlSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
