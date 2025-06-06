---
title: ITextShaperFactory.GetTextShaper
linktitle: GetTextShaper
articleTitle: GetTextShaper
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة GetTextShaper في ITextShaperFactory لإنشاء مشكل نص مخصص لاحتياجات الخط الخاصة بك، مما يعزز تجربة عرض النص لديك.
type: docs
weight: 10
url: /ar/net/aspose.words.shaping/itextshaperfactory/gettextshaper/
---
## GetTextShaper(*string, int*) {#gettextshaper_1}

يعيد مثيلًا جديدًا لمشكل النص للخط المحدد بواسطة*fontPath* و*faceIndex* .

```csharp
public ITextShaper GetTextShaper(string fontPath, int faceIndex)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| fontPath | String | المسار المطلق لملف الخط. |
| faceIndex | Int32 | فهرس لوجه الخط في مجموعة خطوط TrueType، أو 0 إذا كان ملف الخط المحدد ليس مجموعة خطوط TrueType. |

### أنظر أيضا

* interface [ITextShaper](../../itextshaper/)
* interface [ITextShaperFactory](../)
* مساحة الاسم [Aspose.Words.Shaping](../../../aspose.words.shaping/)
* المجسم [Aspose.Words](../../../)

---

## GetTextShaper(*string, byte[], int*) {#gettextshaper}

يعيد مثيلًا جديدًا لمشكل النص للخط الذي يمثله*fontBlob* و*faceIndex* .

```csharp
public ITextShaper GetTextShaper(string fontId, byte[] fontBlob, int faceIndex)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| fontId | String | معرف فريد يمكن ربطه بشكل فريد بالخط المقدم*fontBlob* . |
| fontBlob | Byte[] | مصفوفة بايتات تحتوي على بيانات الخط. |
| faceIndex | Int32 | فهرس لوجه الخط في مجموعة خطوط TrueType، أو 0 إذا*fontBlob* ليست مجموعة خطوط TrueType. |

### أنظر أيضا

* interface [ITextShaper](../../itextshaper/)
* interface [ITextShaperFactory](../)
* مساحة الاسم [Aspose.Words.Shaping](../../../aspose.words.shaping/)
* المجسم [Aspose.Words](../../../)
