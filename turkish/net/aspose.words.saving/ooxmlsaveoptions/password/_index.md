---
title: OoxmlSaveOptions.Password
linktitle: Password
articleTitle: Password
second_title: .NET için Aspose.Words
description: Belgelerinizi OoxmlSaveOptions ile güvence altına alın! Gelişmiş veri koruması için ECMA376 Standardını kullanarak şifreleme için kolayca bir parola ayarlayın.
type: docs
weight: 60
url: /tr/net/aspose.words.saving/ooxmlsaveoptions/password/
---
## OoxmlSaveOptions.Password property

ECMA376 Standart şifreleme algoritmasını kullanarak belgeyi şifrelemek için bir parola alır/ayarlar.

```csharp
public string Password { get; set; }
```

## Notlar

Belgeyi şifrelemeden kaydetmek için bu özellik olmalıdır`hükümsüz` veya boş dize.

## Örnekler

Parola ile şifrelenmiş bir Office Open XML belgesinin nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
saveOptions.Password = "MyPassword";

doc.Save(ArtifactsDir + "OoxmlSaveOptions.Password.docx", saveOptions);

// Bu belgeyi Microsoft Word veya
// Doğru şifreyi sağlamadan Aspose.Words.
Assert.Throws<IncorrectPasswordException>(() =>
    doc = new Document(ArtifactsDir + "OoxmlSaveOptions.Password.docx"));

// Doğru parolayı bir LoadOptions nesnesine geçirerek şifrelenmiş belgeyi açın.
doc = new Document(ArtifactsDir + "OoxmlSaveOptions.Password.docx", new LoadOptions("MyPassword"));

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### Ayrıca bakınız

* class [OoxmlSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
