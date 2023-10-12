---
title: OoxmlSaveOptions.Password
second_title: Aspose.Words for .NET API Referansı
description: OoxmlSaveOptions mülk. ECMA376 Standart şifreleme algoritmasını kullanarak belgeyi şifrelemek için bir parola alır/ayarlar.
type: docs
weight: 50
url: /tr/net/aspose.words.saving/ooxmlsaveoptions/password/
---
## OoxmlSaveOptions.Password property

ECMA376 Standart şifreleme algoritmasını kullanarak belgeyi şifrelemek için bir parola alır/ayarlar.

```csharp
public string Password { get; set; }
```

### Notlar

Belgeyi şifrelemeden kaydetmek için bu özelliğin şu şekilde olması gerekir:`hükümsüz` veya boş dize.

### Örnekler

Parolayla şifrelenmiş bir Office Açık XML belgesinin nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
saveOptions.Password = "MyPassword";

doc.Save(ArtifactsDir + "OoxmlSaveOptions.Password.docx", saveOptions);

// Bu belgeyi Microsoft Word veya ile açamayacağız
// Aspose.Words doğru şifreyi girmeden.
Assert.Throws<IncorrectPasswordException>(() =>
    doc = new Document(ArtifactsDir + "OoxmlSaveOptions.Password.docx"));

// LoadOptions nesnesine doğru parolayı ileterek şifrelenmiş belgeyi açın.
doc = new Document(ArtifactsDir + "OoxmlSaveOptions.Password.docx", new LoadOptions("MyPassword"));

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### Ayrıca bakınız

* class [OoxmlSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../ooxmlsaveoptions/)
* toplantı [Aspose.Words](../../../)


