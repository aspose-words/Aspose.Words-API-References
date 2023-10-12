---
title: UserInformation.DefaultUser
second_title: Aspose.Words för .NET API Referens
description: UserInformation fast egendom. Standardanvändarinformation.
type: docs
weight: 20
url: /sv/net/aspose.words.fields/userinformation/defaultuser/
---
## UserInformation.DefaultUser property

Standardanvändarinformation.

```csharp
public static UserInformation DefaultUser { get; }
```

### Anmärkningar

Använd[`CurrentUser`](../../fieldoptions/currentuser/) egenskap för att ange användarinformation för enstaka dokument.

### Exempel

Visar hur du ställer in användarinformation och visar dem med hjälp av fält.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Skapa ett UserInformation-objekt och ställ in det som datakälla för fält som visar användarinformation.
UserInformation userInformation = new UserInformation
{
    Name = "John Doe",
    Initials = "J. D.",
    Address = "123 Main Street"
};
doc.FieldOptions.CurrentUser = userInformation;

// Infoga fälten USERNAME, USERINITIALS och USERADDRESS, som visar värden på
 // respektive egenskaper för UserInformation-objektet som vi har skapat ovan.
Assert.AreEqual(userInformation.Name, builder.InsertField(" USERNAME ").Result);
Assert.AreEqual(userInformation.Initials, builder.InsertField(" USERINITIALS ").Result);
Assert.AreEqual(userInformation.Address, builder.InsertField(" USERADDRESS ").Result);

// Fältalternativsobjektet har också en statisk standardanvändare som fält från alla dokument kan referera till.
UserInformation.DefaultUser.Name = "Default User";
UserInformation.DefaultUser.Initials = "D. U.";
UserInformation.DefaultUser.Address = "One Microsoft Way";
doc.FieldOptions.CurrentUser = UserInformation.DefaultUser;

Assert.AreEqual("Default User", builder.InsertField(" USERNAME ").Result);
Assert.AreEqual("D. U.", builder.InsertField(" USERINITIALS ").Result);
Assert.AreEqual("One Microsoft Way", builder.InsertField(" USERADDRESS ").Result);

doc.UpdateFields();
doc.Save(ArtifactsDir + "FieldOptions.CurrentUser.docx");
```

### Se även

* class [UserInformation](../)
* namnutrymme [Aspose.Words.Fields](../../userinformation/)
* hopsättning [Aspose.Words](../../../)


