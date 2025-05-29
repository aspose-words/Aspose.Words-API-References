---
title: FieldInfo.NewValue
linktitle: NewValue
articleTitle: NewValue
second_title: Aspose.Words für .NET
description: Entdecken Sie die FieldInfo NewValue-Eigenschaft, verwalten Sie optionale Werte einfach, um Ihre Datenaktualisierungen zu verbessern und Ihr Codierungserlebnis zu optimieren.
type: docs
weight: 30
url: /de/net/aspose.words.fields/fieldinfo/newvalue/
---
## FieldInfo.NewValue property

Ruft einen optionalen Wert ab oder legt ihn fest, der die Eigenschaft aktualisiert.

```csharp
public string NewValue { get; set; }
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

// Festlegen eines Wertes für die NewValue-Eigenschaft des Felds und Aktualisieren
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
