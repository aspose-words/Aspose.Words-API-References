---
title: ShapeMarkupLanguage Enum
linktitle: ShapeMarkupLanguage
articleTitle: ShapeMarkupLanguage
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aufzählung Aspose.Words.Drawing.ShapeMarkupLanguage, die Formmarkierungssprachen für eine verbesserte Dokumentformatierung und Designflexibilität definiert.
type: docs
weight: 1670
url: /de/net/aspose.words.drawing/shapemarkuplanguage/
---
## ShapeMarkupLanguage enumeration

Gibt die für die Form verwendete Auszeichnungssprache an.

```csharp
public enum ShapeMarkupLanguage : byte
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Dml | `0` | Die Drawing Markup Language wird zum Definieren der Form verwendet. |
| Vml | `1` | Zur Definition der Form wird die Vector Markup Language verwendet. |

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

* namensraum [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Montage [Aspose.Words](../../)
