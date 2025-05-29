---
title: FieldIncludePicture.IsLinked
linktitle: IsLinked
articleTitle: IsLinked
second_title: Aspose.Words für .NET
description: Optimieren Sie Ihre Dokumente mit der Eigenschaft „FieldIncludePicture IsLinked“ – steuern Sie die Grafikspeicherung, um die Dateigröße zu reduzieren und die Leistung zu verbessern.
type: docs
weight: 30
url: /de/net/aspose.words.fields/fieldincludepicture/islinked/
---
## FieldIncludePicture.IsLinked property

Ruft ab oder legt fest, ob die Dateigröße reduziert werden soll, indem Grafikdaten nicht mit dem Dokument gespeichert werden.

```csharp
public bool IsLinked { get; set; }
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
