---
title: IncorrectPasswordException Class
linktitle: IncorrectPasswordException
articleTitle: IncorrectPasswordException
second_title: .NET için Aspose.Words
description: Şifrelenmiş belgeler için parola hatalarını işleyen ve güvenli ve sorunsuz erişimi garantileyen Aspose.Words.IncorrectPasswordException sınıfını keşfedin.
type: docs
weight: 3700
url: /tr/net/aspose.words/incorrectpasswordexception/
---
## IncorrectPasswordException class

Bir belge bir parola ile şifrelenmişse ve belgeyi açarken belirtilen parola yanlışsa veya eksikse atılır.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Belgelerle Programlama](https://docs.aspose.com/words/net/programming-with-documents/) belgeleme makalesi.

```csharp
public class IncorrectPasswordException : Exception
```

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

* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
