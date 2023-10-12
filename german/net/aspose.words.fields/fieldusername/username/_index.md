---
title: FieldUserName.UserName
second_title: Aspose.Words für .NET-API-Referenz
description: FieldUserName eigendom. Gest oder legt den Namen des aktuellen Benutzers fest.
type: docs
weight: 20
url: /de/net/aspose.words.fields/fieldusername/username/
---
## FieldUserName.UserName property

Gest oder legt den Namen des aktuellen Benutzers fest.

```csharp
public string UserName { get; set; }
```

### Beispiele

Zeigt, wie das Feld USERNAME verwendet wird.

```csharp
Document doc = new Document();

// Erstellen Sie ein UserInformation-Objekt und legen Sie es als Quelle für Benutzerinformationen für alle von uns erstellten Felder fest.
UserInformation userInformation = new UserInformation();
userInformation.Name = "John Doe";
doc.FieldOptions.CurrentUser = userInformation;

DocumentBuilder builder = new DocumentBuilder(doc);

// Erstellen Sie ein USERNAME-Feld, um den Namen des aktuellen Benutzers anzuzeigen.
// entnommen aus dem UserInformation-Objekt, das wir oben erstellt haben.
FieldUserName fieldUserName = (FieldUserName)builder.InsertField(FieldType.FieldUserName, true);
Assert.AreEqual(userInformation.Name, fieldUserName.Result);

Assert.AreEqual(" USERNAME ", fieldUserName.GetFieldCode());
Assert.AreEqual("John Doe", fieldUserName.Result);

 // Wir können diese Eigenschaft festlegen, damit unser Feld den aktuell im UserInformation-Objekt gespeicherten Wert überschreibt.
fieldUserName.UserName = "Jane Doe";
fieldUserName.Update();

Assert.AreEqual(" USERNAME  \"Jane Doe\"", fieldUserName.GetFieldCode());
Assert.AreEqual("Jane Doe", fieldUserName.Result);

// Dies hat keinen Einfluss auf den Wert im UserInformation-Objekt.
Assert.AreEqual("John Doe", doc.FieldOptions.CurrentUser.Name);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.USERNAME.docx");
```

### Siehe auch

* class [FieldUserName](../)
* namensraum [Aspose.Words.Fields](../../fieldusername/)
* Montage [Aspose.Words](../../../)


