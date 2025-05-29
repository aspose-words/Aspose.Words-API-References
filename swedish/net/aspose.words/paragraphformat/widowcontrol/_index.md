---
title: ParagraphFormat.WidowControl
linktitle: WidowControl
articleTitle: WidowControl
second_title: Aspose.Words för .NET
description: Upptäck hur egenskapen ParagraphFormat WidowControl säkerställer att textens första och sista rader förblir tillsammans på samma sida för bättre läsbarhet.
type: docs
weight: 410
url: /sv/net/aspose.words/paragraphformat/widowcontrol/
---
## ParagraphFormat.WidowControl property

Sant om den första och sista raden i stycket ska förbli på samma sida som resten av stycket.

```csharp
public bool WidowControl { get; set; }
```

## Exempel

Visar hur man aktiverar kontrollen över änkor/överflödiga inställningar för ett stycke.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// När vi skriver text som inte får plats på en sida kan en rad spillas över till nästa sida.
// Den enda raden som hamnar på nästa sida kallas en "Orphan",
// och den föregående raden där det föräldralösa barnet avbröts kallas en "Änka".
// Vi kan åtgärda föräldralösa barn och änkor genom att ordna om texten via teckenstorlek, avstånd eller sidmarginaler.
// Om vi vill behålla dokumentets dimensioner kan vi ställa in denna flagga på "sant"
// att få änkor att samarbeta med sina respektive föräldralösa barn.
// Om denna flagga lämnas som "falsk" lämnas änka/föräldralösa par kvar i texten.
// Varje stycke har den här inställningen tillgänglig i Microsoft Word via Hem -> Stycke -> Styckeinställningar
// (knapp längst ner till höger på fliken "Stycke") -> "Kontroll för änka/föräldralös".
builder.ParagraphFormat.WidowControl = widowControl; 

// Infoga text som producerar en föräldralös och en änka.
builder.Font.Size = 68;
builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc.Save(ArtifactsDir + "ParagraphFormat.WidowControl.docx");
```

### Se även

* class [ParagraphFormat](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
