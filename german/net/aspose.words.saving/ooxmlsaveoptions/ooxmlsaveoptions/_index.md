---
title: OoxmlSaveOptions
linktitle: OoxmlSaveOptions
articleTitle: OoxmlSaveOptions
second_title: Aspose.Words für .NET
description: Entdecken Sie den OoxmlSaveOptions-Konstruktor, um Dokumente mühelos im Docx-Format zu speichern. Profitieren Sie von nahtlosem Dokumentenmanagement und verbesserter Kompatibilität.
type: docs
weight: 10
url: /de/net/aspose.words.saving/ooxmlsaveoptions/ooxmlsaveoptions/
---
## OoxmlSaveOptions() {#constructor}

Initialisiert eine neue Instanz dieser Klasse, die zum Speichern eines Dokuments imDocx format.

```csharp
public OoxmlSaveOptions()
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

* class [OoxmlSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)

---

## OoxmlSaveOptions(*[SaveFormat](../../../aspose.words/saveformat/)*) {#constructor_1}

Initialisiert eine neue Instanz dieser Klasse, die zum Speichern eines Dokuments imDocx , Docm ,Dotx ,Dotm oder FlatOpc format.

```csharp
public OoxmlSaveOptions(SaveFormat saveFormat)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| saveFormat | SaveFormat | Kann seinDocx ,Docm , Dotx ,Dotm oderFlatOpc . |

## Beispiele

Zeigt, wie ältere Steuerzeichen bei der Konvertierung in .docx unterstützt werden.

```csharp
Document doc = new Document(MyDir + "Legacy control character.doc");

// Wenn wir das Dokument in einem OOXML-Format speichern, können wir ein OoxmlSaveOptions-Objekt erstellen
// und übergeben Sie es dann an die Speichermethode des Dokuments, um zu ändern, wie wir das Dokument speichern.
// Setzen Sie die Eigenschaft "KeepLegacyControlChars" auf "true", um
// das Legacy-Zeichen „ShortDateTime“ beim Speichern.
// Setzen Sie die Eigenschaft "KeepLegacyControlChars" auf "false", um
// das Legacy-Zeichen „ShortDateTime“ aus dem Ausgabedokument.
OoxmlSaveOptions so = new OoxmlSaveOptions(SaveFormat.Docx);
so.KeepLegacyControlChars = keepLegacyControlChars;

doc.Save(ArtifactsDir + "OoxmlSaveOptions.KeepLegacyControlChars.docx", so);

doc = new Document(ArtifactsDir + "OoxmlSaveOptions.KeepLegacyControlChars.docx");

Assert.AreEqual(keepLegacyControlChars ? "\u0013date \\@ \"MM/dd/yyyy\"\u0014\u0015\f" : "\u001e\f",
    doc.FirstSection.Body.GetText());
```

### Siehe auch

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [OoxmlSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
