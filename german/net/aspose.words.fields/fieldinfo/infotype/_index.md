---
title: FieldInfo.InfoType
linktitle: InfoType
articleTitle: InfoType
second_title: Aspose.Words für .NET
description: FieldInfo InfoType eigendom. Ruft den Typ der einzufügenden Dokumenteigenschaft ab oder legt diesen fest in C#.
type: docs
weight: 20
url: /de/net/aspose.words.fields/fieldinfo/infotype/
---
## FieldInfo.InfoType property

Ruft den Typ der einzufügenden Dokumenteigenschaft ab oder legt diesen fest.

```csharp
public string InfoType { get; set; }
```

## Beispiele

Zeigt, wie mit INFO-Feldern gearbeitet wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Legen Sie einen Wert für die integrierte Eigenschaft „Kommentare“ fest und fügen Sie dann ein INFO-Feld ein, um den Wert dieser Eigenschaft anzuzeigen.
doc.BuiltInDocumentProperties.Comments = "My comment";
FieldInfo field = (FieldInfo)builder.InsertField(FieldType.FieldInfo, true);
field.InfoType = "Comments";
field.Update();

Assert.AreEqual(" INFO  Comments", field.GetFieldCode());
Assert.AreEqual("My comment", field.Result);

builder.Writeln();

// Einen Wert für die NewValue-Eigenschaft des Felds festlegen und aktualisieren
// Das Feld überschreibt auch die entsprechende integrierte Eigenschaft mit dem neuen Wert.
field = (FieldInfo)builder.InsertField(FieldType.FieldInfo, true);
field.InfoType = "Comments";
field.NewValue = "New comment";
field.Update();

Assert.AreEqual(" INFO  Comments \"New comment\"", field.GetFieldCode());
Assert.AreEqual("New comment", field.Result);
Assert.AreEqual("New comment", doc.BuiltInDocumentProperties.Comments);

doc.Save(ArtifactsDir + "Field.INFO.docx");
```

### Siehe auch

* class [FieldInfo](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
