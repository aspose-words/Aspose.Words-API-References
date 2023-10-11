---
title: FieldImport.IsLinked
second_title: Aspose.Words für .NET-API-Referenz
description: FieldImport eigendom. Ruft ab oder legt fest ob die Dateigröße reduziert werden soll indem keine Grafikdaten mit dem Dokument gespeichert werden.
type: docs
weight: 30
url: /de/net/aspose.words.fields/fieldimport/islinked/
---
## FieldImport.IsLinked property

Ruft ab oder legt fest, ob die Dateigröße reduziert werden soll, indem keine Grafikdaten mit dem Dokument gespeichert werden.

```csharp
public bool IsLinked { get; set; }
```

### Beispiele

Zeigt, wie Bilder mithilfe der Felder IMPORT und INCLUDEPICTURE eingefügt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Nachfolgend finden Sie zwei ähnliche Feldtypen, mit denen wir Bilder anzeigen können, die aus dem lokalen Dateisystem verknüpft sind.
// 1 – Das INCLUDEPICTURE-Feld:
FieldIncludePicture fieldIncludePicture = (FieldIncludePicture)builder.InsertField(FieldType.FieldIncludePicture, true);
fieldIncludePicture.SourceFullName = ImageDir + "Transparent background logo.png";

Assert.True(Regex.Match(fieldIncludePicture.GetFieldCode(), " INCLUDEPICTURE  .*").Success);

// Den PNG32.FLT-Filter anwenden.
fieldIncludePicture.GraphicFilter = "PNG32";
fieldIncludePicture.IsLinked = true;
fieldIncludePicture.ResizeHorizontally = true;
fieldIncludePicture.ResizeVertically = true;

// 2 – Das IMPORT-Feld:
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


