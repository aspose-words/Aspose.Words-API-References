---
title: FieldUserInitials.UserInitials
second_title: Aspose.Words für .NET-API-Referenz
description: FieldUserInitials eigendom. Ruft die Initialen des aktuellen Benutzers ab oder legt diese fest.
type: docs
weight: 20
url: /de/net/aspose.words.fields/fielduserinitials/userinitials/
---
## FieldUserInitials.UserInitials property

Ruft die Initialen des aktuellen Benutzers ab oder legt diese fest.

```csharp
public string UserInitials { get; set; }
```

### Beispiele

Zeigt, wie das Feld USERINITIALS verwendet wird.

```csharp
Document doc = new Document();

// Erstellen Sie ein UserInformation-Objekt und legen Sie es als Quelle für Benutzerinformationen für alle von uns erstellten Felder fest.
UserInformation userInformation = new UserInformation();
userInformation.Initials = "J. D.";
doc.FieldOptions.CurrentUser = userInformation;

// Erstellen Sie ein USERINITIALS-Feld, um die Initialen des aktuellen Benutzers anzuzeigen.
// entnommen aus dem UserInformation-Objekt, das wir oben erstellt haben.
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

// Dies hat keinen Einfluss auf den Wert im UserInformation-Objekt.
Assert.AreEqual("J. D.", doc.FieldOptions.CurrentUser.Initials);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.USERINITIALS.docx");
```

### Siehe auch

* class [FieldUserInitials](../)
* namensraum [Aspose.Words.Fields](../../fielduserinitials/)
* Montage [Aspose.Words](../../../)


