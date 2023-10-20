---
title: DocumentBuilder.MoveToField
linktitle: MoveToField
articleTitle: MoveToField
second_title: Aspose.Words för .NET
description: DocumentBuilder MoveToField metod. Flyttar markören till ett fält i dokumentet i C#.
type: docs
weight: 530
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
| isAfter | Boolean | När`Sann` , flyttar markören så att den hamnar efter fältets slut. When`falsk`, flyttar markören till att vara före fältstarten. |

## Exempel

Visar hur man flyttar markören för en dokumentbyggares nodinsättningspunkt till ett specifikt fält.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga ett fält med DocumentBuilder och lägg till en serie text efter det.
Field field = builder.InsertField(" AUTHOR \"John Doe\" ");

// Byggarens markör är för närvarande i slutet av dokumentet.
Assert.Null(builder.CurrentNode);

// Flytta markören till fältet samtidigt som du anger om markören ska placeras före eller efter fältet.
builder.MoveToField(field, moveCursorToAfterTheField);

// Observera att markören är utanför fältet i båda fallen.
// Det betyder att vi inte kan redigera fältet med hjälp av byggaren så här.
// För att redigera ett fält kan vi använda byggarens MoveTo-metod på ett fälts FieldStart
// eller FieldSeparator-noden för att placera markören inuti.
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
