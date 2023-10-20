---
title: FieldPrint.PostScriptGroup
linktitle: PostScriptGroup
articleTitle: PostScriptGroup
second_title: Aspose.Words for .NET
description: FieldPrint PostScriptGroup mülk. PostScript talimatlarının üzerinde çalıştığı çizim dikdörtgenini alır veya ayarlar C#'da.
type: docs
weight: 20
url: /tr/net/aspose.words.fields/fieldprint/postscriptgroup/
---
## FieldPrint.PostScriptGroup property

PostScript talimatlarının üzerinde çalıştığı çizim dikdörtgenini alır veya ayarlar.

```csharp
public string PostScriptGroup { get; set; }
```

## Örnekler

PRINT alanının eklenmesini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("My paragraph");

// PRINT alanı yazıcıya talimat gönderebilir.
FieldPrint field = (FieldPrint)builder.InsertField(FieldType.FieldPrint, true);

// Yazıcının talimatları uygulayacağı alanı ayarlayın.
// Bu durumda PRINT alanımızı içeren paragraf olacaktır.
field.PostScriptGroup = "para";

// Belgemizi yazdırmak için PostScript'i destekleyen bir yazıcı kullandığımızda,
// bu komut "field.PostScriptGroup"ta belirttiğimiz alanın tamamını beyaza çevirecektir.
field.PrinterInstructions = "erasepage";

Assert.AreEqual(" PRINT  erasepage \\p para", field.GetFieldCode());

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.PRINT.docx");
```

### Ayrıca bakınız

* class [FieldPrint](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)
