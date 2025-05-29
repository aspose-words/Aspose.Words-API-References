---
title: UserInformation Class
linktitle: UserInformation
articleTitle: UserInformation
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Fields.UserInformation, um Benutzerdetails effektiv zu verwalten und die Dokumentverarbeitung in Ihren Anwendungen zu verbessern.
type: docs
weight: 3200
url: /de/net/aspose.words.fields/userinformation/
---
## UserInformation class

Gibt Informationen über den Benutzer an.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Feldern](https://docs.aspose.com/words/net/working-with-fields/) Dokumentationsartikel.

```csharp
public class UserInformation
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [UserInformation](userinformation/)() | Default_Constructor |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| static [DefaultUser](../../aspose.words.fields/userinformation/defaultuser/) { get; } | Standardbenutzerinformationen. |
| [Address](../../aspose.words.fields/userinformation/address/) { get; set; } | Ruft die Postanschrift des Benutzers ab oder legt sie fest. |
| [Initials](../../aspose.words.fields/userinformation/initials/) { get; set; } | Ruft die Initialen des Benutzers ab oder legt sie fest. |
| [Name](../../aspose.words.fields/userinformation/name/) { get; set; } | Ruft den Namen des Benutzers ab oder legt ihn fest. |

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

* namensraum [Aspose.Words.Fields](../../aspose.words.fields/)
* Montage [Aspose.Words](../../)
