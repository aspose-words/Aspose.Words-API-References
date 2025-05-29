---
title: UserInformation Class
linktitle: UserInformation
articleTitle: UserInformation
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Fields.UserInformation för att hantera användarinformation effektivt och förbättra dokumenthanteringen i dina applikationer.
type: docs
weight: 3200
url: /sv/net/aspose.words.fields/userinformation/
---
## UserInformation class

Anger information om användaren.

För att lära dig mer, besök[Arbeta med fält](https://docs.aspose.com/words/net/working-with-fields/) dokumentationsartikel.

```csharp
public class UserInformation
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [UserInformation](userinformation/)() | Default_Constructor |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| static [DefaultUser](../../aspose.words.fields/userinformation/defaultuser/) { get; } | Standardanvändarinformation. |
| [Address](../../aspose.words.fields/userinformation/address/) { get; set; } | Hämtar eller ställer in användarens postadress. |
| [Initials](../../aspose.words.fields/userinformation/initials/) { get; set; } | Hämtar eller ställer in användarens initialer. |
| [Name](../../aspose.words.fields/userinformation/name/) { get; set; } | Hämtar eller ställer in användarens namn. |

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

* namnutrymme [Aspose.Words.Fields](../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../)
