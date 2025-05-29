---
title: OoxmlSaveOptions.SaveFormat
linktitle: SaveFormat
articleTitle: SaveFormat
second_title: Aspose.Words für .NET
description: Entdecken Sie die SaveFormat-Eigenschaft von OoxmlSaveOptions, um einfach Dokumentformate wie Docx, Docm, Dotx, Dotm oder FlatOpc zum nahtlosen Speichern auszuwählen.
type: docs
weight: 70
url: /de/net/aspose.words.saving/ooxmlsaveoptions/saveformat/
---
## OoxmlSaveOptions.SaveFormat property

Gibt das Format an, in dem das Dokument gespeichert wird, wenn dieses Speicheroptionsobjekt verwendet wird. Kann seinDocx ,Docm , Dotx ,Dotm oderFlatOpc .

```csharp
public override SaveFormat SaveFormat { get; set; }
```

## Beispiele

Zeigt, wie eine OOXML-Konformitätsspezifikation festgelegt wird, an die sich ein gespeichertes Dokument halten muss.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Wenn wir die Kompatibilitätsoptionen so konfigurieren, dass sie mit Microsoft Word 2003 kompatibel sind,
// Durch das Einfügen eines Bildes wird seine Form mithilfe von VML definiert.
doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2003);
builder.InsertImage(ImageDir + "Transparent background logo.png");

Assert.AreEqual(ShapeMarkupLanguage.Vml, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).MarkupLanguage);

// Der OOXML-Standard „ISO/IEC 29500:2008“ unterstützt keine VML-Formen.
// Wenn wir die Eigenschaft "Compliance" des SaveOptions-Objekts auf "OoxmlCompliance.Iso29500_2008_Strict" setzen,
    // Jedes Dokument, das wir beim Übergeben dieses Objekts speichern, muss diesem Standard entsprechen.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions
{
    Compliance = OoxmlCompliance.Iso29500_2008_Strict,
    SaveFormat = SaveFormat.Docx
};

doc.Save(ArtifactsDir + "OoxmlSaveOptions.Iso29500Strict.docx", saveOptions);

// Unser gespeichertes Dokument definiert die Form mithilfe von DML, um dem OOXML-Standard „ISO/IEC 29500:2008“ zu entsprechen.
doc = new Document(ArtifactsDir + "OoxmlSaveOptions.Iso29500Strict.docx");

Assert.AreEqual(ShapeMarkupLanguage.Dml, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).MarkupLanguage);
```

### Siehe auch

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [OoxmlSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
