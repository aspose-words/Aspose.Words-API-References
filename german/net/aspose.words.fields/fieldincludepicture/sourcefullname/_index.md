---
title: FieldIncludePicture.SourceFullName
linktitle: SourceFullName
articleTitle: SourceFullName
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „FieldIncludePicture SourceFullName“. Verwalten Sie Bildstandorte ganz einfach mit IRI für eine verbesserte Medienintegration und ein nahtloses Benutzererlebnis.
type: docs
weight: 60
url: /de/net/aspose.words.fields/fieldincludepicture/sourcefullname/
---
## FieldIncludePicture.SourceFullName property

Ruft den Speicherort des Bildes mithilfe eines IRI ab oder legt ihn fest.

```csharp
public string SourceFullName { get; set; }
```

## Beispiele

Zeigt, wie Bilder mithilfe der Felder IMPORT und INCLUDEPICTURE eingefügt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Unten sind zwei ähnliche Feldtypen, die wir verwenden können, um Bilder anzuzeigen, die vom lokalen Dateisystem verknüpft sind.
// 1 - Das Feld INCLUDEPICTURE:
FieldIncludePicture fieldIncludePicture = (FieldIncludePicture)builder.InsertField(FieldType.FieldIncludePicture, true);
fieldIncludePicture.SourceFullName = ImageDir + "Transparent background logo.png";

Assert.True(Regex.Match(fieldIncludePicture.GetFieldCode(), " INCLUDEPICTURE  .*").Success);

// Wenden Sie den PNG32.FLT-Filter an.
fieldIncludePicture.GraphicFilter = "PNG32";
fieldIncludePicture.IsLinked = true;
fieldIncludePicture.ResizeHorizontally = true;
fieldIncludePicture.ResizeVertically = true;

// 2 - Das IMPORT-Feld:
FieldImport fieldImport = (FieldImport)builder.InsertField(FieldType.FieldImport, true);
fieldImport.SourceFullName = ImageDir + "Transparent background logo.png";
fieldImport.GraphicFilter = "PNG32";
fieldImport.IsLinked = true;

Assert.True(Regex.Match(fieldImport.GetFieldCode(), " IMPORT  .* \\\\c PNG32 \\\\d").Success);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.IMPORT.INCLUDEPICTURE.docx");
```

### Siehe auch

* class [FieldIncludePicture](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
