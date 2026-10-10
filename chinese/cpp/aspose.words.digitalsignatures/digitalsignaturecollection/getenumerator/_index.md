---
title: "Aspose::Words::DigitalSignatures::DigitalSignatureCollection::GetEnumerator 方法"
linktitle: "GetEnumerator"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::DigitalSignatures::DigitalSignatureCollection::GetEnumerator 方法。返回一个字典枚举器对象，可用于在 C++ 中遍历集合中的所有项。"
type: docs
weight: 9000
url: /zh/cpp/aspose.words.digitalsignatures/digitalsignaturecollection/getenumerator/
---
## DigitalSignatureCollection::GetEnumerator method


返回一个字典枚举器对象，可用于遍历集合中的所有项。

```cpp
System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::DigitalSignatures::DigitalSignature>>> Aspose::Words::DigitalSignatures::DigitalSignatureCollection::GetEnumerator() override
```


## 示例



展示如何打印已签署文档的所有数字签名。
```cpp
System::SharedPtr<Aspose::Words::DigitalSignatures::DigitalSignatureCollection> digitalSignatures = Aspose::Words::DigitalSignatures::DigitalSignatureUtil::LoadSignatures(get_MyDir() + u"Digitally signed.docx");

{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::DigitalSignatures::DigitalSignature>>> enumerator = digitalSignatures->GetEnumerator();
    while (enumerator->MoveNext())
    {
        System::SharedPtr<Aspose::Words::DigitalSignatures::DigitalSignature> ds = enumerator->get_Current();

        if (ds != nullptr)
        {
            std::cout << System::ObjectExt::ToString(ds) << std::endl;
        }
    }
}
```

## 另见

* Class [DigitalSignature](../../digitalsignature/)
* Class [DigitalSignatureCollection](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
