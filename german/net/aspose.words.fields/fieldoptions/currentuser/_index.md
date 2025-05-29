---
title: FieldOptions.CurrentUser
linktitle: CurrentUser
articleTitle: CurrentUser
second_title: Aspose.Words für .NET
description: Entdecken Sie die FieldOptions CurrentUser-Eigenschaft, um Benutzerinformationen mühelos zu verwalten und anzupassen und so die Funktionalität Ihrer Anwendungen zu verbessern.
type: docs
weight: 50
url: /de/net/aspose.words.fields/fieldoptions/currentuser/
---
## FieldOptions.CurrentUser property

Ruft die aktuellen Benutzerinformationen ab oder legt sie fest.

```csharp
public UserInformation CurrentUser { get; set; }
```

## Beispiele

Zeigt, wie Benutzerdetails festgelegt und mithilfe von Feldern angezeigt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Erstellen Sie ein UserInformation-Objekt und legen Sie es als Datenquelle für Felder fest, die Benutzerinformationen anzeigen.
UserInformation userInformation = new UserInformation
{
    Name = "John Doe",
    Initials = "J. D.",
    Address = "123 Main Street"
};
doc.FieldOptions.CurrentUser = userInformation;

// Fügen Sie die Felder USERNAME, USERINITIALS und USERADDRESS ein, die Werte von
    // die jeweiligen Eigenschaften des UserInformation-Objekts, das wir oben erstellt haben.
Assert.AreEqual(userInformation.Name, builder.InsertField(" USERNAME ").Result);
Assert.AreEqual(userInformation.Initials, builder.InsertField(" USERINITIALS ").Result);
Assert.AreEqual(userInformation.Address, builder.InsertField(" USERADDRESS ").Result);

// Das Feldoptionenobjekt hat auch einen statischen Standardbenutzer, auf den Felder aus allen Dokumenten verweisen können.
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

### Siehe auch

* class [UserInformation](../../userinformation/)
* class [FieldOptions](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
