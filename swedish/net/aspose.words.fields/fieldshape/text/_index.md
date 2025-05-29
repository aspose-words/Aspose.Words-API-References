---
title: FieldShape.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words för .NET
description: Hantera FieldShape-text enkelt – hämta eller ange värden utan ansträngning för sömlös datahämtning och förbättrad funktionalitet i dina applikationer.
type: docs
weight: 20
url: /sv/net/aspose.words.fields/fieldshape/text/
---
## FieldShape.Text property

Hämtar eller ställer in texten som ska hämtas.

```csharp
public string Text { get; set; }
```

## Exempel

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

Visar hur vissa äldre Microsoft Word-fält, som SHAPE och EMBED, hanteras under inläsning.

```csharp
// Öppna ett dokument som skapades i Microsoft Word 2003.
Document doc = new Document(MyDir + "Legacy fields.doc");

// Om vi öppnar Word-dokumentet och trycker Alt+F9, ser vi en SHAPE och ett EMBED-fält.
// Ett SHAPE-fält är ankaret/arbetsytan för ett AutoShape-objekt med radbrytningsstilen "I linje med text" aktiverad.
// Ett EMBED-fält har samma funktion, men för ett inbäddat objekt,
// som till exempel ett kalkylblad från ett externt Excel-dokument.
// Dessa fält kommer dock inte att visas i dokumentets Fields-samling.
Assert.AreEqual(0, doc.Range.Fields.Count);

// Dessa fält stöds endast av äldre versioner av Microsoft Word.
// Dokumentinläsningsprocessen konverterar dessa fält till formobjekt,
// som vi kan komma åt i dokumentets nodsamling.
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);
Assert.AreEqual(3, shapes.Count);

// Den första Shape-noden motsvarar SHAPE-fältet i indatadokumentet,
// vilket är den inbäddade arbetsytan för autoformen.
Shape shape = (Shape)shapes[0];
Assert.AreEqual(ShapeType.Image, shape.ShapeType);

// Den andra formnoden är själva autoformen.
shape = (Shape)shapes[1];
Assert.AreEqual(ShapeType.Can, shape.ShapeType);

// Den tredje formen är det som var EMBED-fältet som innehöll det externa kalkylbladet.
shape = (Shape)shapes[2];
Assert.AreEqual(ShapeType.OleObject, shape.ShapeType);
```

### Se även

* class [FieldShape](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
