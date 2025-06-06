---
title: LoadOptions.PreserveIncludePictureField
linktitle: PreserveIncludePictureField
articleTitle: PreserveIncludePictureField
second_title: Aspose.Words für .NET
description: Steuern Sie das Feld INCLUDEPICTURE in Microsoft Word-Formaten mit LoadOptions PreserveIncludePictureField. Verwalten Sie die Dokumentformatierung ganz einfach für optimale Ergebnisse.
type: docs
weight: 120
url: /de/net/aspose.words.loading/loadoptions/preserveincludepicturefield/
---
## LoadOptions.PreserveIncludePictureField property

Ruft ab oder legt fest, ob das Feld INCLUDEPICTURE beim Lesen von Microsoft Word-Formaten beibehalten werden soll. Der Standardwert ist`FALSCH` .

```csharp
public bool PreserveIncludePictureField { get; set; }
```

## Bemerkungen

Standardmäßig wird das Feld INCLUDEPICTURE in ein Shape-Objekt konvertiert. Sie können dies überschreiben, wenn das Feld erhalten bleiben soll, z. B. wenn Sie es programmgesteuert aktualisieren möchten. Beachten Sie jedoch, dass dieser Ansatz für Aspose.Words nicht üblich ist. Verwenden Sie ihn auf eigene Gefahr.

Ein möglicher Anwendungsfall könnte die Verwendung eines MERGEFIELD als untergeordnetes Feld sein, um den Quellpfad des Bildes dynamisch zu ändern. In diesem Fall muss INCLUDEPICTURE im Modell erhalten bleiben.

## Beispiele

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

    // Wir können ein Flag in einem LoadOptions-Objekt setzen, um zu entscheiden, ob alle INCLUDEPICTURE-Felder konvertiert werden sollen
    // in Bildformen, wenn ein Dokument geladen wird, das diese enthält.
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
* namensraum [Aspose.Words.Loading](../../../aspose.words.loading/)
* Montage [Aspose.Words](../../../)
