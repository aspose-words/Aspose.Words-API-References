---
title: ShapeMarkupLanguage Enum
linktitle: ShapeMarkupLanguage
articleTitle: ShapeMarkupLanguage
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.Drawing.ShapeMarkupLanguage, che definisce i linguaggi di markup delle forme per una formattazione avanzata dei documenti e una maggiore flessibilità di progettazione.
type: docs
weight: 1670
url: /it/net/aspose.words.drawing/shapemarkuplanguage/
---
## ShapeMarkupLanguage enumeration

Specifica il linguaggio di markup utilizzato per la forma.

```csharp
public enum ShapeMarkupLanguage : byte
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Dml | `0` | Il linguaggio di markup del disegno viene utilizzato per definire la forma. |
| Vml | `1` | Il linguaggio di markup vettoriale viene utilizzato per definire la forma. |

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

* spazio dei nomi [Aspose.Words.Drawing](../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../)
