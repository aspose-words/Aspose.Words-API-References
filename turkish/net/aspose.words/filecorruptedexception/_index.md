---
title: FileCorruptedException Class
linktitle: FileCorruptedException
articleTitle: FileCorruptedException
second_title: .NET için Aspose.Words
description: Yükleme sırasında bozuk belgeleri zahmetsizce işlemek için tasarlanmış Aspose.Words.FileCorruptedException sınıfını keşfedin. Sorunsuz belge yönetimini garantileyin!
type: docs
weight: 3210
url: /tr/net/aspose.words/filecorruptedexception/
---
## FileCorruptedException class

Belge yüklenirken, belgenin bozuk ve yüklenmesinin imkansız olduğu durumlarda atılır.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Belgelerle Programlama](https://docs.aspose.com/words/net/programming-with-documents/) belgeleme makalesi.

```csharp
public class FileCorruptedException : Exception
```

## Örnekler

FileCorruptedException'ın nasıl yakalanacağını gösterir.

```csharp
try
{
    // Microsoft Word kullanarak bir belgeyi açmaya çalıştığımızda "Okunamayan içerik" hata mesajı alırsak,
    // Aspose.Words kullanarak bu belgeyi yüklemeye çalıştığımızda bir istisna fırlatılması olasılığı yüksektir.
    Document doc = new Document(MyDir + "Corrupted document.docx");
}
catch (FileCorruptedException e)
{
    Console.WriteLine(e.Message);
}
```

### Ayrıca bakınız

* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
