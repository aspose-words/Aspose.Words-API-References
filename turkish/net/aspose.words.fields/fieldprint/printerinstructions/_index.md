---
title: FieldPrint.PrinterInstructions
linktitle: PrinterInstructions
articleTitle: PrinterInstructions
second_title: Aspose.Words for .NET
description: FieldPrint PrinterInstructions mülk. Yazıcıya özel kontrol kodu karakterlerini veya PostScript talimatlarını alır veya ayarlar C#'da.
type: docs
weight: 30
url: /tr/net/aspose.words.fields/fieldprint/printerinstructions/
---
## FieldPrint.PrinterInstructions property

Yazıcıya özel kontrol kodu karakterlerini veya PostScript talimatlarını alır veya ayarlar.

```csharp
public string PrinterInstructions { get; set; }
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
