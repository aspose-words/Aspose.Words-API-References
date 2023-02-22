---
title: FieldUserInitials.UserInitials
second_title: Aspose.Words för .NET API Referens
description: FieldUserInitials fast egendom. Hämtar eller ställer in den nuvarande användarens initialer.
type: docs
weight: 20
url: /sv/net/aspose.words.fields/fielduserinitials/userinitials/
---
## FieldUserInitials.UserInitials property

Hämtar eller ställer in den nuvarande användarens initialer.

```csharp
public string UserInitials { get; set; }
```

### Exempel

Visar hur man använder fältet ANVÄNDARINFORMATION.

```csharp
Document doc = new Document();

// Skapa ett UserInformation-objekt och ställ in det som källa för användarinformation för alla fält som vi skapar.
UserInformation userInformation = new UserInformation();
userInformation.Initials = "J. D.";
doc.FieldOptions.CurrentUser = userInformation;

// Skapa ett USERINITIALS-fält för att visa den aktuella användarens initialer,
// hämtat från UserInformation-objektet vi skapade ovan.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldUserInitials fieldUserInitials = (FieldUserInitials)builder.InsertField(FieldType.FieldUserInitials, true);
Assert.AreEqual(userInformation.Initials, fieldUserInitials.Result);

Assert.AreEqual(" USERINITIALS ", fieldUserInitials.GetFieldCode());
Assert.AreEqual("J. D.", fieldUserInitials.Result);

  // Vi kan ställa in den här egenskapen för att få vårt fält att åsidosätta värdet som för närvarande är lagrat i UserInformation-objektet.
fieldUserInitials.UserInitials = "J. C.";
fieldUserInitials.Update();

Assert.AreEqual(" USERINITIALS  \"J. C.\"", fieldUserInitials.GetFieldCode());
Assert.AreEqual("J. C.", fieldUserInitials.Result);

// Detta påverkar inte värdet i UserInformation-objektet.
Assert.AreEqual("J. D.", doc.FieldOptions.CurrentUser.Initials);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.USERINITIALS.docx");
```

### Se även

* class [FieldUserInitials](../)
* namnutrymme [Aspose.Words.Fields](../../fielduserinitials/)
* hopsättning [Aspose.Words](../../../)


