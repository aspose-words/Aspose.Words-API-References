---
title: FieldImport.SourceFullName
second_title: Aspose.Words für .NET-API-Referenz
description: FieldImport eigendom. Ruft den Speicherort des Bildes ab oder legt ihn fest.
type: docs
weight: 40
url: /de/net/aspose.words.fields/fieldimport/sourcefullname/
---
## FieldImport.SourceFullName property

Ruft den Speicherort des Bildes ab oder legt ihn fest.

```csharp
public string SourceFullName { get; set; }
```

### Beispiele

Zeigt, wie Bilder mit den Feldern IMPORT und INCLUDEPICTURE eingefügt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Unten sind zwei ähnliche Feldtypen, die wir verwenden können, um Bilder anzuzeigen, die vom lokalen Dateisystem verlinkt sind.
// 1 - Das INCLUDEPICTURE-Feld:
FieldIncludePicture fieldIncludePicture = (FieldIncludePicture)builder.InsertField(FieldType.FieldIncludePicture, true);
fieldIncludePicture.SourceFullName = ImageDir + "Transparent background logo.png";

Assert.True(Regex.Match(fieldIncludePicture.GetFieldCode(), " INCLUDEPICTURE  .*").Success);

// Den PNG32.FLT-Filter anwenden.
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

* class [FieldImport](../)
* namensraum [Aspose.Words.Fields](../../fieldimport/)
* Montage [Aspose.Words](../../../)


