---
title: FieldHyperlink Class
linktitle: FieldHyperlink
articleTitle: FieldHyperlink
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Fields.FieldHyperlink för att enkelt implementera HYPERLINK-fält i dina dokument och förbättra interaktiviteten.
type: docs
weight: 2400
url: /sv/net/aspose.words.fields/fieldhyperlink/
---
## FieldHyperlink class

Implementerar HYPERLINK-fältet

För att lära dig mer, besök[Arbeta med fält](https://docs.aspose.com/words/net/working-with-fields/) dokumentationsartikel.

```csharp
public class FieldHyperlink : Field
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [FieldHyperlink](fieldhyperlink/)() | Default_Constructor |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Address](../../aspose.words.fields/fieldhyperlink/address/) { get; set; } | Hämtar eller anger en plats där denna hyperlänk hoppar. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Hämtar texten som representerar det visade fältresultatet. |
| [End](../../aspose.words.fields/field/end/) { get; } | Hämtar noden som representerar fältets slut. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Får en[`FieldFormat`](../fieldformat/)objekt som ger typad åtkomst till fältets formatering. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Hämtar eller anger om det aktuella resultatet av fältet inte längre är korrekt (inaktuellt) på grund av andra ändringar som gjorts i dokumentet. |
| [IsImageMap](../../aspose.words.fields/fieldhyperlink/isimagemap/) { get; set; } | Hämtar eller anger om koordinater ska läggas till hyperlänken för en bildkarta på serversidan. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Hämtar eller anger om fältet är låst (resultatet ska inte beräknas om). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Hämtar eller ställer in fältets LCID. |
| [OpenInNewWindow](../../aspose.words.fields/fieldhyperlink/openinnewwindow/) { get; set; } | Hämtar eller anger om destinationswebbplatsen ska öppnas i ett nytt webbläsarfönster. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Hämtar eller anger text som är mellan fältavgränsaren och fältslutet. |
| [ScreenTip](../../aspose.words.fields/fieldhyperlink/screentip/) { get; set; } | Hämtar eller ställer in skärmtipstexten för hyperlänken. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Hämtar noden som representerar fältseparatorn. Kan vara`null` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | Hämtar noden som representerar början av fältet. |
| [SubAddress](../../aspose.words.fields/fieldhyperlink/subaddress/) { get; set; } | Hämtar eller anger en plats i filen, till exempel ett bokmärke, dit denna hyperlänk hoppar. |
| [Target](../../aspose.words.fields/fieldhyperlink/target/) { get; set; } | Hämtar eller anger målet som länken ska omdirigeras till. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Hämtar fälttypen Microsoft Word. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Returnerar text mellan fältstart och fältavgränsare (eller fältslut om det inte finns någon avgränsare). Både fältkod och fältresultat för underfält inkluderas. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | Returnerar text mellan fältstart och fältavgränsare (eller fältslut om det inte finns någon avgränsare). |
| [Remove](../../aspose.words.fields/field/remove/)() | Tar bort fältet från dokumentet. Returnerar en nod direkt efter fältet. Om fältets slut är den sista undernoden till dess överordnade nod, returneras dess överordnade stycke. Om fältet redan är borttaget returneras`null` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Utför fältavkopplingen. |
| [Update](../../aspose.words.fields/field/update/)() | Utför fältuppdateringen. Körs om fältet redan uppdateras. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | Utför en fältuppdatering. Körs om fältet redan uppdateras. |

## Anmärkningar

När detta är valt hoppar kontrollen till en plats, till exempel ett bokmärke eller en URL.

## Exempel

Visar hur man använder HYPERLÄNK-fält för att länka till dokument i det lokala filsystemet.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldHyperlink field = (FieldHyperlink)builder.InsertField(FieldType.FieldHyperlink, true);

// När vi klickar på det här HYPERLÄNK-fältet i Microsoft Word,
// den öppnar det länkade dokumentet och placerar sedan markören vid det angivna bokmärket.
field.Address = MyDir + "Bookmarks.docx";
field.SubAddress = "MyBookmark3";
field.ScreenTip = "Open " + field.Address + " on bookmark " + field.SubAddress + " in a new window";

builder.Writeln();

// När vi klickar på det här HYPERLÄNK-fältet i Microsoft Word,
// det öppnar det länkade dokumentet och scrollar automatiskt ner till den angivna iframen.
field = (FieldHyperlink)builder.InsertField(FieldType.FieldHyperlink, true);
field.Address = MyDir + "Iframes.html";
field.ScreenTip = "Open " + field.Address;
field.Target = "iframe_3";
field.OpenInNewWindow = true;
field.IsImageMap = false;

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.HYPERLINK.docx");
```

### Se även

* class [Field](../field/)
* namnutrymme [Aspose.Words.Fields](../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../)
