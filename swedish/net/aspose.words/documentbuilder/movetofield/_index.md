---
title: DocumentBuilder.MoveToField
linktitle: MoveToField
articleTitle: MoveToField
second_title: Aspose.Words för .NET
description: Navigera enkelt i dina dokument med DocumentBuilder MoveToField-metoden, vilket möjliggör snabb markörförflyttning till valfritt fält för förbättrad redigeringseffektivitet.
type: docs
weight: 570
url: /sv/net/aspose.words/documentbuilder/movetofield/
---
## DocumentBuilder.MoveToField method

Flyttar markören till ett fält i dokumentet.

```csharp
public void MoveToField(Field field, bool isAfter)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| field | Field | Fältet att flytta markören till. |
| isAfter | Boolean | När`sann` , flyttar markören så att den är efter fältets slut. När`falsk`, flyttar markören så att den är före fältets början. |

## Exempel

Visar hur man flyttar en dokumentbyggares nodinsättningspunktsmarkör till ett specifikt fält.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga ett fält med hjälp av DocumentBuilder och lägg till en textsekvens efter det.
Field field = builder.InsertField(" AUTHOR \"John Doe\" ");

// Skaparens markör är för närvarande i slutet av dokumentet.
Assert.Null(builder.CurrentNode);

// Flytta markören till fältet medan du anger om markören ska placeras före eller efter fältet.
builder.MoveToField(field, moveCursorToAfterTheField);

// Observera att markören är utanför fältet i båda fallen.
// Det här betyder att vi inte kan redigera fältet med hjälp av verktyget så här.
// För att redigera ett fält kan vi använda byggarens MoveTo-metod på ett fälts FieldStart
// eller FieldSeparator-nod för att placera markören inuti.
if (moveCursorToAfterTheField)
{
    Assert.Null(builder.CurrentNode);
    builder.Write(" Text immediately after the field.");

    Assert.AreEqual("\u0013 AUTHOR \"John Doe\" \u0014John Doe\u0015 Text immediately after the field.", 
        doc.GetText().Trim());
}
else
{
    Assert.AreEqual(field.Start, builder.CurrentNode);
    builder.Write("Text immediately before the field. ");

    Assert.AreEqual("Text immediately before the field. \u0013 AUTHOR \"John Doe\" \u0014John Doe\u0015", 
        doc.GetText().Trim());
}
```

### Se även

* class [Field](../../../aspose.words.fields/field/)
* class [DocumentBuilder](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
