---
title: UserInformation.Name
linktitle: Name
articleTitle: Name
second_title: Aspose.Words för .NET
description: Hantera enkelt användarprofiler med egenskapen UserInformation Name. Hämta eller uppdatera enkelt användarnamn för förbättrad anpassning.
type: docs
weight: 50
url: /sv/net/aspose.words.fields/userinformation/name/
---
## UserInformation.Name property

Hämtar eller ställer in användarens namn.

```csharp
public string Name { get; set; }
```

## Exempel

Visar hur man anger användaruppgifter och visar dem med hjälp av fält.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Skapa ett UserInformation-objekt och ange det som datakälla för fält som visar användarinformation.
UserInformation userInformation = new UserInformation
{
    Name = "John Doe",
    Initials = "J. D.",
    Address = "123 Main Street"
};
doc.FieldOptions.CurrentUser = userInformation;

// Infoga fälten ANVÄNDARNAMN, ANVÄNDARINITIALS och ANVÄNDARADRESS, som visar värden för
 // respektive egenskaper för UserInformation-objektet som vi har skapat ovan.
Assert.AreEqual(userInformation.Name, builder.InsertField(" USERNAME ").Result);
Assert.AreEqual(userInformation.Initials, builder.InsertField(" USERINITIALS ").Result);
Assert.AreEqual(userInformation.Address, builder.InsertField(" USERADDRESS ").Result);

// Objektet fältalternativ har också en statisk standardanvändare som fält från alla dokument kan referera till.
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
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
