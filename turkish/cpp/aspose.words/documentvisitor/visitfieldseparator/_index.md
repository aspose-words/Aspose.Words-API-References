---
title: "Aspose::Words::DocumentVisitor::VisitFieldSeparator method"
linktitle: "VisitFieldSeparator"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::DocumentVisitor::VisitFieldSeparator method. C++'da belgede bir alan ayırıcıyla karşılaşıldığında çağrılır."
type: docs
weight: 22000
url: /tr/cpp/aspose.words/documentvisitor/visitfieldseparator/
---
## DocumentVisitor::VisitFieldSeparator method


Belge içinde bir alan ayırıcıyla karşılaşıldığında çağrılır.

```cpp
virtual Aspose::Words::VisitorAction Aspose::Words::DocumentVisitor::VisitFieldSeparator(System::SharedPtr<Aspose::Words::Fields::FieldSeparator> fieldSeparator)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fieldSeparator | System::SharedPtr\\<Aspose::Words::Fields::FieldSeparator\\> | Ziyaret edilen nesne. |

### ReturnValue

Sıralamayı nasıl devam ettireceğini belirten bir [VisitorAction](../../visitoraction/) değeri.
## Açıklamalar


Alan ayırıcı, belge içinde alan kodunu alan değerinden ayırır. Bazı alanların yalnızca alan kodu olduğunu ve alan ayırıcı ve alan değerine sahip olmadığını unutmayın.

Daha fazla bilgi için [VisitFieldStart()](../visitfieldstart/) adresine bakın.

## Ayrıca Bakınız

* Enum [VisitorAction](../../visitoraction/)
* Class [FieldSeparator](../../../aspose.words.fields/fieldseparator/)
* Class [DocumentVisitor](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
