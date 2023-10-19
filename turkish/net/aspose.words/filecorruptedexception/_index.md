---
title: FileCorruptedException Class
linktitle: FileCorruptedException
articleTitle: FileCorruptedException
second_title: Aspose.Words for .NET
description: Aspose.Words.FileCorruptedException sınıf. Belge yükleme sırasında belge bozuk göründüğünde ve yüklenmesi imkansız olduğunda atılır C#'da.
type: docs
weight: 2800
url: /tr/net/aspose.words/filecorruptedexception/
---
## FileCorruptedException class

Belge yükleme sırasında, belge bozuk göründüğünde ve yüklenmesi imkansız olduğunda atılır.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Belgelerle Programlama](https://docs.aspose.com/words/net/programming-with-documents/) dokümantasyon makalesi.

```csharp
public class FileCorruptedException : Exception
```

## Örnekler

FileCorruptedException'ın nasıl yakalanacağını gösterir.

```csharp
try
{
    // Microsoft Word kullanarak bir belgeyi açmaya çalışırken "Okunamayan içerik" hata mesajı alırsak,
    // Aspose.Words'ü kullanarak bu belgeyi yüklemeye çalışırken bir istisna oluşması ihtimali var.
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
