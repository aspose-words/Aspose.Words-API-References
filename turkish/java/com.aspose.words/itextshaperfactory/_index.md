---
title: "ITextShaperFactory"
linktitle: "ITextShaperFactory"
second_title: "Aspose.Words Java için"
description: "Java'da ITextShaper uygulamalarını oluşturmak için bir fabrika arabirimi."
type: docs
weight: 787
url: /tr/java/com.aspose.words/itextshaperfactory/
---
```
public interface ITextShaperFactory
```

Uygulama oluşturmak için bir fabrika arabirimi: [ITextShaper](../../com.aspose.words/itextshaper/) uygulamaları.
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [getTextShaper(String fontId, byte[] fontBlob, int faceIndex)](#getTextShaper-java.lang.String-byte---int) |   fontBlob  ve  faceIndex  tarafından temsil edilen yazı tipi için yeni bir metin şekillendirici örneği döndürür. |
| [getTextShaper(String fontPath, int faceIndex)](#getTextShaper-java.lang.String-int) |   fontPath  ve  faceIndex  tarafından belirtilen yazı tipi için yeni bir metin şekillendirici örneği döndürür. |
### getTextShaper(String fontId, byte[] fontBlob, int faceIndex) {#getTextShaper-java.lang.String-byte---int}
```
public abstract ITextShaper getTextShaper(String fontId, byte[] fontBlob, int faceIndex)
```


  fontBlob  ve  faceIndex  tarafından temsil edilen yazı tipi için yeni bir metin şekillendirici örneği döndürür.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fontId | java.lang.String | Sağlanan font fontBlob ile benzersiz bir şekilde ilişkilendirilebilen benzersiz bir tanımlayıcı. |
| fontBlob | byte[] | Yazı tipi verilerini içeren bayt dizisi. |
| faceIndex | int | TrueType yazı tipi koleksiyonundaki yazı tipi yüzünün bir indeksi, ya da fontBlob TrueType yazı tipi koleksiyonu değilse 0. |

**Returns:**
[ITextShaper](../../com.aspose.words/itextshaper/)
### getTextShaper(String fontPath, int faceIndex) {#getTextShaper-java.lang.String-int}
```
public abstract ITextShaper getTextShaper(String fontPath, int faceIndex)
```


  fontPath  ve  faceIndex  tarafından belirtilen yazı tipi için yeni bir metin şekillendirici örneği döndürür.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fontPath | java.lang.String | Yazı tipi dosyasına mutlak bir yol. |
| faceIndex | int | TrueType yazı tipi koleksiyonundaki yazı tipi yüzünün bir indeksi, ya da belirtilen yazı tipi dosyası TrueType yazı tipi koleksiyonu değilse 0. |

**Returns:**
[ITextShaper](../../com.aspose.words/itextshaper/)
