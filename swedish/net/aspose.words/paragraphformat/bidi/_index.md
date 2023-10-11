---
title: ParagraphFormat.Bidi
second_title: Aspose.Words för .NET API Referens
description: ParagraphFormat fast egendom. Hämtar eller ställer in om detta är ett stycke från höger till vänster.
type: docs
weight: 50
url: /sv/net/aspose.words/paragraphformat/bidi/
---
## ParagraphFormat.Bidi property

Hämtar eller ställer in om detta är ett stycke från höger till vänster.

```csharp
public bool Bidi { get; set; }
```

### Anmärkningar

När`Sann`, körningarna och andra inline-objekt i denna paragraph läggs ut från höger till vänster.

### Exempel

Visar hur man upptäcker textriktning i klartextdokument.

```csharp
// Skapa ett "TxtLoadOptions"-objekt, som vi kan skicka till ett dokuments konstruktor
// för att ändra hur vi laddar ett dokument i klartext.
TxtLoadOptions loadOptions = new TxtLoadOptions();

// Ställ in egenskapen "DocumentDirection" till "DocumentDirection.Auto" upptäcker automatiskt
// riktningen för varje textstycke som Aspose.Words laddar från klartext.
// Varje styckes "Bidi"-egenskap kommer att lagra dess riktning.
loadOptions.DocumentDirection = DocumentDirection.Auto;

// Upptäck hebreisk text som höger till vänster.
Document doc = new Document(MyDir + "Hebrew text.txt", loadOptions);

Assert.True(doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Bidi);

// Upptäck engelsk text som höger till vänster.
doc = new Document(MyDir + "English text.txt", loadOptions);

Assert.False(doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Bidi);
```

Visar hur man skapar höger-till-vänster språkkompatibla listor med BIDIOUTLINE-fält.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// BIDIOUTLINE-fältet numrerar stycken som AUTONUM/LISTNUM-fälten,
// men är bara synlig när ett redigeringsspråk från höger till vänster är aktiverat, till exempel hebreiska eller arabiska.
// Följande fält kommer att visa ".1", RTL-motsvarigheten till listnummer "1.".
FieldBidiOutline field = (FieldBidiOutline)builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");

Assert.AreEqual(" BIDIOUTLINE ", field.GetFieldCode());

// Lägg till ytterligare två BIDIOUTLINE-fält, som kommer att visa ".2" och ".3".
builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");
builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");

// Ställ in den horisontella textjusteringen för varje stycke i dokumentet till RTL.
foreach (Paragraph para in doc.GetChildNodes(NodeType.Paragraph, true))
{
    para.ParagraphFormat.Bidi = true;
}

// Om vi aktiverar ett redigeringsspråk från höger till vänster i Microsoft Word kommer våra fält att visa siffror.
// Annars kommer de att visa "###".
doc.Save(ArtifactsDir + "Field.BIDIOUTLINE.docx");
```

### Se även

* class [ParagraphFormat](../)
* namnutrymme [Aspose.Words](../../paragraphformat/)
* hopsättning [Aspose.Words](../../../)


