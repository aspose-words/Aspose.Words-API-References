---
title: FieldUserInitials.UserInitials
linktitle: UserInitials
articleTitle: UserInitials
second_title: Aspose.Words für .NET
description: Greifen Sie auf die Eigenschaft „FieldUserInitials“ zu und passen Sie sie an, um Benutzerinitialen mühelos zu verwalten und so die Personalisierung und das Benutzererlebnis zu verbessern.
type: docs
weight: 20
url: /de/net/aspose.words.fields/fielduserinitials/userinitials/
---
## FieldUserInitials.UserInitials property

Ruft die Initialen des aktuellen Benutzers ab oder legt sie fest.

```csharp
public string UserInitials { get; set; }
```

## Beispiele

Zeigt, wie das Feld BENUTZERINITIALEN verwendet wird.

```csharp
Document doc = new Document();

// Erstellen Sie ein UserInformation-Objekt und legen Sie es als Quelle der Benutzerinformationen für alle von uns erstellten Felder fest.
UserInformation userInformation = new UserInformation();
userInformation.Initials = "J. D.";
doc.FieldOptions.CurrentUser = userInformation;

// Erstellen Sie ein USERINITIALS-Feld, um die Initialen des aktuellen Benutzers anzuzeigen.
// aus dem UserInformation-Objekt übernommen, das wir oben erstellt haben.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldUserInitials fieldUserInitials = (FieldUserInitials)builder.InsertField(FieldType.FieldUserInitials, true);
Assert.AreEqual(userInformation.Initials, fieldUserInitials.Result);

Assert.AreEqual(" USERINITIALS ", fieldUserInitials.GetFieldCode());
Assert.AreEqual("J. D.", fieldUserInitials.Result);

    // Wir können diese Eigenschaft festlegen, damit unser Feld den aktuell im UserInformation-Objekt gespeicherten Wert überschreibt.
fieldUserInitials.UserInitials = "J. C.";
fieldUserInitials.Update();

Assert.AreEqual(" USERINITIALS  \"J. C.\"", fieldUserInitials.GetFieldCode());
Assert.AreEqual("J. C.", fieldUserInitials.Result);

// Dies hat keine Auswirkungen auf den Wert im UserInformation-Objekt.
Assert.AreEqual("J. D.", doc.FieldOptions.CurrentUser.Initials);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.USERINITIALS.docx");
```

### Siehe auch

* class [FieldUserInitials](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
