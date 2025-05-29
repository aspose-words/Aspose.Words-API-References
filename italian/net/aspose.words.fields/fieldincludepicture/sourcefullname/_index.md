---
title: FieldIncludePicture.SourceFullName
linktitle: SourceFullName
articleTitle: SourceFullName
second_title: Aspose.Words per .NET
description: Scopri la proprietà FieldIncludePicture SourceFullName. Gestisci facilmente la posizione delle immagini con IRI per una migliore integrazione dei media e un'esperienza utente fluida.
type: docs
weight: 60
url: /it/net/aspose.words.fields/fieldincludepicture/sourcefullname/
---
## FieldIncludePicture.SourceFullName property

Ottiene o imposta la posizione dell'immagine utilizzando un IRI.

```csharp
public string SourceFullName { get; set; }
```

## Esempi

Mostra come inserire immagini utilizzando i campi IMPORT e INCLUDEPICTURE.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Di seguito sono riportati due tipi di campi simili che possiamo utilizzare per visualizzare le immagini collegate dal file system locale.
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

* class [FieldIncludePicture](../)
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
