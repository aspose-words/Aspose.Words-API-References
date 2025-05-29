---
title: ShapeMarkupLanguage Enum
linktitle: ShapeMarkupLanguage
articleTitle: ShapeMarkupLanguage
second_title: Aspose.Words för .NET
description: Upptäck enumerationen Aspose.Words.Drawing.ShapeMarkupLanguage, som definierar markupspråk för former för förbättrad dokumentformatering och designflexibilitet.
type: docs
weight: 1670
url: /sv/net/aspose.words.drawing/shapemarkuplanguage/
---
## ShapeMarkupLanguage enumeration

Anger vilket markupspråk som används för formen.

```csharp
public enum ShapeMarkupLanguage : byte
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Dml | `0` | Ritning Markup Language används för att definiera formen. |
| Vml | `1` | Vektormarkeringsspråk används för att definiera formen. |

## Exempel

Visar hur man ställer in en OOXML-efterlevnadsspecifikation som ett sparat dokument ska följa.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Om vi konfigurerar kompatibilitetsalternativ så att de följer Microsoft Word 2003,
// att infoga en bild definierar dess form med hjälp av VML.
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

// Vårt sparade dokument definierar formen med hjälp av DML för att följa OOXML-standarden "ISO/IEC 29500:2008".
doc = new Document(ArtifactsDir + "OoxmlSaveOptions.Iso29500Strict.docx");

Assert.AreEqual(ShapeMarkupLanguage.Dml, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).MarkupLanguage);
```

### Se även

* namnutrymme [Aspose.Words.Drawing](../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../)
