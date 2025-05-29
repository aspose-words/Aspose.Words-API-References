---
title: DocSaveOptions
linktitle: DocSaveOptions
articleTitle: DocSaveOptions
second_title: .NET için Aspose.Words
description: Doc formatında sorunsuz belge kaydetme için DocSaveOptions oluşturucusunu keşfedin. Kolay ve etkili belge yönetimiyle iş akışınızı geliştirin.
type: docs
weight: 10
url: /tr/net/aspose.words.saving/docsaveoptions/docsaveoptions/
---
## DocSaveOptions() {#constructor}

Bu sınıfın, bir belgeyi kaydetmek için kullanılabilecek yeni bir örneğini başlatır.Doc biçim.

```csharp
public DocSaveOptions()
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

* class [DocSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)

---

## DocSaveOptions(*[SaveFormat](../../../aspose.words/saveformat/)*) {#constructor_1}

Bu sınıfın, bir belgeyi kaydetmek için kullanılabilecek yeni bir örneğini başlatır.Doc veya Dot biçim.

```csharp
public DocSaveOptions(SaveFormat saveFormat)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| saveFormat | SaveFormat | OlabilirDoc veyaDot. |

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

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [DocSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
