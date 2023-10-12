---
title: OoxmlSaveOptions.OoxmlSaveOptions
second_title: Aspose.Words för .NET API Referens
description: OoxmlSaveOptions byggare. Initierar en ny instans av denna klass som kan användas för att spara ett dokument iDocx format.
type: docs
weight: 10
url: /sv/net/aspose.words.saving/ooxmlsaveoptions/ooxmlsaveoptions/
---
## OoxmlSaveOptions() {#constructor}

Initierar en ny instans av denna klass som kan användas för att spara ett dokument iDocx format.

```csharp
public OoxmlSaveOptions()
```

### Exempel

Visar hur man ställer in en OOXML-efterlevnadsspecifikation för ett sparat dokument att följa.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Om vi konfigurerar kompatibilitetsalternativ för att följa Microsoft Word 2003,
// att infoga en bild kommer att definiera dess form med VML.
doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2003);
builder.InsertImage(ImageDir + "Transparent background logo.png");

Assert.AreEqual(ShapeMarkupLanguage.Vml, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).MarkupLanguage);

// OOXML-standarden "ISO/IEC 29500:2008" stöder inte VML-former.
// Om vi ställer in egenskapen "Compliance" för SaveOptions-objektet till "OoxmlCompliance.Iso29500_2008_Strict",
 // alla dokument vi sparar när vi skickar detta objekt måste följa den standarden.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions
{
    Compliance = OoxmlCompliance.Iso29500_2008_Strict,
    SaveFormat = SaveFormat.Docx
};

doc.Save(ArtifactsDir + "OoxmlSaveOptions.Iso29500Strict.docx", saveOptions);

// Vårt sparade dokument definierar formen med DML för att följa OOXML-standarden "ISO/IEC 29500:2008".
doc = new Document(ArtifactsDir + "OoxmlSaveOptions.Iso29500Strict.docx");

Assert.AreEqual(ShapeMarkupLanguage.Dml, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).MarkupLanguage);
```

### Se även

* class [OoxmlSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../ooxmlsaveoptions/)
* hopsättning [Aspose.Words](../../../)

---

## OoxmlSaveOptions(SaveFormat) {#constructor_1}

Initierar en ny instans av denna klass som kan användas för att spara ett dokument iDocx , Docm ,Dotx ,Dotm or FlatOpc format.

```csharp
public OoxmlSaveOptions(SaveFormat saveFormat)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| saveFormat | SaveFormat | Kan varaDocx ,Docm , Dotx ,Dotm ellerFlatOpc . |

### Exempel

Visar hur man stöder äldre kontrolltecken vid konvertering till .docx.

```csharp
Document doc = new Document(MyDir + "Legacy control character.doc");

// När vi sparar dokumentet i ett OOXML-format kan vi skapa ett OoxmlSaveOptions-objekt
// och skicka det sedan till dokumentets sparmetod för att ändra hur vi sparar dokumentet.
// Ställ in egenskapen "KeepLegacyControlChars" till "true" för att bevara
// det äldre tecknet "ShortDateTime" när du sparar.
// Ställ in egenskapen "KeepLegacyControlChars" till "false" för att ta bort
// det äldre tecknet "ShortDateTime" från utdatadokumentet.
OoxmlSaveOptions so = new OoxmlSaveOptions(SaveFormat.Docx);
so.KeepLegacyControlChars = keepLegacyControlChars;

doc.Save(ArtifactsDir + "OoxmlSaveOptions.KeepLegacyControlChars.docx", so);

doc = new Document(ArtifactsDir + "OoxmlSaveOptions.KeepLegacyControlChars.docx");

Assert.AreEqual(keepLegacyControlChars ? "\u0013date \\@ \"MM/dd/yyyy\"\u0014\u0015\f" : "\u001e\f",
    doc.FirstSection.Body.GetText());
```

### Se även

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [OoxmlSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../ooxmlsaveoptions/)
* hopsättning [Aspose.Words](../../../)


