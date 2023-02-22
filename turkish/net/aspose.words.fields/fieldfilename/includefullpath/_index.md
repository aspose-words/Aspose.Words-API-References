---
title: FieldFileName.IncludeFullPath
second_title: Aspose.Words for .NET API Referansı
description: FieldFileName mülk. Tam dosya yolu adının dahil edilip edilmeyeceğini alır veya ayarlar.
type: docs
weight: 20
url: /tr/net/aspose.words.fields/fieldfilename/includefullpath/
---
## FieldFileName.IncludeFullPath property

Tam dosya yolu adının dahil edilip edilmeyeceğini alır veya ayarlar.

```csharp
public bool IncludeFullPath { get; set; }
```

### Örnekler

FILENAME alanı için varsayılan değeri geçersiz kılmak için FieldOptions'ın nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Document.docx");
DocumentBuilder builder = new DocumentBuilder(doc);

builder.MoveToDocumentEnd();
builder.Writeln();

// Bu FILENAME alanı yüklediğimiz belgenin yerel sistem dosya adını gösterecek.
FieldFileName field = (FieldFileName)builder.InsertField(FieldType.FieldFileName, true);
field.Update();

Assert.AreEqual(" FILENAME ", field.GetFieldCode());
Assert.AreEqual("Document.docx", field.Result);

builder.Writeln();

// Varsayılan olarak, FILENAME alanı dosyanın adını gösterir, ancak tam yerel dosya sistemi yolunu göstermez.
// Tam dosya yolunu göstermesi için bir bayrak ayarlayabiliriz.
field = (FieldFileName)builder.InsertField(FieldType.FieldFileName, true);
field.IncludeFullPath = true;
field.Update();

Assert.AreEqual(MyDir + "Document.docx", field.Result);

// Bu özellik için de bir değer ayarlayabiliriz.
// DOSYAADI alanının görüntülediği değeri geçersiz kıl.
doc.FieldOptions.FileName = "FieldOptions.FILENAME.docx";
field.Update();

Assert.AreEqual(" FILENAME  \\p", field.GetFieldCode());
Assert.AreEqual("FieldOptions.FILENAME.docx", field.Result);

doc.UpdateFields();
doc.Save(ArtifactsDir + doc.FieldOptions.FileName);
```

### Ayrıca bakınız

* class [FieldFileName](../)
* ad alanı [Aspose.Words.Fields](../../fieldfilename/)
* toplantı [Aspose.Words](../../../)


