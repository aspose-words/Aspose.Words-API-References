---
title: DocSaveOptions
linktitle: DocSaveOptions
articleTitle: DocSaveOptions
second_title: Aspose.Words for .NET
description: DocSaveOptions inşaatçı. Bir belgeyi kaydetmek için kullanılabilecek bu sınıfın yeni bir örneğini başlatır.Doc format C#'da.
type: docs
weight: 10
url: /tr/net/aspose.words.saving/docsaveoptions/docsaveoptions/
---
## DocSaveOptions() {#constructor}

Bir belgeyi kaydetmek için kullanılabilecek bu sınıfın yeni bir örneğini başlatır.Doc format.

```csharp
public DocSaveOptions()
```

## Örnekler

Eski Microsoft Word formatları için kaydetme seçeneklerinin nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Hello world!");

DocSaveOptions options = new DocSaveOptions(SaveFormat.Doc);

// Belgenin Microsoft Word veya Aspose.Words tarafından yüklenmesini koruyacak bir şifre belirleyin.
// Bunun belgenin içeriğini hiçbir şekilde şifrelemediğini unutmayın.
options.Password = "MyPassword";

// Doküman bir yönlendirme fişi içeriyorsa bu bayrağı true yaparak kaydederken onu koruyabiliriz.
options.SaveRoutingSlip = true;

doc.Save(ArtifactsDir + "DocSaveOptions.SaveAsDoc.doc", options);

// Dokümanı yükleyebilmek için,
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

Bir belgeyi kaydetmek için kullanılabilecek bu sınıfın yeni bir örneğini başlatır.Doc veya Dot format.

```csharp
public DocSaveOptions(SaveFormat saveFormat)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| saveFormat | SaveFormat | OlabilirDoc veyaDot. |

## Örnekler

Eski Microsoft Word formatları için kaydetme seçeneklerinin nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Hello world!");

DocSaveOptions options = new DocSaveOptions(SaveFormat.Doc);

// Belgenin Microsoft Word veya Aspose.Words tarafından yüklenmesini koruyacak bir şifre belirleyin.
// Bunun belgenin içeriğini hiçbir şekilde şifrelemediğini unutmayın.
options.Password = "MyPassword";

// Doküman bir yönlendirme fişi içeriyorsa bu bayrağı true yaparak kaydederken onu koruyabiliriz.
options.SaveRoutingSlip = true;

doc.Save(ArtifactsDir + "DocSaveOptions.SaveAsDoc.doc", options);

// Dokümanı yükleyebilmek için,
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
