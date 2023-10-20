---
title: DigitalSignatureCollection.GetEnumerator
linktitle: GetEnumerator
articleTitle: GetEnumerator
second_title: Aspose.Words لـ .NET
description: DigitalSignatureCollection GetEnumerator طريقة. يُرجع كائن عداد القاموس الذي يمكن استخدامه للتكرار على كافة العناصر الموجودة في المجموعة في C#.
type: docs
weight: 50
url: /ar/net/aspose.words.digitalsignatures/digitalsignaturecollection/getenumerator/
---
## DigitalSignatureCollection.GetEnumerator method

يُرجع كائن عداد القاموس الذي يمكن استخدامه للتكرار على كافة العناصر الموجودة في المجموعة.

```csharp
public IEnumerator<DigitalSignature> GetEnumerator()
```

## أمثلة

يوضح كيفية طباعة جميع التوقيعات الرقمية للمستند الموقع.

```csharp
DigitalSignatureCollection digitalSignatures =
    DigitalSignatureUtil.LoadSignatures(MyDir + "Digitally signed.docx");

using (IEnumerator<DigitalSignature> enumerator = digitalSignatures.GetEnumerator())
{
    while (enumerator.MoveNext())
    {
        DigitalSignature ds = enumerator.Current;

        if (ds != null)
            Console.WriteLine(ds.ToString());
    }
}
```

### أنظر أيضا

* class [DigitalSignature](../../digitalsignature/)
* class [DigitalSignatureCollection](../)
* مساحة الاسم [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* المجسم [Aspose.Words](../../../)
