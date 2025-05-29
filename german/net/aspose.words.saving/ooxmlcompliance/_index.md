---
title: OoxmlCompliance Enum
linktitle: OoxmlCompliance
articleTitle: OoxmlCompliance
second_title: Aspose.Words für .NET
description: Erkunden Sie die Enumeration Aspose.Words.Saving.OoxmlCompliance, um Ihre bevorzugte OOXML-Spezifikation für optimales Speichern im DOCX-Format auszuwählen. Verbessern Sie noch heute die Dokumentenqualität!
type: docs
weight: 6120
url: /de/net/aspose.words.saving/ooxmlcompliance/
---
## OoxmlCompliance enumeration

Ermöglicht die Angabe, welche OOXML-Spezifikation beim Speichern im DOCX-Format verwendet wird.

```csharp
public enum OoxmlCompliance
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Ecma376_2006 | `0` | ECMA-376 1. Ausgabe, 2006. |
| Iso29500_2008_Transitional | `1` | ISO/IEC 29500:2008 Übergangskonformitätsstufe. |
| Iso29500_2008_Strict | `2` | ISO/IEC 29500:2008 Strenge Konformitätsstufe. |

## Beispiele

Zeigt, wie DML-Formen in ein Dokument eingefügt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Unten sind zwei Umbrucharten aufgeführt, die Formen haben können.
// 1 - Schwebend:
builder.InsertShape(ShapeType.TopCornersRounded, RelativeHorizontalPosition.Page, 100,
        RelativeVerticalPosition.Page, 100, 50, 50, WrapType.None);

// 2 - Inline:
builder.InsertShape(ShapeType.DiagonalCornersRounded, 50, 50);

// Wenn Sie „nicht-primitive“ Formen erstellen müssen, wie z. B. SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
// TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded oder DiagonalCornersRounded,
// Speichern Sie das Dokument dann mit der Konformität „Strict“ oder „Transitional“, wodurch die Form als DML gespeichert werden kann.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(SaveFormat.Docx);
saveOptions.Compliance = OoxmlCompliance.Iso29500_2008_Transitional;

doc.Save(ArtifactsDir + "Shape.ShapeInsertion.docx", saveOptions);
```

Zeigt, wie eine Liste so konfiguriert wird, dass die Nummerierung bei jedem Abschnitt neu beginnt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

doc.Lists.Add(ListTemplate.NumberDefault);

Aspose.Words.Lists.List list = doc.Lists[0];
list.IsRestartAtEachSection = restartListAtEachSection;

// Die Eigenschaft „IsRestartAtEachSection“ ist nur anwendbar, wenn
// Die OOXML-Konformitätsstufe des Dokuments entspricht einem neueren Standard als „OoxmlComplianceCore.Ecma376“.
OoxmlSaveOptions options = new OoxmlSaveOptions
{
    Compliance = OoxmlCompliance.Iso29500_2008_Transitional
};

builder.ListFormat.List = list;

builder.Writeln("List item 1");
builder.Writeln("List item 2");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Writeln("List item 3");
builder.Writeln("List item 4");

doc.Save(ArtifactsDir + "OoxmlSaveOptions.RestartingDocumentList.docx", options);

doc = new Document(ArtifactsDir + "OoxmlSaveOptions.RestartingDocumentList.docx");

Assert.AreEqual(restartListAtEachSection, doc.Lists[0].IsRestartAtEachSection);
```

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

* namensraum [Aspose.Words.Saving](../../aspose.words.saving/)
* Montage [Aspose.Words](../../)
