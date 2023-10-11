---
title: ITextShaperFactory.GetTextShaper
second_title: Aspose.Words لمراجع .NET API
description: ITextShaperFactory طريقة. إرجاع مثيل جديد لمشكل النص للخط المحدد بواسطةfontPath وfaceIndex .
type: docs
weight: 10
url: /ar/net/aspose.words.shaping/itextshaperfactory/gettextshaper/
---
## GetTextShaper(string, int) {#gettextshaper_1}

إرجاع مثيل جديد لمشكل النص للخط المحدد بواسطة*fontPath* و*faceIndex* .

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
* مساحة الاسم [Aspose.Words.Shaping](../../itextshaperfactory/)
* المجسم [Aspose.Words](../../../)

---

## GetTextShaper(string, byte[], int) {#gettextshaper}

إرجاع مثيل جديد لمشكل النص للخط الذي يمثله*fontBlob* و*faceIndex* .

```csharp
public ITextShaper GetTextShaper(string fontId, byte[] fontBlob, int faceIndex)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| fontId | String | معرف فريد يمكن ربطه بشكل فريد بالخط المقدم*fontBlob* . |
| fontBlob | Byte[] | مجموعة بايت مع بيانات الخط. |
| faceIndex | Int32 | فهرس وجه الخط في مجموعة خطوط TrueType، أو 0 إذا*fontBlob* ليست مجموعة خطوط TrueType. |

### أنظر أيضا

* interface [ITextShaper](../../itextshaper/)
* interface [ITextShaperFactory](../)
* مساحة الاسم [Aspose.Words.Shaping](../../itextshaperfactory/)
* المجسم [Aspose.Words](../../../)


