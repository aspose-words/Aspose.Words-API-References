---
title: FieldImport.IsLinked
second_title: Aspose.Words per .NET API Reference
description: FieldImport proprietà. Ottiene o imposta se ridurre la dimensione del file non memorizzando i dati grafici con il documento.
type: docs
weight: 30
url: /it/net/aspose.words.fields/fieldimport/islinked/
---
## FieldImport.IsLinked property

Ottiene o imposta se ridurre la dimensione del file non memorizzando i dati grafici con il documento.

```csharp
public bool IsLinked { get; set; }
```

### Esempi

Mostra come inserire immagini utilizzando i campi IMPORT e INCLUDEPICTURE.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Di seguito sono riportati due tipi di campo simili che possiamo utilizzare per visualizzare le immagini collegate dal file system locale.
// 1 - Il campo INCLUDEPICTURE:
FieldIncludePicture fieldIncludePicture = (FieldIncludePicture)builder.InsertField(FieldType.FieldIncludePicture, true);
fieldIncludePicture.SourceFullName = ImageDir + "Transparent background logo.png";

Assert.True(Regex.Match(fieldIncludePicture.GetFieldCode(), " INCLUDEPICTURE  .*").Success);

// Applica il filtro PNG32.FLT.
fieldIncludePicture.GraphicFilter = "PNG32";
fieldIncludePicture.IsLinked = true;
fieldIncludePicture.ResizeHorizontally = true;
fieldIncludePicture.ResizeVertically = true;

// 2 - Il campo IMPORT:
FieldImport fieldImport = (FieldImport)builder.InsertField(FieldType.FieldImport, true);
fieldImport.SourceFullName = ImageDir + "Transparent background logo.png";
fieldImport.GraphicFilter = "PNG32";
fieldImport.IsLinked = true;

Assert.True(Regex.Match(fieldImport.GetFieldCode(), " IMPORT  .* \\\\c PNG32 \\\\d").Success);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.IMPORT.INCLUDEPICTURE.docx");
```

### Guarda anche

* class [FieldImport](../)
* spazio dei nomi [Aspose.Words.Fields](../../fieldimport/)
* assemblea [Aspose.Words](../../../)


