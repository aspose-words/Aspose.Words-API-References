---
title: SaveOptions.UpdateCreatedTimeProperty
linktitle: UpdateCreatedTimeProperty
articleTitle: UpdateCreatedTimeProperty
second_title: Aspose.Words für .NET
description: Optimieren Sie Ihre SaveOptions mit der UpdateCreatedTimeProperty. Kontrollieren Sie CreatedTime-Updates vor dem Speichern und verbessern Sie so die Datengenauigkeit. Standard „false“.
type: docs
weight: 160
url: /de/net/aspose.words.saving/saveoptions/updatecreatedtimeproperty/
---
## SaveOptions.UpdateCreatedTimeProperty property

Ruft einen Wert ab oder legt ihn fest, der bestimmt, ob die[`CreatedTime`](../../../aspose.words.properties/builtindocumentproperties/createdtime/) Eigenschaft wird vor dem Speichern aktualisiert. Der Standardwert ist`FALSCH` ;

```csharp
public bool UpdateCreatedTimeProperty { get; set; }
```

## Beispiele

Zeigt, wie die Eigenschaft „CreatedTime“ eines Dokuments beim Speichern aktualisiert wird.

```csharp
Document doc = new Document();

DateTime createdTime = new DateTime(2019, 12, 20);
doc.BuiltInDocumentProperties.CreatedTime = createdTime;

// Dieses Flag bestimmt, ob die Erstellungszeit, die eine integrierte Eigenschaft ist, aktualisiert wird.
// Wenn ja, dann das Datum des letzten Speichervorgangs des Dokuments
// wobei dieses als Parameter übergebene SaveOptions-Objekt als Erstellungszeit verwendet wird.
DocSaveOptions saveOptions = new DocSaveOptions();
saveOptions.UpdateCreatedTimeProperty = isUpdateCreatedTimeProperty;

doc.Save(ArtifactsDir + "DocSaveOptions.UpdateCreatedTimeProperty.docx", saveOptions);

// Öffnen Sie das gespeicherte Dokument und überprüfen Sie dann den Wert der Eigenschaft.
doc = new Document(ArtifactsDir + "DocSaveOptions.UpdateCreatedTimeProperty.docx");

if (isUpdateCreatedTimeProperty)
    Assert.AreNotEqual(createdTime, doc.BuiltInDocumentProperties.CreatedTime);
else
    Assert.AreEqual(createdTime, doc.BuiltInDocumentProperties.CreatedTime);
```

### Siehe auch

* class [SaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
