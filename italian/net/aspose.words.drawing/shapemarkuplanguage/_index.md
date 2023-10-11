---
title: Enum ShapeMarkupLanguage
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Drawing.ShapeMarkupLanguage enum. Specifica il linguaggio di markup utilizzato per la forma.
type: docs
weight: 1280
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
| Dml | `0` | Drawing Markup Language viene utilizzato per definire la forma. |
| Vml | `1` | Vector Markup Language viene utilizzato per definire la forma. |

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

* spazio dei nomi [Aspose.Words.Drawing](../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../)


