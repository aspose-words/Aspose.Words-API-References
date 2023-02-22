---
title: DigitalSignatureCollection.GetEnumerator
second_title: Aspose.Words for .NET API 参考
description: DigitalSignatureCollection 方法. 返回一个字典枚举器对象可用于迭代集合中的所有项目
type: docs
weight: 50
url: /zh/net/aspose.words.digitalsignatures/digitalsignaturecollection/getenumerator/
---
## DigitalSignatureCollection.GetEnumerator method

返回一个字典枚举器对象，可用于迭代集合中的所有项目。

```csharp
public IEnumerator<DigitalSignature> GetEnumerator()
```

### 例子

演示如何打印已签名文档的所有数字签名。

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

### 也可以看看

* class [DigitalSignature](../../digitalsignature/)
* class [DigitalSignatureCollection](../)
* 命名空间 [Aspose.Words.DigitalSignatures](../../digitalsignaturecollection/)
* 部件 [Aspose.Words](../../../)


