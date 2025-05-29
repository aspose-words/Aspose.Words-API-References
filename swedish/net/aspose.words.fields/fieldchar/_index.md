---
title: FieldChar Class
linktitle: FieldChar
articleTitle: FieldChar
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Fields.FieldChar, den viktiga basen för dokumentfälttecken, som förbättrar din dokumentbearbetning och anpassning.
type: docs
weight: 2080
url: /sv/net/aspose.words.fields/fieldchar/
---
## FieldChar class

Basklass för noder som representerar fälttecken i ett dokument.

För att lära dig mer, besök[Arbeta med fält](https://docs.aspose.com/words/net/working-with-fields/) dokumentationsartikel.

```csharp
public abstract class FieldChar : SpecialChar
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Anger anpassad nodidentifierare. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Hämtar dokumentet som denna nod tillhör. |
| [FieldType](../../aspose.words.fields/fieldchar/fieldtype/) { get; } | Returnerar fälttypen. |
| [Font](../../aspose.words/inline/font/) { get; } | Ger åtkomst till teckensnittsformateringen för detta objekt. |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | Returer`sann` om denna nod kan innehålla andra noder. |
| [IsDeleteRevision](../../aspose.words/inline/isdeleterevision/) { get; } | Returnerar sant om det här objektet togs bort i Microsoft Word medan ändringsspårning var aktiverad. |
| [IsDirty](../../aspose.words.fields/fieldchar/isdirty/) { get; set; } | Hämtar eller anger om det aktuella resultatet av fältet inte längre är korrekt (inaktuellt) på grund av andra ändringar som gjorts i dokumentet. |
| [IsFormatRevision](../../aspose.words/inline/isformatrevision/) { get; } | Returnerar sant om objektets formatering ändrades i Microsoft Word medan ändringsspårning var aktiverad. |
| [IsInsertRevision](../../aspose.words/inline/isinsertrevision/) { get; } | Returnerar sant om det här objektet infogades i Microsoft Word medan ändringsspårning var aktiverad. |
| [IsLocked](../../aspose.words.fields/fieldchar/islocked/) { get; set; } | Hämtar eller anger om det överordnade fältet är låst (ska inte beräkna om resultatet). |
| [IsMoveFromRevision](../../aspose.words/inline/ismovefromrevision/) { get; } | Returer`sann` om det här objektet flyttades (raderades) i Microsoft Word medan ändringsspårning var aktiverad. |
| [IsMoveToRevision](../../aspose.words/inline/ismovetorevision/) { get; } | Returer`sann` om det här objektet flyttades (infogades) i Microsoft Word medan ändringsspårning var aktiverad. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Hämtar noden som följer direkt efter denna nod. |
| override [NodeType](../../aspose.words/specialchar/nodetype/) { get; } | ReturerSpecialChar . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Hämtar den omedelbara föräldern till denna nod. |
| [ParentParagraph](../../aspose.words/inline/parentparagraph/) { get; } | Hämtar föräldern[`Paragraph`](../../aspose.words/paragraph/) av denna nod. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Hämtar noden som omedelbart föregår denna nod. |
| [Range](../../aspose.words/node/range/) { get; } | Returnerar en[`Range`](../../aspose.words/range/)objekt som representerar den del av ett dokument som finns i denna nod. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| override [Accept](../../aspose.words/specialchar/accept/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Tar emot en besökare. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Skapar en duplikat av noden. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../../aspose.words/nodetype/)*) | Hämtar den första förfadern till den angivna[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Hämtar den första förfadern till den angivna objekttypen. |
| [GetField](../../aspose.words.fields/fieldchar/getfield/)() | Returnerar ett fält för fältet char. |
| override [GetText](../../aspose.words/specialchar/gettext/)() | Hämtar specialtecknet som denna nod representerar. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../../aspose.words/node/)*) | Hämtar nästa nod enligt algoritmen för förbeställningsträdtraversering. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../../aspose.words/node/)*) | Hämtar föregående nod enligt algoritmen för trädtraversering i förbeställning. |
| [Remove](../../aspose.words/node/remove/)() | Tar bort sig själv från föräldern. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../../aspose.words/saveformat/)*) | Exporterar nodens innehåll till en sträng i det angivna formatet. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Exporterar nodens innehåll till en sträng med de angivna sparalternativen. |

## Anmärkningar

Ett komplett fält i ett Microsoft Word-dokument är en komplex struktur som består av , ett fältstarttecken, fältkod, fältavgränsare, fältresultat och fältsluttecken. Vissa fält har bara fältstart, fältkod och fältslut.

För att enkelt infoga ett nytt fält i ett dokument, använd[`InsertField`](../../aspose.words/documentbuilder/insertfield/) -metoden.

## Exempel

Visar hur man arbetar med en FieldStart-nod.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldDate field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.Format.DateTimeFormat = "dddd, MMMM dd, yyyy";
field.Update();

FieldChar fieldStart = field.Start;

Assert.AreEqual(FieldType.FieldDate, fieldStart.FieldType);
Assert.AreEqual(false, fieldStart.IsDirty);
Assert.AreEqual(false, fieldStart.IsLocked);

// Hämta fasadobjektet som representerar fältet i dokumentet.
field = (FieldDate)fieldStart.GetField();

Assert.AreEqual(false, field.IsLocked);
Assert.AreEqual(" DATE  \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());

// Uppdatera fältet för att visa aktuellt datum.
field.Update();
```

### Se även

* class [FieldStart](../fieldstart/)
* class [FieldSeparator](../fieldseparator/)
* class [FieldEnd](../fieldend/)
* class [SpecialChar](../../aspose.words/specialchar/)
* namnutrymme [Aspose.Words.Fields](../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../)
