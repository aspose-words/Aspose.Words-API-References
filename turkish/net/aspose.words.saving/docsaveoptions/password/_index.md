---
title: DocSaveOptions.Password
linktitle: Password
articleTitle: Password
second_title: .NET için Aspose.Words
description: Belgelerinizi DocSaveOptions ile güvenceye alın! Hassas bilgilerinizi korumak için RC4 şifrelemesi için kolayca bir parola ayarlayın veya alın.
type: docs
weight: 40
url: /tr/net/aspose.words.saving/docsaveoptions/password/
---
## DocSaveOptions.Password property

Belgeyi RC4 şifreleme yöntemini kullanarak şifrelemek için bir parola alır/ayarlar.

```csharp
public string Password { get; set; }
```

## Notlar

Belgeyi şifrelemeden kaydetmek için bu özellik olmalıdır`hükümsüz` veya boş dize.

## Örnekler

Eski Microsoft Word biçimleri için kaydetme seçeneklerinin nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Hello world!");

DocSaveOptions options = new DocSaveOptions(SaveFormat.Doc);

// Microsoft Word veya Aspose.Words ile belgenin yüklenmesini koruyacak bir parola belirleyin.
// Bu işlemin belgenin içeriğini hiçbir şekilde şifrelemediğini unutmayın.
options.Password = "MyPassword";

// Belgede yönlendirme fişi varsa, bu bayrağı true olarak ayarlayarak kaydederken bunu koruyabiliriz.
options.SaveRoutingSlip = true;

doc.Save(ArtifactsDir + "DocSaveOptions.SaveAsDoc.doc", options);

// Belgeyi yükleyebilmek için,
// DocSaveOptions nesnesinde belirttiğimiz şifreyi bir LoadOptions nesnesine uygulamamız gerekecek.
Assert.Throws<IncorrectPasswordException>(() => doc = new Document(ArtifactsDir + "DocSaveOptions.SaveAsDoc.doc"));

LoadOptions loadOptions = new LoadOptions("MyPassword");
doc = new Document(ArtifactsDir + "DocSaveOptions.SaveAsDoc.doc", loadOptions);

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### Ayrıca bakınız

* class [DocSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
