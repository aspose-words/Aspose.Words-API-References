---
title: ParagraphFormat.Bidi
linktitle: Bidi
articleTitle: Bidi
second_title: Aspose.Words för .NET
description: Upptäck egenskapen ParagraphFormat Bidi för att enkelt styra textformatering från höger till vänster för förbättrad läsbarhet och dokumentlayout.
type: docs
weight: 50
url: /sv/net/aspose.words/paragraphformat/bidi/
---
## ParagraphFormat.Bidi property

Hämtar eller anger om detta är ett stycke som skrivs från höger till vänster.

```csharp
public bool Bidi { get; set; }
```

## Anmärkningar

När`sann`, körningarna och andra inline-objekt i detta stycke är utplacerade från höger till vänster.

## Exempel

Visar hur man identifierar textriktningen i klartextdokument.

```csharp
// Skapa ett "TxtLoadOptions"-objekt, som vi kan skicka till ett dokuments konstruktor
// för att ändra hur vi laddar ett klartextdokument.
TxtLoadOptions loadOptions = new TxtLoadOptions();

// Sätt egenskapen "DocumentDirection" till "DocumentDirection.Auto" identifierar automatiskt
// riktningen för varje textstycke som Aspose.Words laddar från klartext.
// Varje styckes "Bidi"-egenskap lagrar dess riktning.
loadOptions.DocumentDirection = DocumentDirection.Auto;

// Identifiera hebreisk text som höger-till-vänster.
Document doc = new Document(MyDir + "Hebrew text.txt", loadOptions);

Assert.True(doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Bidi);

// Identifiera engelsk text som höger-till-vänster.
doc = new Document(MyDir + "English text.txt", loadOptions);

Assert.False(doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Bidi);
```

Visar hur man skapar listor som är kompatibla med höger-till-vänster-skrivrutor med BIDIOUTLINE-fält.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// BIDIOUTLINE-fältet numrerar stycken på samma sätt som AUTONUMM/LISTNUM-fälten,
// men är bara synlig när ett höger-till-vänster-redigeringsspråk är aktiverat, till exempel hebreiska eller arabiska.
// Följande fält visar ".1", RTL-motsvarigheten till listnummer "1.".
FieldBidiOutline field = (FieldBidiOutline)builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");

Assert.AreEqual(" BIDIOUTLINE ", field.GetFieldCode());

// Lägg till två fler BIDIOUTLINE-fält, som visar ".2" och ".3".
builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");
builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");

// Ställ in den horisontella textjusteringen för varje stycke i dokumentet till RTL.
foreach (Paragraph para in doc.GetChildNodes(NodeType.Paragraph, true))
{
    para.ParagraphFormat.Bidi = true;
}

// Om vi aktiverar ett höger-till-vänster-redigeringsspråk i Microsoft Word kommer våra fält att visa siffror.
// Annars visas "###".
doc.Save(ArtifactsDir + "Field.BIDIOUTLINE.docx");
```

### Se även

* class [ParagraphFormat](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
