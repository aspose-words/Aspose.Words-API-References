---
title: Enum ShapeMarkupLanguage
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Drawing.ShapeMarkupLanguage opsomming. Gibt die für die Form verwendete Auszeichnungssprache an.
type: docs
weight: 1130
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
| Dml | `0` | Drawing Markup Language wird verwendet, um die Form zu definieren. |
| Vml | `1` | Vector Markup Language wird verwendet, um die Form zu definieren. |

### Beispiele

Zeigt, wie eine OOXML-Compliance-Spezifikation festgelegt wird, die ein gespeichertes Dokument einhalten soll.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Wenn wir Kompatibilitätsoptionen so konfigurieren, dass sie Microsoft Word 2003 entsprechen,
// Durch das Einfügen eines Bildes wird seine Form mit VML definiert.
doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2003);
builder.InsertImage(ImageDir + "Transparent background logo.png");

Assert.AreEqual(ShapeMarkupLanguage.Vml, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).MarkupLanguage);

// Der OOXML-Standard "ISO/IEC 29500:2008" unterstützt keine VML-Formen.
// Wenn wir die "Compliance"-Eigenschaft des SaveOptions-Objekts auf "OoxmlCompliance.Iso29500_2008_Strict" setzen,
 // Jedes Dokument, das wir speichern, während wir dieses Objekt übergeben, muss diesem Standard folgen.
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


