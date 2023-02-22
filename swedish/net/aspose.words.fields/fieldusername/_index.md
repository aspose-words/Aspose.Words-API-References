---
title: Class FieldUserName
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Fields.FieldUserName klass. Implementerar fältet USERNAME.
type: docs
weight: 2440
url: /sv/net/aspose.words.fields/fieldusername/
---
## FieldUserName class

Implementerar fältet USERNAME.

```csharp
public class FieldUserName : Field
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [FieldUserName](fieldusername/)() | Default_Constructor |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Hämtar texten som representerar det visade fältresultatet. |
| [End](../../aspose.words.fields/field/end/) { get; } | Hämtar noden som representerar fältänden. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Får en[`FieldFormat`](../fieldformat/) objekt som ger maskinskriven åtkomst till fältets formatering. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Hämtar eller ställer in om det aktuella resultatet av fältet inte längre är korrekt (inaktuellt) på grund av andra ändringar som gjorts i dokumentet. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Hämtar eller ställer in om fältet är låst (ska inte räkna om resultatet). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Hämtar eller ställer in LCID för fältet. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Hämtar eller ställer in text som är mellan fältavgränsaren och fältslutet. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Hämtar noden som representerar fältseparatorn. Kan vara null. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Hämtar noden som representerar början av fältet. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Hämtar fälttypen Microsoft Word. |
| [UserName](../../aspose.words.fields/fieldusername/username/) { get; set; } | Gest eller ställer in den nuvarande användarens namn. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Returnerar text mellan fältstart och fältavgränsare (eller fältslut om det inte finns någon avgränsare). Både fältkod och fältresultat för underordnade fält ingår. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(bool) | Returnerar text mellan fältstart och fältavgränsare (eller fältslut om det inte finns någon avgränsare). |
| [Remove](../../aspose.words.fields/field/remove/)() | Tar bort fältet från dokumentet. Returnerar en nod direkt efter fältet. Om fältets slut är den sista child av dess överordnade nod, returnerar dess överordnade stycke. Om fältet redan är borttaget, returneras **null** . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Utför fältavlänkningen. |
| [Update](../../aspose.words.fields/field/update/)() | Utför fältuppdateringen. Kastar om fältet redan uppdateras. |
| [Update](../../aspose.words.fields/field/update/)(bool) | Utför en fältuppdatering. Kastar om fältet redan uppdateras. |

### Anmärkningar

Hämtar den aktuella användarens namn.

### Exempel

Visar hur man använder fältet USERNAME.

```csharp
Document doc = new Document();

// Skapa ett UserInformation-objekt och ställ in det som källa för användarinformation för alla fält som vi skapar.
UserInformation userInformation = new UserInformation();
userInformation.Name = "John Doe";
doc.FieldOptions.CurrentUser = userInformation;

DocumentBuilder builder = new DocumentBuilder(doc);

// Skapa ett ANVÄNDARNAMN-fält för att visa den aktuella användarens namn,
// hämtat från UserInformation-objektet vi skapade ovan.
FieldUserName fieldUserName = (FieldUserName)builder.InsertField(FieldType.FieldUserName, true);
Assert.AreEqual(userInformation.Name, fieldUserName.Result);

Assert.AreEqual(" USERNAME ", fieldUserName.GetFieldCode());
Assert.AreEqual("John Doe", fieldUserName.Result);

  // Vi kan ställa in den här egenskapen för att få vårt fält att åsidosätta värdet som för närvarande är lagrat i UserInformation-objektet.
fieldUserName.UserName = "Jane Doe";
fieldUserName.Update();

Assert.AreEqual(" USERNAME  \"Jane Doe\"", fieldUserName.GetFieldCode());
Assert.AreEqual("Jane Doe", fieldUserName.Result);

// Detta påverkar inte värdet i UserInformation-objektet.
Assert.AreEqual("John Doe", doc.FieldOptions.CurrentUser.Name);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.USERNAME.docx");
```

### Se även

* class [Field](../field/)
* namnutrymme [Aspose.Words.Fields](../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../)


