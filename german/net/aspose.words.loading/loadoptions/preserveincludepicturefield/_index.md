---
title: LoadOptions.PreserveIncludePictureField
second_title: Aspose.Words für .NET-API-Referenz
description: LoadOptions eigendom. Ruft ab oder legt fest ob das INCLUDEPICTUREFeld beim Lesen von Microsoft WordFormaten beibehalten werden soll. Der Standardwert istFALSCH .
type: docs
weight: 120
url: /de/net/aspose.words.loading/loadoptions/preserveincludepicturefield/
---
## LoadOptions.PreserveIncludePictureField property

Ruft ab oder legt fest, ob das INCLUDEPICTURE-Feld beim Lesen von Microsoft Word-Formaten beibehalten werden soll. Der Standardwert ist`FALSCH` .

```csharp
public bool PreserveIncludePictureField { get; set; }
```

### Bemerkungen

Standardmäßig wird das INCLUDEPICTURE-Feld in ein Formobjekt konvertiert. Sie können dies überschreiben, wenn das Feld erhalten bleiben soll, beispielsweise wenn Sie es programmgesteuert aktualisieren möchten. Beachten Sie jedoch, dass dieser -Ansatz für Aspose.Words nicht üblich ist. Die Nutzung erfolgt auf eigene Gefahr.

Einer der möglichen Anwendungsfälle könnte die Verwendung eines MERGEFIELD als untergeordnetes Feld sein, um den Quellpfad des Bildes dynamisch zu ändern. In diesem Fall muss das INCLUDEPICTURE im Modell erhalten bleiben.

### Beispiele

Zeigt, wie INCLUDEPICTURE-Felder beim Laden eines Dokuments beibehalten oder verworfen werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldIncludePicture includePicture = (FieldIncludePicture)builder.InsertField(FieldType.FieldIncludePicture, true);
includePicture.SourceFullName = ImageDir + "Transparent background logo.png";
includePicture.Update(true);

using (MemoryStream docStream = new MemoryStream())
{
    doc.Save(docStream, new OoxmlSaveOptions(SaveFormat.Docx));

    // Wir können in einem LoadOptions-Objekt ein Flag setzen, um zu entscheiden, ob alle INCLUDEPICTURE-Felder konvertiert werden sollen
    // in Bildformen konvertieren, wenn ein Dokument geladen wird, das diese enthält.
    LoadOptions loadOptions = new LoadOptions
    {
        PreserveIncludePictureField = preserveIncludePictureField
    };

    doc = new Document(docStream, loadOptions);

    if (preserveIncludePictureField)
    {
        Assert.True(doc.Range.Fields.Any(f => f.Type == FieldType.FieldIncludePicture));

        doc.UpdateFields();
        doc.Save(ArtifactsDir + "Field.PreserveIncludePicture.docx");
    }
    else
    {
        Assert.False(doc.Range.Fields.Any(f => f.Type == FieldType.FieldIncludePicture));
    }
}
```

### Siehe auch

* class [LoadOptions](../)
* namensraum [Aspose.Words.Loading](../../loadoptions/)
* Montage [Aspose.Words](../../../)


