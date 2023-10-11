---
title: ParagraphFormat.WidowControl
second_title: Aspose.Words för .NET API Referens
description: ParagraphFormat fast egendom. Sant om första och sista raden i stycket ska vara kvar på samma sida som resten av stycket.
type: docs
weight: 400
url: /sv/net/aspose.words/paragraphformat/widowcontrol/
---
## ParagraphFormat.WidowControl property

Sant om första och sista raden i stycket ska vara kvar på samma sida som resten av stycket.

```csharp
public bool WidowControl { get; set; }
```

### Exempel

Visar hur man aktiverar änka/föräldralös kontroll för ett stycke.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// När vi skriver texten som inte får plats på en sida kan en rad spilla över på nästa sida.
// Den enstaka raden som hamnar på nästa sida kallas för "Orphan",
// och föregående rad där den föräldralösa bröt av kallas "Änka".
// Vi kan fixa föräldralösa barn och änkor genom att ordna om text via teckenstorlek, mellanrum eller sidmarginaler.
// Om vi vill bevara vårt dokuments dimensioner kan vi ställa in denna flagga på "true"
 // för att trycka in änkor på samma sida som deras respektive föräldralösa barn.
// Lämna denna flagga som "false" kommer att lämna änka/föräldralösa par i text.
// Varje stycke har denna inställning tillgänglig i Microsoft Word via Hem -> Stycke -> Styckeinställningar
// (knappen i det nedre högra hörnet av "Paragraph"-fliken) -> "Änka/föräldralös kontroll".
builder.ParagraphFormat.WidowControl = widowControl; 

// Infoga text som ger ett föräldralöst barn och en änka.
builder.Font.Size = 68;
builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc.Save(ArtifactsDir + "ParagraphFormat.WidowControl.docx");
```

### Se även

* class [ParagraphFormat](../)
* namnutrymme [Aspose.Words](../../paragraphformat/)
* hopsättning [Aspose.Words](../../../)


